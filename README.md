# 📦 API Stock – Curso de Backend en TypeScript

Este es un curso práctico y progresivo diseñado para personas con conocimientos básicos de JavaScript y TypeScript que quieren aprender a construir un backend moderno con tecnologías actuales. A diferencia de otros cursos, aquí trabajarás en un proyecto real desde el primer día, evolucionando tu propio repositorio en GitHub a medida que avanzas.

## 🎯 Objetivo del Curso

El objetivo es que, al finalizar, tengas una API funcional y escalable en tu GitHub, construida con buenas prácticas y herramientas profesionales. Aprenderás desde los fundamentos hasta técnicas avanzadas, ganando experiencia en un entorno similar al de un equipo de desarrollo real.

Este curso no solo te enseña a programar, sino que también te prepara para enfrentar desafíos comunes en el desarrollo backend, con un enfoque en depuración, pruebas automatizadas y uso de herramientas modernas.

## 👤 ¿A quién va dirigido?

- Personas que ya hicieron cursos introductorios de JavaScript/TypeScript y quieren dar el siguiente paso en backend.
- Desarrolladores que buscan experiencia práctica con un proyecto real.
- Estudiantes o autodidactas que quieran fortalecer su portafolio en GitHub.
- Quienes quieran aprender herramientas modernas como Prisma, GitHub Copilot y Zod aplicadas a un backend real.

No es un curso para **absolutos principiantes** en programación. Se asume que entendés los fundamentos de JavaScript y TypeScript, pero no necesitás experiencia profesional en backend.

## 🛠️ Tecnologías y herramientas

Durante el curso, trabajarás con un stack moderno que simula lo que se usa en la industria:\

✅ **TypeScript**: Código tipado para mayor seguridad y escalabilidad.\
✅ **Express v5**: Framework rápido y flexible para APIs REST.\
✅ **Prisma ORM**: Interfaz moderna para bases de datos SQL.\
✅ **PostgreSQL**: Base de datos robusta y estándar en la industria.\
✅ **Vitest + Supertest**: Pruebas automatizadas con TDD.\
✅ **Zod** – Validaciones de datos seguras y declarativas.\
✅ **GitHub Copilot + ChatGPT**: Aprendizaje asistido con IA.\
✅ **GitHub Actions**: _(opcional)_ Automatización de pruebas y despliegue.\
✅ **Docker + Railway**: _(opcional)_ Entornos de desarrollo y producción reales.

## 🚀 ¿Qué aprenderás?

✔️ Configurar un backend profesional desde cero.\
✔️ Crear endpoints REST con buenas prácticas.\
✔️ Manejar errores y validaciones avanzadas.\
✔️ Conectar y gestionar bases de datos SQL con Prisma.\
✔️ Aplicar TDD con pruebas automatizadas.\
✔️ Implementar autenticación y autorización con JWT.\
✔️ Estructurar código de forma escalable con una arquitectura en capas.\
✔️ Optimizar la API con paginación, filtros y consultas eficientes.\
✔️ Desplegar la API en producción _(opcional, con pasos extra)_.

## 📌 Metodología y progresión

Este curso tiene un enfoque práctico y progresivo:

1. **Inicio guiado** – Al principio, cada paso está detallado línea por línea.
2. **Menos guía, más autonomía** – Luego, se dan requisitos y tests, dejando que el estudiante implemente.
3. **Uso de herramientas como GitHub Copilot** – Para fomentar la resolución de problemas de forma autónoma.
4. **Validación con pruebas** – Todo el código debe pasar tests para considerarse correcto.
5. **Pasos opcionales** – Funcionalidades extra para quienes quieran profundizar más.

## 🌍 Comunidad y soporte

El curso fomenta el aprendizaje colaborativo dentro de GitHub, usando:

📌 **GitHub Discussions** – Espacio para dudas y debates.\
📌 **Issues** – Para reportar errores o sugerir mejoras.\
📌 **Pull Requests** – Para desafíos opcionales y contribuciones.

## 💡 ¿Por qué este curso?

A diferencia de otros cursos en español que se quedan en teoría o ejemplos básicos, este curso:

✅ Te da un proyecto real que podés mostrar en GitHub.\
✅ Usa herramientas actuales y prácticas reales de la industria.\
✅ Te entrena en depuración y pruebas automatizadas.\
✅ No te deja todo servido: progresivamente te hace pensar y resolver problemas.

Si querés aprender backend de verdad, no solo copiar código, este curso es para vos. 🚀

## 🤝 Contribuciones

Si querés mejorar este curso, podés contribuir de varias formas:

- Reportando errores o mejoras en la sección de Issues.
- Proponiendo cambios mediante Pull Requests.
- Compartiendo el curso con otros desarrolladores.

Todas las sugerencias y mejoras son bienvenidas. 🚀

## 👤 Autor

Este curso fue creado por [Germán Aliprandi](https://www.linkedin.com/in/galiprandi). Si tenés preguntas o sugerencias, no dudes en contactarme o abrir una discusión en GitHub.

## 📜 Licencia

Este proyecto está bajo la Licencia MIT, lo que significa que podés usar, modificar y distribuir el código con total libertad, siempre que incluyas la licencia original.

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

> 📚 Para más detalles sobre las opciones de configuración de TypeScript, te recomiendo leer la [cheat sheet de tsconfig](https://www.totaltypescript.com/tsconfig-cheat-sheet).

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

Antes de crear el archivo `.env` que contrendrá información sensible, debemos crear un archivo `.gitignore` en la raíz de tu proyecto y agregues las siguientes líneas:

```env
.env
node_modules
dist
```

⚠️ IMPORTANTE: Esto evitará que el archivo .env, con las variables de entorno sensibles, se suba al repositorio.

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

### 🎉 ¡Felicitaciones!

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

### 🎉 ¡Felicitaciones!

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

### 🎉 ¡Felicitaciones!

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
import { products } from "../data/products";
import { app } from "../libs/server";

describe("POST /api/products", () => {
  it("should create a new product", async () => {
    const totlasProducts = products.length;
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
    expect(response.body.id).toBe(totlasProducts + 1);
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

  it("should return 404 if product not found", async () => {
    const productId = "invalid-id";
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

    expect(response.status).toBe(404);
    expect(response.body).toMatchObject({ message: "Product not found" });
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
    expect(response.body).toMatchObject({ message: "Product deleted" });
    expect(products.some(product => product.id === productId)).toBe(false);
  });

  it("should return 404 if product not found", async () => {
    const productId = "invalid-id";
    const response = await request(app).delete(`/api/products/${productId}`);

    expect(response.status).toBe(404);
    expect(response.body).toMatchObject({ message: "Product not found" });
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

### 🎉 ¡Felicitaciones!

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

Reemplaza el contenido de archivo `biome.json` recientemente creado en la raíz de tu proyecto con el siguiente contenido:

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

Abre las configuraciones de Visual Studio Code presionando `Shift + Ctrl + P` y selecciona "Preferences: Open User Settings (JSON)". Agrega la siguiente configuración para que Biome chequeé automáticamente tu código al guardar:

```json
{
  // Mantén el resto de configuraciones
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

### Da formato a tu código con Biome

Ejecuta el siguiente comando en tu terminal para dar formato a tu código con Biome:

```bash
npm run check
```

Esto formateará automáticamente TODO tu código según las reglas definidas en el archivo `biome.json` por lo que verás muchos cambios en tus archivos. Si ingresas a ver esos cambios verás que Biome ha corregido automáticamente los errores de estilo en tu código uniformando el estilo de todo tu proyecto.

💡 Este es un buen momento para hacer un commit con todo tu código formateado. Antes de hacerlo, asegúrate de que tu servidor funcione correctamente y que todas las pruebas unitarias se ejecuten sin errores.

### Criterios de Aceptación del Paso 10

- [ ] Deberás instalar la extensión de Biome para Visual Studio Code.
- [ ] Deberás instalar Biome y configurarlo en tu proyecto.
- [ ] Deberás agregar un script en el archivo `package.json` para corregir automáticamente los errores de estilo.
- [ ] Deberás configurar Visual Studio Code para que Biome chequeé automáticamente tu código al guardar.
- [ ] Deberás verificar que Biome funcione correctamente y corrija los errores de estilo en tu código.
- [ ] Deberás chequear tu código con Biome y corregir los errores de estilo.
- [ ] Deberas verificar que las pruebas unitarias sigan pasando después de dar formato a tu código.

### 🎉 ¡Felicitaciones!

Has mejorado la calidad y consistencia de tu código con Biome, una herramienta de análisis de código estático que te ayudará a mantener un código limpio y consistente. ¡Sigue así!

## Paso 11: Refactorización del CRUD con Servicios y Controladores

En este paso, vamos a refactorizar el código de nuestra API para seguir una arquitectura más escalable y mantenible. Vamos a separar la lógica de negocio en servicios y controladores para mejorar la organización y reutilización del código. Además vamos a implementar una arquitectura en capas (Layered Architecture) que es más escalable y mantenible.

### Agreguemos los typos necesarios

Antes de continuar con la refactorización, necesitamos agregar los tipos necesarios para TypeScript. Crea un archivo `src/api/products/products.interfaces.ts` y agrega el siguiente código:

```typescript
// Interface para el objeto Producto
export type ProductDTO = {
  id: number;
  title: string;
  brand: string;
  category: string;
  price: number;
  stock: number;
}

// Interface para crear un nuevo producto
export type CreateProductDTO = Omit<ProductDTO, "id">;

// Interface para actualizar un producto existente
export type UpdateProductDTO = Partial<ProductDTO>;
```

Estas interfaces nos ayudarán a definir la forma de los objetos de producto, así como los datos necesarios para crear y actualizar un producto.

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
import { Router } from "express";
import { getAllProductsController } from "./controllers/products.get.all.controller";

export const productsRoutes = Router();

productsRoutes.get("/", getAllProductsController);
```

### Integremos la Ruta en el Servidor

Edita el archivo `src/libs/server.ts` para importar y usar la ruta de productos y eliminar las rutas antiguas:

```typescript
import cors from "cors";
import express from "express";
import pinoHttp from "pino-http";
import { healthCheckRoutes } from "../api/health-check/health-check.routes";
import { productsRoutes } from "../api/products/products.routes";
import { logger } from "./logger";

const app = express();

// Middleware
app.use(cors());
app.use(express.json());
app.use(pinoHttp({ logger }));

// Rutas
app.use("/api/health-check", healthCheckRoutes);
app.use("/api/products", productsRoutes);

// Exportar el servidor para usarlo en index.ts
export { app };
```

### Refactorizamos la ruta de creación de productos

Crea un archivo `src/api/products/services/products.create.service.ts` y agrega el siguiente código:

```typescript
import { products } from "../../../data/products";
import { CreateProductDTO } from "../products.interfaces";

export const createProductService = (newProduct: CreateProductDTO) => {
  const id = products.length + 1;
  const product = { id, ...newProduct };
  products.push(product);
  return product;
};
```

Crea un archivo `src/api/products/controllers/products.create.controller.ts` y agrega el siguiente código:

```typescript
import type { Request, Response } from "express";
import { createProductService } from "../services/products.create.service";

export const createProductController = (req: Request, res: Response) => {
  const newProduct = req.body;
  const product = createProductService(newProduct);
  res.status(201).json(product);
};
```

Modifica el archivo `src/api/products/products.routes.ts` y agrega el siguiente código:

```typescript
import { Router } from "express";
import { createProductController } from "./controllers/products.create.controller";
import { getAllProductsController } from "./controllers/products.get.all.controller";

export const productsRoutes = Router();

productsRoutes.get("/", getAllProductsController);
productsRoutes.post("/", createProductController);
```

### Tu guía de desarrollo deben ser la pruebas unitarias

Si ejecutas las pruebas unitarias ahora, es posible que algunas fallen debido a la refactorización. Asegúrate de refactorizar las rutas PUT y DELETE siguiendo el mismo proceso hasta que las pruebas pasen correctamente.

```bash
  RERUN  rerun all tests 

 ✓ src/tests/products.get.test.ts (1 test) 39ms
   ✓ GET /api/products > should return a list of products
 ❯ src/tests/products.delete.test.ts (2 tests | 2 failed) 66ms
   × DELETE /api/products/:id > should delete an existing product 49ms
     → expected 404 to be 200 // Object.is equality
   × DELETE /api/products/:id > should return 404 if product not found 16ms
     → expected {} to match object { message: 'Product not found' }
 ✓ src/tests/health-check.get.test.ts (1 test) 39ms
   ✓ GET /api/health-check > should return { status: 'ready' }
 ❯ src/tests/products.put.test.ts (2 tests | 2 failed) 78ms
   × PUT /api/products/:id > should update an existing product 64ms
     → expected 404 to be 200 // Object.is equality
   × PUT /api/products/:id > should return 404 if product not found 13ms
     → expected {} to match object { message: 'Product not found' }
 ✓ src/tests/products.post.test.ts (1 test) 42ms
   ✓ POST /api/products > should create a new product
```

### Refactoriza el resto de las rutas

Mueve la lógica de negocio del archivo `src/routes/products.ts` a los servicios y controladores correspondientes en el directorio `src/api/products`. Repite el proceso para las rutas de creación, actualización y eliminación de productos.

💡 Usa GitHub Copilot o ChatGPT para obtener sugerencias y asistencia mientras desarrollas tu API. Estas herramientas pueden ayudarte a escribir código más rápido y a resolver problemas comunes de programación.

⚠️ Recuerda que por cada ruta deberás crear un servicio y un controlador correspondiente, además de crear la ruta en el archivo `src/api/products/products.routes.ts` y verificar que el test unitario correspondiente pase correctamente.

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
│   │   │   ├── products.get.all.controller.ts
│   │   │   ├── products.create.controller.ts
│   │   │   ├── products.update.controller.ts
│   │   │   ├── products.delete.controller.ts
│   │   ├── services/
│   │   │   ├── products.get.all.service.ts
│   │   │   ├── products.create.service.ts
│   │   │   ├── products.update.service.ts
│   │   │   ├── products.delete.service.ts
│   │   ├── products.routes.ts
```

⚠️ Ya puedes eliminar el archivo `src/routes/products.ts`.
Luego ejecuta los tests para verificar que todo sigue funcionando correctamente, y has los ajustes necesarios en caso de que algo falle.

### Criterios de Aceptación del Paso 11

- [ ] Deberás crear una estructura de carpetas y archivos para los servicios y controladores de la API.
- [ ] Deberás crear servicios y controladores para las operaciones CRUD de los productos.
- [ ] Deberás crear interfaces para los objetos de producto y los datos necesarios para crear y actualizar un producto.
- [ ] Deberás refactorizar las rutas de productos para seguir una arquitectura en capas.
- [ ] Deberás mover la lógica de negocio de las rutas a los servicios y controladores correspondientes.
- [ ] Deberás integrar las rutas de productos en el servidor Express y eliminar las rutas antiguas.
- [ ] Deberás verificar que las rutas de productos funcionen correctamente después de la refactorización.

### 🎉 ¡Felicitaciones!

Has refactorizado tu API para seguir una arquitectura más escalable y mantenible, utilizando servicios y controladores para separar la lógica de negocio de las rutas. ¡Sigue así!

## Paso 12: Implementar una base de datos PostgreSQL con Prisma

En este paso, vamos a implementar una base de datos PostgreSQL con Prisma, un ORM moderno y seguro para Node.js y TypeScript. Prisma nos permitirá interactuar con la base de datos de forma segura y eficiente, y nos facilitará la implementación de consultas y migraciones de esquema.

Antes de comenzar con el código, necesitas hacer lo siguiente:

1. Crea una cuenta en Prisma ORM.
2. Crea un nuevo proyecto en la Prisma Console. Te sugerimos el nombre api-stock.
3. Crea una base de datos Prisma PostgreSQL. Este proceso tomará unos minutos.
4. Copia tu `DATABASE_URL` y agregalo en el archivo `.env` de tu proyecto.
5. Copia tu DATABASE_URL y agrégalo en el archivo .env de tu proyecto.

Listo, ya podemos comenzar con la implementación de Prisma ORM

### Instalación de Prisma

Ejecuta el siguiente comando en tu terminal para instalar Prisma CLI y Prisma Client:

```bash
npm install -D prisma
npx prisma init
```

### Configuración de Prisma

Luego de inicializar Prisma, se creará un archivo `prisma/schema.prisma` con la configuración de la base de datos. Este archivo es clave para definir el esquema de la base de datos y las tablas que vamos a utilizar en nuestra aplicación y la relación entre ellas.

Edita el archivo `prisma/schema.prisma` y reemplázalo con el siguiente código:

```prisma
generator client {
  provider = "prisma-client-js"
}

datasource db {
  provider = "postgresql"
  url      = env("DATABASE_URL")
}

model Configuration {
  id            String   @id @default(cuid())
  currency      String
  cents         Int
  negativeStock Boolean
  createdAt     DateTime @default(now())
  updatedAt     DateTime @updatedAt
}

model User {
  id          String   @id @default(cuid())
  email       String   @unique
  displayName String?
  password    String
  createdAt   DateTime @default(now())
  updatedAt   DateTime @updatedAt
}

model Product {
  id         String          @id @default(cuid())
  title      String
  price      Int
  stock      Int
  brand      ProductBrand    @relation(fields: [brandId], references: [id], onDelete: Cascade)
  brandId    String
  category   ProductCategory @relation(fields: [categoryId], references: [id], onDelete: Cascade)
  categoryId String
  createdAt  DateTime        @default(now())
  updatedAt  DateTime        @updatedAt
}

model ProductBrand {
  id        String    @id @default(cuid())
  name      String
  createdAt DateTime  @default(now())
  updatedAt DateTime  @updatedAt
  Product   Product[]

  @@map("product_brand")
}

model ProductCategory {
  id        String    @id @default(cuid())
  name      String
  createdAt DateTime  @default(now())
  updatedAt DateTime  @updatedAt
  Product   Product[]

  @@map("product_category")
}
```

Hemos creado 5 modelos en el archivo `prisma/schema.prisma`:

- `Configuration`: Configuración de la aplicación, como la moneda y la cantidad de decimales. (Lo necesitarás más adelante)
- `User`: Usuarios de la aplicación, con un email, nombre de usuario y contraseña. (Lo necesitarás más adelante)
- `Product`: Productos de la aplicación, con un título, precio, stock, marca y categoría.
- `ProductBrand`: Marcas de los productos, con un nombre.
- `ProductCategory`: Categorías de los productos, con un nombre.

Cada modelo tiene campos y relaciones que definen la estructura de la base de datos. Si quieres aprender más sobre el modelado de datos en Prisma, consulta la [documentación oficial de Prisma](https://www.prisma.io/docs/orm/prisma-schema/data-model/models).

### Generación de Migraciones y Prisma Client

> 📚 ¿Que son las migraciones en Prisma ORM? Las migraciones en Prisma ORM son cambios en el esquema de la base de datos que se aplican de forma incremental y controlada. Las migraciones permiten modificar la estructura de la base de datos sin perder datos existentes.

Ejecuta los siguientes comandos en tu terminal para generar tu primera migración y generar el Prisma Client:

```bash
npx prisma migrate dev --name init
npx prisma generate
```

### Instalación de Prisma Client

Prisma Client es una biblioteca de base de datos generada automáticamente que se utiliza para interactuar con la base de datos PostgreSQL. Vamos a instalar Prisma Client en nuestra aplicación para realizar consultas y operaciones en la base de datos.

En tu terminal:

```bash
npm install @prisma/client
```

Además vamos a modificar el archivo `package.json` para agregar un script que genere el Prisma Client automáticamente después de cada migración:

```json
{
  "scripts": {
    "prisma:generate": "npx prisma generate"
  }
}
```

### Configuración de Prisma Client

Crea un archivo `src/libs/prisma.ts` para configurar y exportar el Prisma Client:

```typescript
import { PrismaClient } from "@prisma/client";
import { logger } from "./logger";

export const DB = new PrismaClient();

DB.$connect()
  .then(() => {
    logger.info("💾 Database connected successfully");
  })
  .catch((error) => {
    logger.fatal(error, "💾 Database connection error");
    throw error;
  });

process.on("beforeExit", async () => {
  await DB.$disconnect();
  logger.info("💾 Database connection closed");
});
```

### Integración de Prisma Client en el Servidor

Agrega al archivo `src/index.ts` la importación del cliente de Prisma para que se conecte a la base de datos al iniciar el servidor:

```typescript
import "./libs/prisma";
```

### Criterios de Aceptación del Paso 12

- [ ] Deberás crear una cuenta en Prisma y configurar una base de datos PostgreSQL.
- [ ] Deberás obtener el string de conexión DATABASE_URL y agregarlo en el archivo .env.
- [ ] Deberás instalar Prisma CLI y Prisma Client en tu proyecto.
- [ ] Deberás configurar el archivo prisma/schema.prisma con los modelos y relaciones de la base de datos.
- [ ] Deberás generar la primera migración y el Prisma Client.
- [ ] Deberás configurar y exportar el Prisma Client en un archivo src/libs/prisma.ts.

### 🎉 ¡Felicitaciones!

Has implementado una base de datos PostgreSQL con Prisma, un ORM moderno y seguro para Node.js y TypeScript. Prisma te permitirá interactuar con la base de datos de forma segura y eficiente, y facilitará la implementación de consultas y migraciones de esquema. ¡Sigue así!

## Paso 13: Manejo de Errores y Validaciones Avanzadas

En este paso, vamos a implementar un middleware de manejo de errores y validaciones avanzadas utilizando Zod. Esto nos permitirá estandarizar las respuestas de error y asegurarnos de que los datos recibidos en las solicitudes sean válidos.

> 📚 ¿Qué es Zod? Zod es una biblioteca de validación de esquemas para TypeScript y JavaScript. Permite definir esquemas de datos y validar objetos de manera declarativa y segura.

### Instalación de Zod

Primero, necesitamos instalar Zod, una biblioteca de validación de esquemas para TypeScript.

Ejecuta el siguiente comando en tu terminal:

```bash
npm install zod
```

### Creación del Middleware de Manejo de Errores

Vamos a crear un middleware para manejar los errores de forma centralizada. Crea un archivo `src/middleware/errorHandler.ts` y agrega el siguiente código:

```typescript
import type { NextFunction, Request, Response } from "express";
import { ZodError } from "zod";
import { logger } from "../libs/logger";

export const errorHandler = (
  err: any,
  _req: Request,
  res: Response,
  _next: NextFunction,
) => {
  if (err instanceof ZodError) {
    return res.status(400).json({
      message: "Validation error",
      errors: err.errors,
    });
  }

  logger.error(err);
  res.status(500).json({
    message: "Internal server error",
  });
};
```

### Integración del Middleware en el Servidor

Edita el archivo `src/libs/server.ts` para usar el middleware de manejo de errores:

```typescript
import cors from "cors";
import express from "express";
import pinoHttp from "pino-http";
import { healthCheckRoutes } from "../api/health-check/health-check.routes";
import { productsRoutes } from "../api/products/products.routes";
import { errorHandler } from "../middleware/errorHandler";
import { logger } from "./logger";

const app = express();

// Middleware
app.use(cors());
app.use(express.json());
app.use(pinoHttp({ logger }));

// Routes
app.use("/api/health-check", healthCheckRoutes);
app.use("/api/products", productsRoutes);

// Error handling middleware
app.use(errorHandler);

// Exportar el servidor para usarlo en index.ts
export { app };
```

### Validaciones con Zod

Vamos a crear un esquema de validación para los productos utilizando Zod. Crea un archivo `src/api/products/schemas/product.schema.ts` y agrega el siguiente código:

```typescript
import { z } from "zod";

export const productSchema = z.object({
  title: z.string().min(1, "Title is required"),
  brand: z.string().min(1, "Brand is required"),
  category: z.string().min(1, "Category is required"),
  price: z.number().positive("Price must be a positive number"),
  stock: z.number().int().nonnegative("Stock must be a non-negative integer"),
});
```

### Validación en el Controlador de Creación de Productos

Edita el archivo `src/api/products/controllers/products.create.controller.ts` para validar los datos del producto antes de crear uno nuevo:

```typescript
import type { Request, Response } from "express";
import { productSchema } from "../schemas/product.schema";
import { createProductService } from "../services/products.create.service";

export const createProductController = (req: Request, res: Response) => {
  const validationResult = productSchema.safeParse(req.body);

  if (!validationResult.success) {
    throw validationResult.error;
  }

  const newProduct = createProductService(validationResult.data);
  res.status(201).json(newProduct);
};
```

> 💡 Es importante usar `safeParse` de Zod para filtrar cualquier dato sensible en la respuesta y asegurarse de que solo los datos válidos sean procesados.

### Criterios de Aceptación del Paso 13

- [ ] Deberás instalar la librería `zod` para validaciones.
- [ ] Deberás crear un middleware de manejo de errores en `src/middleware/errorHandler.ts`.
- [ ] Deberás integrar el middleware de manejo de errores en el servidor Express.
- [ ] Deberás crear un esquema de validación para los productos en `src/api/products/schemas/product.schema.ts`.
- [ ] Deberás validar los datos del producto en el controlador de creación de productos.

### 🎉 ¡Felicitaciones!

Has implementado un middleware de manejo de errores y validaciones avanzadas utilizando Zod. Esto te permitirá estandarizar las respuestas de error y asegurarte de que los datos recibidos en las solicitudes sean válidos. ¡Sigue así!

## Paso 14: Adaptar Servicios para Usar Base de Datos Real

En este paso, vamos a actualizar los servicios de tu API de productos para que, en lugar de usar datos mockeados (como arrays en memoria), realicen operaciones reales contra la base de datos PostgreSQL a través de Prisma. Esto significa que modificarás los servicios de obtención, creación, actualización y eliminación de productos para que interactúen directamente con las tablas definidas en tu modelo Prisma (por ejemplo, la tabla `Product` y sus relaciones con `ProductBrand` y `ProductCategory`). Además, ajustaremos los controladores correspondientes para manejar las operaciones asíncronas y los errores de forma correcta.

La integración con la base de datos se realizará utilizando la instancia de Prisma Client configurada en `src/libs/prisma.ts`. Con estos cambios, tu API trabajará con datos persistentes y podrás aplicar consultas reales, transacciones y operaciones complejas en la base de datos.

### 1. Servicio para Obtener Todos los Productos

Actualiza el servicio para obtener todos los productos consultando la base de datos.

Modifica el archivo `src/api/products/services/products.get.all.service.ts`:

```typescript
import { DB } from "../../../libs/prisma";

export const getAllProductsService = async () => {
  const products = await DB.product.findMany({
    include: {
      brand: true,
      category: true,
    },
  });
  return products;
};
```

### 2. Servicio para Crear un Producto

Actualiza el servicio de creación para insertar un nuevo producto en la base de datos. Se consultarán las entidades relacionadas (marca y categoría) antes de crear el producto.

Modifica el archivo `src/api/products/services/products.create.service.ts`:

```typescript
import { DB } from "../../../libs/prisma";

export interface CreateProductData {
  title: string;
  brand: string;
  category: string;
  price: number;
  stock: number;
}

export const createProductService = async (data: CreateProductData) => {
  // Buscar la marca y categoría por nombre
  const brandRecord = await DB.productBrand.findFirst({
    where: { name: data.brand },
  });
  const categoryRecord = await DB.productCategory.findFirst({
    where: { name: data.category },
  });

  if (!brandRecord || !categoryRecord) {
    throw new Error("La marca o categoría no existen en la base de datos");
  }

  const newProduct = await DB.product.create({
    data: {
      title: data.title,
      price: Math.floor(data.price), // Asegurarse de que el precio sea un entero
      stock: data.stock,
      brandId: brandRecord.id,
      categoryId: categoryRecord.id,
    },
    include: {
      brand: true,
      category: true,
    },
  });

  return newProduct;
};
```

### 3. Servicio para Actualizar un Producto

Actualiza el servicio para modificar un producto existente. Se leerán los posibles cambios, incluyendo la actualización de la marca y/o categoría, validando y obteniendo sus IDs correspondientes.

Modifica el archivo `src/api/products/services/products.update.service.ts`:

```typescript
import { DB } from "../../../libs/prisma";

export interface UpdateProductData {
  title?: string;
  brand?: string;
  category?: string;
  price?: number;
  stock?: number;
}

export const updateProductService = async (
  id: string,
  data: UpdateProductData,
) => {
  let brandId: string | undefined;
  let categoryId: string | undefined;

  if (data.brand) {
    const brandRecord = await DB.productBrand.findFirst({
      where: { name: data.brand },
    });
    if (!brandRecord) {
      throw new Error("Marca no encontrada");
    }
    brandId = brandRecord.id;
  }
  if (data.category) {
    const categoryRecord = await DB.productCategory.findFirst({
      where: { name: data.category },
    });
    if (!categoryRecord) {
      throw new Error("Categoría no encontrada");
    }
    categoryId = categoryRecord.id;
  }

  const updatedProduct = await DB.product.update({
    where: { id },
    data: {
      title: data.title,
      price: data.price !== undefined ? Math.floor(data.price) : undefined,
      stock: data.stock,
      ...(brandId && { brandId }),
      ...(categoryId && { categoryId }),
    },
    include: {
      brand: true,
      category: true,
    },
  });

  return updatedProduct;
};
```

### 4. Servicio para Eliminar un Producto

Actualiza el servicio para eliminar un producto, validando que existe en la base de datos antes de borrar el registro.

Modifica el archivo `src/api/products/services/products.delete.service.ts`:

```typescript
import { DB } from "../../../libs/prisma";

export const deleteProductService = async (id: string) => {
  const productToDelete = await DB.product.findUnique({ where: { id } });
  if (!productToDelete) {
    throw new Error("Product not found");
  }

  await DB.product.delete({
    where: { id },
  });

  return { message: "Product deleted", id };
};
```

### 5. Actualización de los Controladores

Modifica los controladores para utilizar las funciones de los servicios adaptadas a Prisma y para manejar correctamente las operaciones asíncronas y los errores.

Para modificar el controlador para Crear un Producto, modifica el archivo `src/api/products/controllers/products.create.controller.ts`:

```typescript
import type { Request, Response } from "express";
import { productSchema } from "../schemas/product.schema";
import { createProductService } from "../services/products.create.service";

export const createProductController = async (req: Request, res: Response) => {
  const validationResult = productSchema.safeParse(req.body);

  if (!validationResult.success) {
    return res.status(400).json({
      message: "Validation error",
      errors: validationResult.error.errors,
    });
  }

  try {
    const newProduct = await createProductService(validationResult.data);
    res.status(201).json(newProduct);
  } catch (error: any) {
    res.status(500).json({ message: error.message });
  }
};
```

Para modificar el controlador para Actualizar un Producto, modifica el archivo `src/api/products/controllers/products.update.controller.ts`:

```typescript
import type { Request, Response } from "express";
import { productSchema } from "../schemas/product.schema"; // (Opcional: para validar datos)
import { updateProductService } from "../services/products.update.service";

export const updateProductController = async (req: Request, res: Response) => {
  const { id } = req.params;
  const validationResult = productSchema.safeParse(req.body);

  if (!validationResult.success) {
    return res.status(400).json({
      message: "Validation error",
      errors: validationResult.error.errors,
    });
  }

  try {
    const updatedProduct = await updateProductService(
      id,
      validationResult.data,
    );
    res.status(200).json(updatedProduct);
  } catch (error: any) {
    if (
      error.message === "Marca no encontrada"
      || error.message === "Categoría no encontrada"
    ) {
      return res.status(404).json({ message: error.message });
    }
    res.status(500).json({ message: error.message });
  }
};
```

Para modificar el controlador para Eliminar un Producto, modifica el archivo `src/api/products/controllers/products.delete.controller.ts`:

```typescript
import type { Request, Response } from "express";
import { deleteProductService } from "../services/products.delete.service";

export const deleteProductController = async (req: Request, res: Response) => {
  const { id } = req.params;

  try {
    const result = await deleteProductService(id);
    res.status(200).json(result);
  } catch (error: any) {
    if (error.message === "Product not found") {
      return res.status(404).json({ message: error.message });
    }
    res.status(500).json({ message: error.message });
  }
};
```

💡 Es una buena práctica utilizar Zod dentro de cada servicio para validar tanto los datos de entrada como los datos de salida. Esto asegura que los datos que se procesan y se devuelven cumplen con los esquemas definidos, lo que ayuda a prevenir errores y a mantener la integridad de los datos en toda la aplicación.

Por ejemplo, puedes definir un esquema de validación para los datos de entrada en el servicio de creación de productos y otro esquema para los datos de salida:

Crea un archivo `src/api/products/schemas/product.schema.ts` y agrega los esquemas de validación:

```typescript
import { z } from "zod";

const createProductInputSchema = z.object({
  title: z.string().min(1, "Title is required"),
  brand: z.string().min(1, "Brand is required"),
  category: z.string().min(1, "Category is required"),
  price: z.number().positive("Price must be a positive number"),
  stock: z.number().int().nonnegative("Stock must be a non-negative integer"),
});

const createProductOutputSchema = z.object({
  id: z.string(),
  title: z.string(),
  brand: z.string(),
  category: z.string(),
  price: z.number(),
  stock: z.number(),
  createdAt: z.string(),
  updatedAt: z.string(),
});

export const createProductService = async (data: CreateProductData) => {
  const validationResult = createProductInputSchema.safeParse(data);

  if (!validationResult.success) {
    throw new Error("Validation error");
  }

  // Lógica para crear el producto en la base de datos
  const newProduct = await DB.product.create({
    data: validationResult.data,
    include: {
      brand: true,
      category: true,
    },
  });

  const outputValidationResult = createProductOutputSchema.safeParse(
    newProduct,
  );

  if (!outputValidationResult.success) {
    throw new Error("Output validation error");
  }

  return outputValidationResult.data;
};
```

De esta manera, aseguras que tanto los datos de entrada como los datos de salida cumplen con los esquemas definidos, lo que mejora la robustez y la confiabilidad de tu aplicación. Te invitamos a crear schemas para los demás servicios y controladores siguiendo esta misma lógica.

### Criterios de Aceptación del Paso 14

- [ ] Actualizar el servicio de obtención de productos en `src/api/products/services/products.get.all.service.ts` para consultar la base de datos usando Prisma.
- [ ] Actualizar el servicio de creación en `src/api/products/services/products.create.service.ts` para insertar un nuevo producto, validando y consultando las relaciones de marca y categoría.
- [ ] Actualizar el servicio de actualización en `src/api/products/services/products.update.service.ts` para modificar un producto existente.
- [ ] Actualizar el servicio de eliminación en `src/api/products/services/products.delete.service.ts` para remover el producto de la base de datos.
- [ ] Modificar los controladores en `src/api/products/controllers/` para utilizar las funciones asíncronas de los servicios y manejar errores de forma adecuada.
- [ ] Ejecutar las pruebas para verificar que las operaciones CRUD funcionan correctamente contra la base de datos real.

### 🎉 ¡Felicitaciones!

Has adaptado exitosamente tus servicios y controladores para interactuar con una base de datos PostgreSQL real mediante Prisma. Con estos cambios, tu API ahora trabajará con datos persistentes y estarás un paso más cerca de construir una solución escalable y profesional. ¡Sigue así y continúa avanzando en el curso!

## Paso 15: Despliegue y Configuración en Producción

En este paso, desplegaremos tu API en Railway, una plataforma en la nube que facilita el hosting de aplicaciones. Aprovecharemos la base de datos PostgreSQL y la configuración de Prisma ya establecidas, y configuraremos las variables de entorno y logging para el ambiente de producción.

### Creación de una Cuenta y Servicio en Railway

Si aún no tienes una cuenta en Railway, puedes crear una gratuita visitando [Railway](https://railway.app/). Sigue estos pasos básicos:

1. Regístrate con tu email o con tu cuenta de GitHub.
2. Una vez dentro, haz clic en **"New Project"**.
3. Selecciona la opción **"Deploy from GitHub Repo"** y conecta tu repositorio.
4. Configura el servicio, asegurándote de establecer la variable `DATABASE_URL` (con el string de conexión de tu base de datos PostgreSQL) y otras variables necesarias para la ejecución, como `NODE_ENV` con el valor `"production"`.
5. Railway generará una URL pública para acceder a tu API en producción.

### Configuración de Variables de Entorno y Logs

1. **Variables de Entorno:**\
   Asegúrate de definir en Railway las siguientes variables:
   - `DATABASE_URL`: Conecta tu base de datos PostgreSQL.
   - `NODE_ENV`: Establecido a `"production"`.
   - Cualquier otra variable que tu aplicación requiera (por ejemplo, `PORT`).

2. **Logging en Producción:**\
   Revisa que en el archivo `src/libs/logger.ts` el nivel de log se configure según el entorno:
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
   Esto garantizará que en producción se muestren logs a nivel `info` para evitar el exceso de información.

### Actualización del Script de Inicio

Asegúrate de que el script de inicio en tu `package.json` utilice el código compilado y respete las variables de entorno:

```json
{
  "scripts": {
    "start": "node --env-file=.env dist/index.js"
  }
}
```

> Nota: Railway manejará sus propias variables de entorno en el dashboard, por lo que es crucial que la variable `DATABASE_URL` y `NODE_ENV` estén correctamente definidas allí.

### Pruebas y Validaciones Previas al Despliegue

Antes de desplegar, verifica los siguientes puntos:

- Ejecuta `npm test` para asegurarte de que todos los tests pasen.
- Comprueba el funcionamiento de la API en ambiente local en modo producción:
  1. Compila el proyecto con `npm run build`.
  2. Inicia la aplicación con `npm start`.
- Revisa los logs para confirmar que no se presenten errores y que la conexión a la base de datos sea exitosa.

Una vez validados estos pasos, realiza el despliegue en Railway siguiendo el proceso de importación del repositorio.

### Solución de Problemas Comunes

- Verificá que las variables de entorno estén correctamente definidas.
- Revisá los logs (usando Pino) para identificar problemas de conexión a la base de datos.
- Probá localmente en modo producción antes del despliegue:

```bash
npm run build
npm start
```

> 💡 Consejo: Si se presentan errores en la conexión a la base de datos, consultá la documentación de Prisma y Railway.

### Criterios de Aceptación del Paso 15

- [ ] Deberás tener una cuenta en Railway (puedes crear una gratuita [aquí](https://railway.app/)).
- [ ] Deberás configurar en Railway las variables de entorno, incluyendo `DATABASE_URL` y `NODE_ENV=production`.
- [ ] La API deberá conectarse correctamente a la base de datos PostgreSQL en el entorno de Railway.
- [ ] Los logs deben indicar que la aplicación se inicia sin errores y en modo producción.
- [ ] Deberás verificar el funcionamiento de la API en producción accediendo a la URL proporcionada por Railway.

### 🎉 ¡Felicitaciones!

Has completado el despliegue de tu API en Railway, configurando adecuadamente las variables de entorno y los logs para el ambiente de producción. ¡Tu API ahora está lista para recibir tráfico real y crecer de forma escalable! ¡Excelente trabajo y sigue adelante!

## Paso 16: Implementación de CI/CD

En este paso, configuraremos GitHub Actions para automatizar las pruebas y el despliegue continuo de tu API. Con esta integración, cada vez que realices cambios en la rama principal se ejecutarán los tests y, de estar todo correcto, se compilará y desplegará la aplicación. Esto te ayudará a detectar errores rápidamente y a mantener un proceso de despliegue confiable y eficiente.

### Creación del Workflow en GitHub Actions

1. Dentro de tu repositorio, crea el directorio `.github/workflows`.
2. Crea un archivo llamado `ci-cd.yml` en dicho directorio.

En este archivo definirás el workflow de CI/CD. Un ejemplo de configuración es el siguiente:

```yaml
name: CI/CD Pipeline

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v3

      - name: Setup Node.js environment
        uses: actions/setup-node@v3
        with:
          node-version: 16

      - name: Install dependencies
        run: npm install

      - name: Run tests
        run: npm test

      - name: Build project
        run: npm run build

      - name: Deploy to Railway
        if: github.ref == 'refs/heads/main'
        run: |
          npx railway deploy
        env:
          RAILWAY_TOKEN: ${{ secrets.RAILWAY_TOKEN }}
```

> 📚 Nota:
>
> - Asegúrate de tener configurado el secret `RAILWAY_TOKEN` en la sección de secrets de tu repositorio en GitHub. Railway ofrece un CLI que permite desplegar tu servicio; si aún no lo tienes instalado, puedes agregarlo a través de `npx railway` en tus scripts.
> - Revisa que los scripts definidos en tu `package.json` (como `npm test` y `npm run build`) funcionen correctamente.

### Pruebas y Validaciones Previas al Despliegue

Antes de integrar el workflow de CI/CD, sigue estos pasos en local:

- Ejecuta `npm test` para confirmar que las pruebas pasen sin errores.
- Realiza la compilación con `npm run build` y verifica que no se produzcan errores.
- Si usas Railway, prueba manualmente el despliegue con `npx railway deploy` para asegurarte de que la conexión y las variables de entorno están correctamente configuradas.

### Criterios de Aceptación del Paso 16

- [ ] Deberás crear el directorio `.github/workflows` en tu repositorio si aún no existe.
- [ ] Deberás crear un archivo `ci-cd.yml` que defina el workflow para ejecutar tests, compilar la aplicación y desplegarla.
- [ ] El workflow deberá ejecutarse en cada push o pull request a la rama `main`.
- [ ] Deberás tener configurado el secret `RAILWAY_TOKEN` en GitHub para el despliegue.
- [ ] Los tests deben correr y pasar, y el despliegue se debe ejecutar sin errores.

### 🎉 ¡Felicitaciones!

Has implementado con éxito un pipeline de CI/CD utilizando GitHub Actions. Ahora, cada cambio en la rama principal activará automáticamente pruebas y despliegues, lo que garantiza la calidad y la estabilidad de tu API en producción. ¡Excelente trabajo y sigue avanzando en tu aprendizaje!

> 💡 Consejo: Revisa periódicamente los logs de GitHub Actions para detectar posibles fallos o áreas de mejora en tu pipeline de CI/CD.

## ⚠️ Recuerda detener y eliminar cualquier instancia de tu API en Railway si ya no la necesitas para evitar costos innecesarios.

Si bien Railway ofrece un plan gratuito, es importante mantener un control de los recursos utilizados para evitar cargos adicionales. Si no estás utilizando tu API en producción, asegúrate de detener y eliminar cualquier instancia para evitar costos innecesarios.

# 🏁 ¡Felicidades! Has completado el Curso de API REST con Node.js y TypeScript

¡Enhorabuena! Has completado el Curso de API REST con Node.js y TypeScript. Has aprendido a construir una API RESTful escalable y mantenible utilizando tecnologías modernas como Express, Prisma, Zod y Railway. Has implementado funcionalidades esenciales como CRUD de productos, servicios, controladores, validaciones, manejo de errores, base de datos PostgreSQL, despliegue en producción y CI/CD. ¡Excelente trabajo!

💡 Es fundamental que entiendas que este curso es solo el comienzo para convertirte en un gran desarrollador backend, pero que debes seguir aprendiendo y practicando con frecuencia para lograr tus objetivos. La práctica constante y la curiosidad por aprender nuevas tecnologías y mejores prácticas te ayudarán a mejorar tus habilidades y a mantenerte actualizado en un campo que evoluciona rápidamente. ¡Sigue adelante y nunca dejes de aprender!

# 🚀 Recursos Adicionale

- [Express.js](https://expressjs.com/): Documentación oficial de Express.js.
- [Prisma](https://www.prisma.io/): Documentación oficial de Prisma ORM.
- [Zod](https://zod.dev/): Documentación oficial de Zod.
- [Railway](https://railway.app/): Documentación oficial de Railway.
- [GitHub Actions](https://docs.github.com/en/actions): Documentación oficial de GitHub Actions.
- [Documentación de Pino](https://getpino.io/): Documentación oficial de Pino.
- [Biome para vscode](https://marketplace.visualstudio.com/items?itemName=biomejs.biome): Extensión de Biome para Visual Studio Code.

# 🔜 Próximos Pasos

> ### ⚠️ Importante: Esta guía se encuentra en desarrollo y puede sufrir cambios en el futuro. Si tienes alguna sugerencia o corrección, no dudes en abrir un issue o una pull request. ¡Gracias por tu colaboración!

- Paso 16: Implementación de CI/CD
  - Configurar GitHub Actions para pruebas automatizadas y despliegue continuo.

# Pasos opcionales

Esta serie de pasos busca que el usuario continue en su aprendizaje incluyendo desafíos más complejos y avanzados. Si deseas continuar con el curso, puedes seguir con los pasos opcionales.

- Opcional: Implementar Paginación y Filtros en Endpoints
  - Agregar paginación y filtros dinámicos en los endpoints.
  - Optimizar consultas para mejorar el rendimiento en grandes volúmenes de datos.

- Opcional: Documentación Automática con OpenAPI (Swagger)
  - Generar documentación interactiva para la API.
  - Agregar ejemplos de uso y esquemas de respuesta.
  - Permitir pruebas de endpoints directamente desde la documentación.

- Opcional: CRUD de Usuarios, Roles y Autenticación
  - Implementar endpoints para crear, leer, actualizar y eliminar usuarios y roles.
  - Agregar endpoints para obtener y refrescar tokens de acceso.
  - Implementar endpoints para asignar y revocar roles y permisos.
  - Implementar autenticación con JWT y Passport.
  - Implementar autorización basada en roles y permisos.
  - Proteger rutas sensibles y recursos críticos.
  - Agregar pruebas automatizadas para los endpoints de usuarios y roles.

- Opcional: Reportes y Estadísticas
  - Implementar endpoints para generar reportes y estadísticas.
  - Agregar filtros y parámetros para personalizar los reportes.

- Paso 18: Movimientos de stocks y Control de Inventario
  - Implementar endpoints para registrar movimientos de stocks.
  - Agregar lógica de negocio para controlar el inventario.
  - Implementar endpoints para consultar el stock disponible y los movimientos de inventario.
  - Agregar pruebas automatizadas para los endpoints de inventario.

- Paso 20: Módulo de importar/exportar datos
  - Implementar endpoints para importar y exportar datos en formato CSV o JSON.
  - Agregar validaciones y transformaciones de datos para garantizar la integridad.

- Paso 21: Seguridad y Buenas Prácticas en Producción
  - Configurar Helmet y Rate Limiting para proteger la API.
  - Evitar inyecciones SQL y ataques XSS.
  - Agregar CORS con restricciones adecuadas.
