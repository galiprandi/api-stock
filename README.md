# 📦 api-stock

Este es un repositorio educativo diseñado para aprender paso a paso cómo construir una API REST moderna para control de inventario utilizando TypeScript, Express v5, Prisma ORM y PostgreSQL.

## Propósito

Este proyecto está estructurado como una guía práctica de aprendizaje. Al seguir las instrucciones paso a paso, aprenderás a construir una API profesional mientras aplicas las mejores prácticas de desarrollo moderno. El objetivo es proporcionarte las habilidades necesarias para convertirte en un desarrollador backend moderno y competente.

### Herramientas Necesarias

- [Visual Studio Code](https://code.visualstudio.com/) (Editor de código recomendado)
- [Github Copilot](https://copilot.github.com/) (como asistente de código)
- [GitHub](https://github.com/) (para control de versiones)
- [Github cli](https://cli.github.com/) (para manejar repositorios desde la terminal)
- [ChatGPT](https://chat.openai.com/) (como asistente de aprendizaje)
- [Node.js y npm](https://nodejs.org/) (para ejecutar y construir la aplicación)

### Lo que Aprenderás

- Configuración de un proyecto TypeScript moderno
- Uso de Express.js v5 con TypeScript
- Implementación de endpoints REST
- Manejo de errores y validaciones
- Pruebas unitarias y de integración
- Modelado de datos con Prisma ORM
- Integración con PostgreSQL
- Documentación de API
- Despliegue en un entorno de producción

### Resultado Final

Al completar todos los pasos, tendrás una API completamente funcional para control de inventario que permite:

- Gestión completa de productos (CRUD)
- Control de stock
- Registro de movimientos de inventario
- Documentación completa de la API
- Pruebas automatizadas para asegurar la calidad del código
- Despliegue en un servidor de producción

### Público Objetivo

Este repositorio está dirigido a desarrolladores que desean mejorar sus habilidades en el desarrollo backend utilizando tecnologías modernas. Es ideal para aquellos que tienen conocimientos básicos de programación y desean profundizar en el desarrollo de APIs RESTful con TypeScript y Node.js.

### Contribuciones

Las contribuciones son bienvenidas. Si deseas mejorar este proyecto, por favor, abre un issue o envía un pull request con tus sugerencias y mejoras.

### Autor

Este proyecto fue creado por [Germán Aliprandi](mailto:galiprandi@gmail.com) y te invito a contactarme si tienes alguna pregunta o sugerencia.

### Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles.

## Paso 1: Fork del repositorio [api-stock](https://github.com/galiprandi/api-stock)

> 📚 ¿Que es un fork? Un fork es una copia de un repositorio que se crea en tu cuenta de GitHub. Permite que puedas hacer cambios en el proyecto original sin afectar el repositorio principal. Los forks son útiles cuando deseas contribuir a un proyecto de código abierto, ya que puedes trabajar en tus propias modificaciones y luego proponer que se integren en el proyecto original mediante un pull request.

### Verificar que tengas una cuenta en GitHub

Si no tienes una cuenta en GitHub, [regístrate en GitHub](https://github.com/join).
Si ya tienes una cuenta, asegúrate de haber iniciado sesión.

### Instalar y configurar Git y GitHub CLI

Sigue las instrucciones en la [página oficial de Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).
Instalar GitHub CLI (gh):

Sigue las instrucciones en la [página oficial de GitHub CLI](https://cli.github.com/).
Configurar Git:

Configura tu nombre de usuario y correo electrónico:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu-email@example.com"
```

### Hacer el fork, clonar el repo y abrirlo en VSCode

En tu navegador, ve al repositorio original: https://github.com/galiprandi/api-stock.
Haz clic en el botón "Fork" en la esquina superior derecha y selecciona tu cuenta.
Clonar el repositorio:

En tu terminal, clona el repositorio forkeado:
Cambia tu-usuario por tu nombre de usuario de GitHub.
Abrir el proyecto en VSCode:

Navega al directorio del proyecto clonado:
Abre el proyecto en VSCode:

Con estos pasos, habrás completado la configuración inicial y estarás listo para comenzar a trabajar en el proyecto.

## Paso 2: Configuremos nuestro proyecto

Primero, necesitamos inicializar TypeScript en nuestro proyecto. Abre tu terminal y ejecuta el siguiente comando:

```bash
npm install -D typescript # Instalar TypeScript como dependencia de desarrollo
npx tsc --init # Inicializar un archivo de configuración de TypeScript
```

Esto creará un archivo `tsconfig.json` en tu proyecto. A continuación, te muestro un ejemplo de un archivo `tsconfig.json` optimizado para una aplicación Node.js, reemplaza el contenido de tu archivo `tsconfig.json` con el siguiente código, te recomendamos que habras el proyecto en VSCode para hacerlo más fácil:

```json
{
  "compilerOptions": {
    "target": "ES2020",
    "module": "commonjs",
    "strict": true,
    "esModuleInterop": true,
    "skipLibCheck": true,
    "forceConsistentCasingInFileNames": true,
    "outDir": "./dist",
    "rootDir": "./src",
    "resolveJsonModule": true,
    "sourceMap": true
  },
  "include": ["src/**/*.ts"],
  "exclude": ["node_modules"]
}
```

Este archivo de configuración establece varias opciones importantes para un proyecto Node.js, como el objetivo de compilación (target), el sistema de módulos (module), y los directorios de salida y raíz (outDir y rootDir).

Para más detalles sobre las opciones de configuración de TypeScript, te recomiendo leer la [cheat sheet de tsconfig](https://www.totaltypescript.com/tsconfig-cheat-sheet).

### Scripts del package.json

Ahora, vamos a agregar algunos scripts útiles en nuestro archivo `package.json`. Abre el archivo `package.json` y agrega los siguientes scripts en la sección "scripts":

```json
{
  "scripts": {
    "dev": "tsx watch --env-file=.env src/index.ts",
    "build": "tsc",
    "start": "node --env-file=.env dist/index.js"
  }
}
```

- `npm run dev`: Este script utiliza tsx para ejecutar tu aplicación en modo de desarrollo, permitiendo recargas automáticas cuando cambias el código.

- `npm run build`: Este script compila tu código TypeScript en JavaScript, colocando los archivos compilados en el directorio dist.

- `npm run start`: Este script ejecuta la versión compilada de tu aplicación desde el directorio dist.

Con estos scripts, estarás listo para desarrollar, compilar y ejecutar tu aplicación Node.js con TypeScript.

### Instalemos dependencias de desarrollo

Para poder ejecutar nuestra aplicación en modo de desarrollo, necesitamos instalar tsx y @types/node. Ejecuta el siguiente comando en tu terminal:

> 📚 ¿Qué es tsx? tsx es una herramienta que permite ejecutar TypeScript en Node.js con soporte para hot-reloading, lo que significa que la aplicación se reinicia automáticamente cuando se detectan cambios en el código fuente.

> 📚 ¿Cuales son las diferencias entre dependencias de desarrollo y de producción? Las dependencias de desarrollo son aquellas que solo se necesitan durante el proceso de desarrollo, como herramientas de prueba y compiladores. Las dependencias de producción son aquellas que se necesitan para que la aplicación funcione en un entorno de producción, como bibliotecas y frameworks necesarios para la ejecución del código.

```bash
npm install -D tsx @types/node
```

### Gestión de variables de entorno

> 📚 ¿Qué son las variables de entorno? Las variables de entorno son valores dinámicos que pueden afectar el comportamiento de un programa. Se utilizan para configurar la aplicación en diferentes entornos, como desarrollo, pruebas y producción.

Para gestionar las variables de entorno en nuestro proyecto, vamos a crear un archivo `.env` en la raíz de nuestro proyecto. Este archivo contendrá las variables de entorno necesarias para configurar nuestra aplicación.

Crea un archivo `.env` en la raíz de tu proyecto y agrega las siguientes variables de entorno:

```env
PORT=3000
```

Para centrar la gestión de las variables de entorno en un solo lugar, vamos a crear un archivo de configuración `src/config.ts` que cargará las variables de entorno y las exportará para su uso en la aplicación.

Crea un archivo `src/config.ts` y agrega el siguiente código:

```typescript
export const config = {
  ENV: process.env.NODE_ENV || "development",
  PORT: process.env.PORT || 3000,
};
```

### Hello World!

Para verificar que todo está configurado correctamente, vamos a crear un simple "Hello World!" en la consola. Crea un archivo `src/index.ts` con el siguiente contenido:

```typescript
console.log("Hello, World!");
```

Ahora, ejecuta el siguiente comando en tu terminal:

```bash
npm run dev
```

Deberías ver el mensaje "Hello, World!" impreso en la consola. Si ves este mensaje, ¡tu configuración de TypeScript está lista y funcionando! Ahora, puedes avanzar al siguiente paso.

```bash
# Salida esperada
> npx tsx watch --env-file=.env src/index.ts

Hello, World!
```

### Probando el hot-reloading

Para probar el hot-reloading, modifica el mensaje en `src/index.ts` por "Hello, TypeScript!" y guarda el archivo. Deberías ver que el servidor se reinicia automáticamente y muestra el nuevo mensaje en la consola.

> 📚 ¿Qué es hot-reloading? Hot-reloading es una técnica que permite recargar automáticamente la aplicación cuando se detectan cambios en el código fuente. Es una característica muy útil para el desarrollo de aplicaciones, ya que permite ver los cambios en tiempo real sin tener que reiniciar manualmente el servidor.

```bash
# Salida esperada
Hello, TypeScript!
```

¡Excelente! Has configurado correctamente tu proyecto con TypeScript y tsx. Ahora, puedes avanzar al siguiente paso para configurar un servidor Express.

## Paso 3: Configuración del Servidor Express y primer endpoint

En este paso, vamos a instalar Express y CORS, y crearemos un endpoint /api/health-check que devolverá `status: "ready"`.

> 📚 ¿Qué función tiene este endpoint? Este tipo de endpoints son comunes en las aplicaciones web y sirven para verificar si el servidor está en funcionamiento y listo para recibir solicitudes. Proporciona una forma sencilla de comprobar el estado del servidor y la conexión a la base de datos.

### Instalar Dependencias

Ejecuta el siguiente comando en tu terminal para instalar Express y CORS:

```bash
# Instalar Express y CORS
npm install "express@>=5.0.0" cors 
# Instalar tipos de TypeScript para Express y CORS
npm install -D @types/express @types/cors
```

### Configurar el Servidor

Crea el archivo `src/libs/server.ts` y agrega el siguiente código:

```typescript
import cors from "cors";
import express from "express";

const app = express();

// Middleware
app.use(cors());
app.use(express.json());

// Rutas
app.get("/api/health-check", (_req, res) => {
  res.json({ status: "ready", uptime: process.uptime() });
});

// Exportar el servidor para usarlo en index.ts
export { app };
```

> 📚 ¿Qué es un middleware? En Express, un middleware es una función que tiene acceso al objeto de solicitud (req), al objeto de respuesta (res) y a la siguiente función de middleware en el ciclo de solicitud-respuesta. Los middlewares se utilizan para realizar tareas como el registro de solicitudes, la validación de datos, la autenticación de usuarios, etc.

### Inicializar el Servidor

Edita `src/index.ts` para importar e iniciar el servidor:

```typescript
import { config } from "./config";
import { app } from "./libs/server";

const { PORT } = config;

app.listen(PORT, () => {
  console.log(
    `🚀 Server is up and running! Access it at: http://localhost:${PORT}/api/health-check`,
  );
});
```

### Probar el Servidor

Ejecuta el siguiente comando:

```bash
npm run dev
```

Luego, abre tu navegador o usa curl para probar el endpoint:

```bash
curl http://localhost:3000/api/health-check
```

Deberías recibir esta respuesta:

```json
{ "status": "ready", "uptime": 0.123 }
```

> 📚 ¿Qué es curl? curl es una herramienta de línea de comandos que permite transferir datos con URL sintácticas. Es una herramienta muy practica para realizar solicitudes HTTP desde la terminal.

### Criterios de Aceptación del Paso 3

- [ ] Deberás instalar Express y CORS en tu proyecto.
- [ ] Deberás crear un servidor Express en el archivo `src/libs/server.ts`.
- [ ] El servidor deberá tener un endpoint GET `/api/health-check` que devuelva `{ status: 'ready' }`.
- [ ] Deberás inicializar el servidor en el archivo `src/index.ts` y escuchar en el puerto 3000.
- [ ] Deberás probar el servidor y verificar que el endpoint `/api/health-check` responda correctamente.

## 🎉 ¡Felicitaciones!

Has creado tu primer endpoint en Express. Ahora, puedes avanzar al siguiente paso para implementar más funcionalidades en tu API.

## Paso 4: Agregar Pruebas Unitarias

> 📚 ¿Qué son las pruebas unitarias? Las pruebas unitarias son pruebas automatizadas que verifican que una unidad de código (como una función o un módulo) funcione correctamente. Estas pruebas se centran en probar partes específicas del código para garantizar que se comporten como se espera.

En este paso, agregaremos pruebas automatizadas para verificar que el endpoint /api/health-check responde correctamente.

### Instalar Dependencias necesarias

Primero, necesitamos instalar Vitest y Supertest para realizar pruebas automatizadas. Ejecuta el siguiente comando en tu terminal:

```bash
npm install -D vitest supertest @types/supertest
```

### Crear el Archivo de Pruebas

> 💡 Todos los archivos de pruebas unitarias estarán alojados en la carpeta `src/tests/` lo que facilita su organización y mantenimiento.

Crea el archivo `src/tests/health-check.get.test.ts` y agrega el siguiente código:

```typescript
import request from "supertest";
import { describe, expect, it } from "vitest";
import { app } from "../libs/server";

describe("GET /api/health-check", () => {
  it("should return { status: 'ready' }", async () => {
    const response = await request(app).get("/api/health-check");

    expect(response.status).toBe(200);
    expect(response.body).toHaveProperty("status", "ready");
  });
});
```

### Agregar el Script para lanzar las Pruebas

Agrega el siguiente script en la sección "scripts" de tu archivo `package.json`:

```json
{
  "scripts": {
    "test": "vitest"
  }
}
```

### Ejecutar las Pruebas

Ejecuta el siguiente comando en tu terminal para ejecutar las pruebas:

```bash
npm test
```

Deberías ver una salida similar a esta:

```bash
 ✓ src/tests/health-check.get.test.ts (1 test) 28ms
   ✓ GET /api/health-check > should return { status: 'ready' }

 Test Files  1 passed (1)
      Tests  1 passed (1)
   Start at  02:44:18
   Duration  208ms

 PASS  Waiting for file changes...
       press h to show help, press q to quit
```

¡Listo! Ahora tienes pruebas automatizadas para validar que el endpoint /api/health-check funciona correctamente. 🚀

## 🎉 ¡Felicitaciones!

En este punto, has configurado tu proyecto con TypeScript y Express, además haz configurado tu primer endpoint y pruebas automatizadas. ¡Estás en camino de construir una API REST moderna para control de inventario!

Si aún tienes ganas de explorar más en profundidad, puedes visitar los siguientes recursos:

- [Express.js](https://expressjs.com/en/guide/routing.html)
- [Pruebas con Vites](https://vitest.dev/guide)
- [Intercambio de recursos de origen cruzado (CORS)](https://developer.mozilla.org/es/docs/Web/HTTP/CORS)
- [Supertest](https://github.com/ladjs/supertest)
- [API REST](https://es.wikipedia.org/wiki/Transferencia_de_Estado_Representacional)

## Paso 5: Ruta /api/products

En este paso, vamos a implementar una ruta que devuelva una lista mockeada de productos. Esta ruta será accesible a través de /api/products con el método GET y devolverá una lista de productos en formato JSON.

### Crear un Mock de Productos

Crea un archivo `src/data/products.ts` y agrega el siguiente código:

```typescript
export const products = [
  {
    id: 1,
    title: "Laptop",
    brand: "Apple",
    category: "Electronics",
    price: 1299.99,
    stock: 10,
  },
  {
    id: 2,
    title: "Smartphone",
    brand: "Samsung",
    category: "Electronics",
    price: 899.99,
    stock: 20,
  },
  {
    id: 3,
    title: "Tablet",
    brand: "Amazon",
    category: "Electronics",
    price: 299.99,
    stock: 5,
  },
  {
    id: 4,
    title: "Smartwatch",
    brand: "Fitbit",
    category: "Electronics",
    price: 199.99,
    stock: 15,
  },
  {
    id: 5,
    title: "Headphones",
    brand: "Sony",
    category: "Electronics",
    price: 99.99,
    stock: 30,
  },
  {
    id: 6,
    title: "Backpack",
    brand: "North Face",
    category: "Fashion",
    price: 79.99,
    stock: 25,
  },
  {
    id: 7,
    title: "Sneakers",
    brand: "Nike",
    category: "Fashion",
    price: 129.99,
    stock: 40,
  },
  {
    id: 8,
    title: "T-shirt",
    brand: "Adidas",
    category: "Fashion",
    price: 29.99,
    stock: 50,
  },
  {
    id: 9,
    title: "Jeans",
    brand: "Levi's",
    category: "Fashion",
    price: 59.99,
    stock: 20,
  },
  {
    id: 10,
    title: "Sunglasses",
    brand: "Ray-Ban",
    category: "Fashion",
    price: 149.99,
    stock: 10,
  },
];
```

> 📚 ¿Qué es un mock de datos? Un mock de datos es un conjunto de datos falsos o simulados que se utilizan para pruebas o desarrollo. En este caso, hemos creado un mock de productos que se utilizará para simular una base de datos de productos hasta que implementemos la integración con Prisma y PostgreSQL.

### Crear la Ruta /api/products

En este punto es importante que separemos las rutas en archivos diferentes para mantener nuestro código organizado y fácil de mantener. Crea un archivo `src/routes/products.ts` y agrega el siguiente código:

```typescript
import { Router } from "express";
import { products } from "../data/products";

const router = Router();

router.get("/", (_req, res) => {
  res.json(products);
});

export { router as productsRouter };
```

### Agregar la Ruta en el Servidor

Importa y usa la ruta `/api/products` en tu servidor. Edita el archivo `src/libs/server.ts` para agregar la ruta de productos:

```typescript
import cors from "cors";
import express from "express";
import { productsRouter } from "../routes/products";

const app = express();

// Middleware
app.use(cors());
app.use(express.json());

// Rutas
app.get("/api/health-check", (_req, res) => {
  res.json({ status: "ready", uptime: process.uptime() });
});

app.use("/api/products", productsRouter);

// Exportar el servidor para usarlo en index.ts
export { app };
```

### Probar la Ruta /api/products

Ejecuta tu servidor con `npm run dev` y luego abre tu navegador o usa curl para probar la ruta `/api/products`:

```bash
curl http://localhost:3000/api/products
```

Deberías recibir una respuesta con la lista de productos en formato JSON.

### Pruebas Automatizadas para /api/products

Agrega pruebas automatizadas para la ruta `/api/products`. Crea un archivo `src/tests/products.get.test.ts` y agrega el siguiente código:

```typescript
import request from "supertest";
import { describe, expect, it } from "vitest";
import { products } from "../data/products";
import { app } from "../libs/server";

// ⚠️ Introducimos un error intencional en la prueba
describe("GET /api/products", () => {
  it("should return a list of products", async () => {
    const response = await request(app).get("/api/products");

    expect(response.status).toBe(200);
    expect(response.body).not.toEqual(products);
  });
});
```

> 📚 ¿Qué es TDD? El Desarrollo Guiado por Pruebas (TDD) es una metodología de desarrollo de software en la que las pruebas se escriben antes del código de producción. El ciclo de TDD generalmente sigue estos pasos:
>
> 1. **Escribir una prueba que falle:** Crear una prueba automatizada para una nueva funcionalidad que aún no está implementada.
> 2. **Escribir el código mínimo para pasar la prueba:** Implementar el código necesario para que la prueba pase.
> 3. **Refactorizar el código:** Mejorar el código asegurándose de que todas las pruebas sigan pasando.
>
> En este caso, hemos introducido un error intencional en la prueba para que falle. El siguiente paso es corregir el código para que la prueba pase.

### ⚠️ Recuerda corregir la Prueba

Corrige la prueba en `src/tests/products.get.test.ts` para que pase correctamente. Lee atentamente el código de la prueba, ejecuta las pruebas y asegúrate de que pasen correctamente.

## 🎉 ¡Felicitaciones!

Haz avanzado mucho y ya tiene la estructura básica de tu API REST y los conocimientos necesarios para agregar nuevas rutas y funcionalidades. A partir de ahora las intrucciones serán menos precisas y tendrás que investigar y probar por tu cuenta. Las proximas tareas serán más parecidas a requeriemientos de un cliente y tendrás que implementarlos por tu cuenta, pero siempre especificaremos los criterios de aceptación que deberás cumplir.

> 💡 Recuerda apoyarte en las sugerencias de GitHub Copilot a partir de ahora, será tu compañero y te facilitará el aprendizaje y las tareas repetitivas. Para más información, consulta la [documentación oficial de GitHub Copilot](https://docs.github.com/en/copilot/quickstart?tool=visualstudio).

## Paso 6: Implementar un Endpoint para Crear Productos

En este paso, vamos a implementar un endpoint POST /api/products que permita crear un nuevo producto. El endpoint recibirá los datos del producto en el cuerpo de la solicitud y devolverá el producto creado con un ID único.

Los pasos a seguir son los siguientes:

1. Crear la ruta POST /api/products en el archivo `src/routes/products.ts`.
2. Recuperar del body de la solicitud los datos del producto a crear.
3. Generar un ID único para el nuevo producto. Por ahora puedes usar la longitud del array + 1 como ID.
4. Agregar el nuevo producto al array de productos usando el método push.
5. Devolver el producto creado con el código de estado 201 (Created).
6. Verifica que el GET /api/products devuelva las lista de productos con el nuevo producto creado.
7. Agregar pruebas automatizadas para el endpoint POST /api/products.

Comencemos creando primero las pruebas unitarias, crea el archivo `src/tests/products.post.test.ts` y agrega el siguiente código:

```typescript
import request from "supertest";
import { describe, expect, it } from "vitest";
import { app } from "../libs/server";

describe("POST /api/products", () => {
  it("should create a new product", async () => {
    const newProduct = {
      title: "Smart Speaker",
      brand: "Google",
      category: "Electronics",
      price: 99.99,
      stock: 15,
    };

    const response = await request(app)
      .post("/api/products")
      .send(newProduct);

    expect(response.status).toBe(201);
    expect(response.body).toMatchObject(newProduct);
  });
});
```

Una vez que hayan implementado el endpoint POST /api/products y las pruebas unitarias unitarias pasen correctamente, prueba manualmente crea un nuevo producto usando el siguiente curl:

```bash
# Curl para crear un nuevo producto
curl -X POST http://localhost:3000/api/products -H "Content-Type: application/json" -d '{"title": "Smart Speaker", "brand": "Google", "category": "Electronics", "price": 99.99, "stock": 15}'
```

### Criterios de Aceptación del Paso 6

- [ ] Deberás implementar el endpoint POST /api/products en el archivo src/routes/products.ts.
- [ ] El endpoint deberá recibir los datos del producto a crear en el cuerpo de la solicitud.
- [ ] El endpoint deberá devolver el producto creado con un ID único y el código de estado 201 (Created).
- [ ] El producto creado deberá ser agregado al array de productos.
- [ ] El endpoint GET /api/products deberá devolver la lista de productos con el nuevo producto creado.
- [ ] Deberás agregar pruebas automatizadas para el endpoint POST /api/products.

## Paso 7: Implementar un Endpoint para Actualizar Productos

> 📚 ¿Qué significa CRUD? CRUD es un acrónimo que significa Crear, Leer, Actualizar y Eliminar. Se utiliza para describir las cuatro operaciones básicas que se pueden realizar en una base de datos o en una API REST.

En este paso, vamos a implementar un endpoint PUT /api/products/:id que permita actualizar un producto existente. El endpoint recibirá el ID del producto a actualizar en la URL y los nuevos datos del producto en el cuerpo de la solicitud.

Los pasos a seguir son los siguientes:

1. Crear la ruta PUT /api/products/:id en el archivo `src/routes/products.ts`.
2. Recuperar el ID del producto a actualizar de los parámetros de la URL.
3. Recuperar los nuevos datos del producto del cuerpo de la solicitud.
4. Buscar el producto con el ID proporcionado en el array de productos.
5. Actualizar los datos del producto con los nuevos datos proporcionados.
6. Devolver el producto actualizado con el código de estado 200 (OK).
7. Verificar que el GET /api/products devuelva las lista de productos con el producto actualizado.
8. Agregar pruebas automatizadas para el endpoint PUT /api/products/:id.

Comencemos creando primero las pruebas unitarias, crea el archivo `src/tests/products.put.test.ts` y agrega el siguiente código:

```typescript
import request from "supertest";
import { describe, expect, it } from "vitest";
import { products } from "../data/products";
import { app } from "../libs/server";

describe("PUT /api/products/:id", () => {
  it("should update an existing product", async () => {
    const productId = 1;
    const updatedProduct = {
      title: "Updated Laptop",
      brand: "Apple",
      category: "Electronics",
      price: 1499.99,
      stock: 5,
    };

    const response = await request(app)
      .put(`/api/products/${productId}`)
      .send(updatedProduct);

    expect(response.status).toBe(200);
    expect(response.body).toMatchObject(updatedProduct);
  });
});
```

Una vez que hayan implementado el endpoint PUT /api/products/:id y las pruebas unitarias unitarias pasen correctamente, prueba manualmente actualizando un producto usando el siguiente curl:

```bash
# Curl para actualizar un producto
curl -X PUT http://localhost:3000/api/products/1 -H "Content-Type: application/json" -d '{"title": "Updated Laptop", "brand": "Apple", "category": "Electronics", "price": 1499.99, "stock": 5}'
```

### Criterios de Aceptación del Paso 7

- [ ] Deberás implementar el endpoint PUT /api/products/:id en el archivo src/routes/products.ts.
- [ ] El endpoint deberá recibir el ID del producto a actualizar en los parámetros de la URL.
- [ ] El endpoint deberá recibir los nuevos datos del producto en el cuerpo de la solicitud.
- [ ] El producto actualizado deberá ser devuelto con el código de estado 200 (OK).
- [ ] Deberás agregar pruebas automatizadas para el endpoint PUT /api/products/:id.

## Paso 8: Implementar un Endpoint para Eliminar Productos

En este paso, vamos a implementar un endpoint DELETE /api/products/:id que permita eliminar un producto existente. El endpoint recibirá el ID del producto a eliminar en la URL.

Los pasos a seguir son los siguientes:

1. Crear la ruta DELETE /api/products/:id en el archivo `src/routes/products.ts`.
2. Recuperar el ID del producto a eliminar de los parámetros de la URL.
3. Buscar el producto con el ID proporcionado en el array de productos.
4. Eliminar el producto del array de productos.
5. Devolver el producto eliminado con el código de estado 200 (OK).
6. Verificar que el GET /api/products devuelva las lista de productos sin el producto eliminado.
7. Agregar pruebas automatizadas para el endpoint DELETE /api/products/:id.

Comencemos creando primero las pruebas unitarias, crea el archivo `src/tests/products.delete.test.ts` y agrega el siguiente código:

```typescript
import request from "supertest";
import { describe, expect, it } from "vitest";
import { products } from "../data/products";
import { app } from "../libs/server";

describe("DELETE /api/products/:id", () => {
  it("should delete an existing product", async () => {
    const productId = 1;
    const response = await request(app).delete(`/api/products/${productId}`);

    expect(response.status).toBe(200);
    expect(products.some(product => product.id === productId)).toBe(false);
  });
});
```

Una vez que hayan implementado el endpoint DELETE /api/products/:id y las pruebas unitarias unitarias pasen correctamente, prueba manualmente eliminando un producto usando el siguiente curl:

```bash
# Curl para eliminar un producto
curl -X DELETE http://localhost:3000/api/products/1
```

### Criterios de Aceptación del Paso 8

- [ ] Deberás implementar el endpoint DELETE /api/products/:id en el archivo src/routes/products.ts.
- [ ] El endpoint deberá recibir el ID del producto a eliminar en los parámetros de la URL.
- [ ] El producto eliminado deberá ser devuelto con el código de estado 200 (OK).
- [ ] El producto eliminado deberá ser removido del array de productos.
- [ ] Deberás agregar pruebas automatizadas para el endpoint DELETE /api/products/:id.

## Paso 9: Introducción a la Observabilidad y Configuración de Herramientas

> 📚 ¿Qué es la observabilidad? La observabilidad es la capacidad de comprender y depurar un sistema complejo a través de la recopilación y análisis de datos. En el contexto de las aplicaciones web, la observabilidad se refiere a la capacidad de monitorear y analizar el comportamiento de la aplicación en tiempo real.

En este paso, vamos a introducir los conceptos básicos de observabilidad y configurar herramientas para el monitoreo y logging de nuestra API. La observabilidad es crucial para entender el comportamiento de nuestra aplicación en producción y detectar problemas antes de que afecten a los usuarios.

### Instalación de Pino Logger

[Pino](https://getpino.io) es una biblioteca de logging rápida y eficiente para Node.js. Vamos a instalar y configurar Pino para registrar eventos y errores en nuestra API.

Ejecuta el siguiente comando en tu terminal para instalar Pino:

```bash
npm install pino pino-pretty pino-http
```

### Configuración de Pino Logger

Crea un archivo `src/libs/logger.ts` para configurar Pino y exportar un logger personalizado:

```typescript
import pino from "pino";
import { config } from "../config";

const { ENV } = config;

export const logger = pino({
  transport: {
    target: "pino-pretty",
    options: {
      colorize: true,
    },
  },
  level: ENV === "production" ? "info" : "debug",
});
```

Luego, integra Pino en tu servidor Express. Edita el archivo `src/libs/server.ts` para importar y usar Pino como un nuevo middleware de Express, recuerda importar el `logger` que acabas de crear:

```typescript
import pinoHttp from "pino-http";
import { logger } from "./logger";

// Middleware
app.use(pinoHttp({ logger }));
```

Tambien podemos usar Pino para registar el evento que indica que el servidor está corriendo, para ello edita el archivo `src/index.ts` y modifica el mensaje de inicio del servidor por el siguiente:

```typescript
logger.info(
  `🚀 Server is up and running! Access it at: http://localhost:${PORT}/api/health-check`,
);
```

> 📚 ¿Cuál es la diferencia entre pino y pino-http?
>
> - `pino` es un logger rápido para registrar eventos generales en la aplicación.
> - `pino-http` es un middleware de Express que captura automáticamente las solicitudes HTTP y las registra en el log.
>
> Usamos pino-http({ logger }) en server.ts para que todas las peticiones queden registradas automáticamente.

Luego de instalar y configurar Pino, ejecuta tu servidor con `npm run dev` y verifica que los eventos y errores se registren correctamente en la consola.

```bash
# Salida esperada
> tsx watch --env-file=.env src/index.ts

[01:41:32.832] INFO (160460): 🚀 Server is up and running! Access it at: http://localhost:3000/api/health-check
```

### Criterios de Aceptación del Paso 9

- [ ] Deberás instalar la librería `pino` para el logging y configurarla en tu proyecto.
- [ ] Deberás crear un archivo `src/libs/logger.ts` para configurar Pino y exportar un logger personalizado.
- [ ] Deberás integrar Pino en tu servidor Express como un middleware.
- [ ] Deberás crear un archivo `src/libs/datadog.ts` para configurar Datadog y exportar el agente.
- [ ] Deberás verificar que el logging y la integración con Datadog funcionen correctamente en tu aplicación.

## 🎉 ¡Felicitaciones!

Has hecho avances muy impresionantes en tu proyecto, y mejorado la infraestructura de tu API con herramientas de observabilidad y monitoreo que son claves para escalar y mantener aplicaciones en producción. ¡Sigue así!

## Paso 10: Le pongamos estilo a nuestro código con Biome

En este paso, vamos a asegurarnos que el código de nuestra API siga las mejores prácticas y estándares de codificación. Para ello, vamos a utilizar Biome, su extensión para vscode y definiremos un estilo de código minimalista.

### Instalar la extensión de Biome para Visual Studio Code

La extensión de Biome para Visual Studio Code proporciona una integración perfecta con la herramienta de análisis de código estático. Vamos a instalar la extensión para mejorar la experiencia de desarrollo.

Abre Visual Studio Code y busca la extensión "Biome" en el Marketplace. Haz clic en "Install" para instalar la extensión.

### Instalación de Biome

Biome es una herramienta de análisis de código estático que ayuda a mantener un código limpio y consistente. Vamos a instalar Biome y su extensión para Visual Studio Code.

Ejecuta el siguiente comando en tu terminal para instalar Biome:

```bash
npm install -D @biomejs/biome
npx @biomejs/biome init
```

### Configuración de Biome

Crea un archivo `biome.json` en la raíz de tu proyecto y agrega la siguiente configuración:

```json
{
  "$schema": "https://biomejs.dev/schemas/1.9.4/schema.json",
  "vcs": {
    "enabled": false,
    "clientKind": "git",
    "useIgnoreFile": false
  },
  "files": {
    "ignoreUnknown": false,
    "ignore": []
  },
  "formatter": {
    "enabled": true,
    "indentStyle": "tab"
  },
  "organizeImports": {
    "enabled": true
  },
  "linter": {
    "enabled": true,
    "rules": {
      "correctness": {
        "noUnusedImports": "warn",
        "noUnusedVariables": "warn",
        "noUnusedFunctionParameters": "warn"
      },
      "recommended": true
    }
  },
  "javascript": {
    "formatter": {
      "quoteStyle": "single",
      "semicolons": "asNeeded"
    }
  }
}
```

### Script que corrige automáticamente los errores de estilo

Agrega el siguiente script en la sección "scripts" de tu archivo `package.json`:

```json
{
  "scripts": {
    "check": "biome check --write ."
  }
}
```

### Configuración de Visual Studio Code

Abre las configuraciones de Visual Studio Code presionando `Shift + Ctrl + P` y selecciona "Preferences: Open Settings (JSON)". Agrega la siguiente configuración para que Biome chequeé automáticamente tu código al guardar:

```json
{
  "editor.formatOnSave": true,
  "[javascript]": {
    "editor.defaultFormatter": "biomejs.biome"
  },
  "[typescript]": {
    "editor.defaultFormatter": "biomejs.biome"
  },
  "[json]": {
    "editor.defaultFormatter": "biomejs.biome"
  },
  "[jsonc]": {
    "editor.defaultFormatter": "vscode.json-language-features"
  }
}
```

### Criterios de Aceptación del Paso 10

- [ ] Deberás instalar la extensión de Biome para Visual Studio Code.
- [ ] Deberás instalar Biome y configurarlo en tu proyecto.
- [ ] Deberás agregar un script en el archivo `package.json` para corregir automáticamente los errores de estilo.
- [ ] Deberás configurar Visual Studio Code para que Biome chequeé automáticamente tu código al guardar.
- [ ] Deberás verificar que Biome funcione correctamente y corrija los errores de estilo en tu código.

## 🎉 ¡Felicitaciones!

Has mejorado la calidad y consistencia de tu código con Biome, una herramienta de análisis de código estático que te ayudará a mantener un código limpio y consistente. ¡Sigue así!

## Paso 11: Refactorización del CRUD con Servicios y Controladores

En este paso, vamos a refactorizar el código de nuestra API para seguir una arquitectura más escalable y mantenible. Vamos a separar la lógica de negocio en servicios y controladores para mejorar la organización y reutilización del código. Además vamos a implementar una arquitectura en capas (Layered Architecture) que es más escalable y mantenible.

### Creemos la estructura de carpetas

Organizaremos los servicios y controladores en módulos dentro del directorio `src/api`. Cada módulo representará un recurso de la aplicación, como products y users.

```bash
src/
│── api/
│   ├── health-check/
│   │   ├── controllers/
│   │   ├── services/
│   │   ├── health-check.route.ts
│   ├── products/
│   │   ├── controllers/
│   │   ├── services/
│   │   ├── products.routes.ts
│   ├── users/ # Ejemplo de un módulo de usuarios
│   │   ├── controllers/
│   │   ├── services/
│   │   ├── users.route.ts
│   ├── orders/ # Ejemplo de un módulo de órdenes
│   │   ├── controllers/
│   │   ├── services/
│   │   ├── orders.route.ts
│   ├── ... # Otros módulos
```

> 📚 Separación en módulos: La separación en módulos es una técnica de diseño de software que consiste en dividir una aplicación en partes más pequeñas y manejables. Cada módulo se enfoca en una tarea específica y se comunica con otros módulos a través de interfaces bien definidas.

### Creemos nuestro primer Servicio

Crea un archivo `src/api/products/services/products.get.all.service.ts` y agrega el siguiente código:

```typescript
import { products } from "../../../data/products";

export const getAllProductsService = () => {
  return products;
};
```

### Creemos el primer Controlador

Crea un archivo `src/api/products/controllers/products.get.all.controller.ts` y agrega el siguiente código:

```typescript
import type { Request, Response } from "express";
import { getAllProductsService } from "../services/products.get.all.service";

export const getAllProductsController = (_req: Request, res: Response) => {
  const allProducts = getAllProductsService();
  res.json(allProducts);
};
```

### Creemos la Ruta para los Productos

Crea un archivo `src/api/products/products.routes.ts` y agrega el siguiente código:

```typescript
import { Router } from 'express'
import { getAllProductsController } from './controllers/products.get.all.controller'

export const productsRoutes = Router()

productsRoutes.get('/', getAllProductsController)
```

### Integremos la Ruta en el Servidor

Edita el archivo `src/libs/server.ts` para importar y usar la ruta de productos y eliminar las rutas antiguas:

```typescript
import cors from 'cors'
import express from 'express'
import pinoHttp from 'pino-http'
import { logger } from './logger'
import { productsRoutes } from '../api/products/products.routes'
import { healthCheckRoutes } from '../api/health-check/health-check.routes'

const app = express()

// Middleware
app.use(cors())
app.use(express.json())
app.use(pinoHttp({ logger }))

// Routes
app.use('/api/health-check', healthCheckRoutes)
app.use('/api/products', productsRoutes)

// Exportar el servidor para usarlo en index.ts
export { app }

```

### Refactoriza el resto de las rutas

Mueve la lógica de negocio del archivo `src/routes/products.ts` a los servicios y controladores correspondientes en el directorio `src/api/products`. Repite el proceso para las rutas de creación, actualización y eliminación de productos.

La estructura de carpetas y archivos debería verse así:

```bash
src/
│── api/
│   ├──   /
│   │   ├── controllers/
│   │   │   ├── health-check.get.controller.ts
│   │   ├── services/
│   │   │   ├── health-check.get.service.ts
│   │   ├── health-check.routes.ts
│   ├── products/
│   │   ├── controllers/
│   │   │   ├── products.create.controller.ts
│   │   │   ├── products.get.all.controller.ts
│   │   │   ├── products.update.controller.ts
│   │   │   ├── products.delete.controller.ts
│   │   ├── services/
│   │   │   ├── products.create.service.ts
│   │   │   ├── products.get.all.service.ts
│   │   │   ├── products.update.service.ts
│   │   │   ├── products.delete.service.ts
│   │   ├── products.routes.ts
```

Ya puedes eliminar el archivo `src/routes/products.ts` y su importación en `src/libs/server.ts`.
Luego ejecuta los tests para verificar que todo sigue funcionando correctamente, y has los ajustes necesarios en caso de que algo falle.

### Criterios de Aceptación del Paso 11

- [ ] Deberás crear una estructura de carpetas y archivos para los servicios y controladores de la API.
- [ ] Deberás crear servicios y controladores para las operaciones CRUD de los productos.
- [ ] Deberás mover la lógica de negocio de las rutas a los servicios y controladores correspondientes.
- [ ] Deberás integrar las rutas de productos en el servidor Express y eliminar las rutas antiguas.
- [ ] Deberás verificar que las rutas de productos funcionen correctamente después de la refactorización.

## 🎉 ¡Felicitaciones!

Has refactorizado tu API para seguir una arquitectura más escalable y mantenible, utilizando servicios y controladores para separar la lógica de negocio de las rutas. ¡Sigue así!
