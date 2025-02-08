# 📦 api-stock

Este es un repositorio educativo diseñado para aprender paso a paso cómo construir una API REST moderna para control de inventario utilizando TypeScript, Express v5, Prisma ORM y PostgreSQL.

## Propósito

Este proyecto está estructurado como una guía práctica de aprendizaje. Al seguir las instrucciones paso a paso, aprenderás a construir una API profesional mientras aplicas las mejores prácticas de desarrollo moderno. El objetivo es proporcionarte las habilidades necesarias para convertirte en un desarrollador backend moderno y competente.

### Herramientas Necesarias
- [Visual Studio Code](https://code.visualstudio.com/) (Editor de código recomendado)
- [GitHub](https://github.com/) (para control de versiones)
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
Este proyecto fue creado por [Germán Aliprandi](mailto:galiprandi@gmail.com) y te inito a contactarme si tienes alguna pregunta o sugerencia.

### Licencia
Este proyecto está bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles.

## Paso 1: Fork del repositorio [api-stock](https://github.com/galiprandi/api-stock)

> 📚 ¿Que es un fork? Un fork es una copia de un repositorio que se crea en tu cuenta de GitHub. Permite que puedas hacer cambios en el proyecto original sin afectar el repositorio principal. Los forks son útiles cuando deseas contribuir a un proyecto de código abierto, ya que puedes trabajar en tus propias modificaciones y luego proponer que se integren en el proyecto original mediante un pull request.

### Verificar que tengas una cuenta en GitHub

Si no tienes una cuenta en GitHub, [regístrate en GitHub](https://github.com/join).
Si ya tienes una cuenta, asegúrate de haber iniciado sesión.

### Instalar y configurar Git y GitHub CLI
Instalar Git:

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
Hacer el fork del repositorio:

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
npm i -D typescript
npx tsc --init
```

Esto creará un archivo tsconfig.json en tu proyecto. A continuación, te muestro un ejemplo de un archivo tsconfig.json optimizado para una aplicación Node.js, reemplaza el contenido de tu archivo tsconfig.json con el siguiente código:

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
Ahora, vamos a agregar algunos scripts útiles en nuestro archivo `package.json`. Abre el archivo package.json y agrega los siguientes scripts en la sección "scripts":

```json
{
  "scripts": {
    "dev": "ts-node-dev --respawn --transpile-only src/index.ts",
    "build": "tsc",
    "start": "node dist/index.js"
  }
}
```

- `npm run dev`: Este script utiliza ts-node-dev para ejecutar tu aplicación en modo de desarrollo, permitiendo recargas automáticas cuando cambias el código.

- `npm run build`: Este script compila tu código TypeScript en JavaScript, colocando los archivos compilados en el directorio dist.

- `npm run start`: Este script ejecuta la versión compilada de tu aplicación desde el directorio dist.

Con estos scripts, estarás listo para desarrollar, compilar y ejecutar tu aplicación Node.js con TypeScript.

### Instalemos `ts-node-dev` y `@types/node`
Para poder ejecutar nuestra aplicación en modo de desarrollo, necesitamos instalar `ts-node-dev` y `@types/node`. Ejecuta el siguiente comando en tu terminal:

```bash
npm install -D ts-node-dev @types/node
```

### Hello World en consola

Para verificar que todo está configurado correctamente, vamos a crear un simple "Hello World" en la consola. Crea un archivo `src/index.ts` con el siguiente contenido:

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
[INFO] 01:00:00 ts-node-dev ver. 2.0.0 (using ts-node ver. 10.9.2, typescript ver. 5.7.3)
Hello, World!
```

### Probando el hot-reloading
Para probar el hot-reloading, modifica el mensaje en `src/index.ts` por "Hello, TypeScript!" y guarda el archivo. Deberías ver que el servidor se reinicia automáticamente y muestra el nuevo mensaje en la consola.

```bash
# Salida esperada
[INFO] 01:00:00 ts-node-dev ver. 2.0.0 (using ts-node ver. 10.9.2, typescript ver. 5.7.3)
Hello, TypeScript!
```

¡Excelente! Has configurado correctamente tu proyecto con TypeScript y ts-node-dev. Ahora, puedes avanzar al siguiente paso para configurar un servidor Express.

## Paso 3: Configuración del Servidor Express y primer endpoint
En este paso, vamos a instalar Express y CORS, y crearemos un endpoint /api/health-check que devolverá { status: "ready" }.

### Instalar Dependencias
Ejecuta el siguiente comando en tu terminal para instalar Express y CORS:

```bash
npm install "express@>=5.0.0" cors
npm install --save-dev @types/express @types/cors
```

### Configurar el Servidor en src/libs/server.ts
Crea el archivo `src/libs/server.ts` y agrega el siguiente código:

```typescript
import express from "express";
import cors from "cors";

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

### Inicializar el Servidor en src/index.ts
Edita `src/index.ts` para importar e iniciar el servidor:

```typescript
import { app } from "./libs/server";

const PORT = process.env.PORT || 3000;

app.listen(PORT, () => {
  console.log(`🚀 Server running at http://localhost:${PORT}/api/health-check`);
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

¡Felicidades! Has creado tu primer endpoint en Express. Ahora, puedes avanzar al siguiente paso para implementar más funcionalidades en tu API.

## Paso 4: Agregar Pruebas para /api/health-check

> 📚 ¿Qué son las pruebas unitarias? Las pruebas unitarias son pruebas automatizadas que verifican que una unidad de código (como una función o un módulo) funcione correctamente. Estas pruebas se centran en probar partes específicas del código para garantizar que se comporten como se espera.

En este paso, agregaremos pruebas automatizadas para verificar que el endpoint /api/health-check responde correctamente.

### Instalar Dependencias
Primero, necesitamos instalar Vitest y Supertest para realizar pruebas automatizadas. Ejecuta el siguiente comando en tu terminal:

```bash
npm install --save-dev vitest supertest @types/supertest
```

### Crear el Archivo de Pruebas


> 📌 Todos los archivos de pruebas unitarias estarán alojados en la carpeta `src/tests/` lo que facilita su organización y mantenimiento.

Crea el archivo `src/tests/health-check.test.ts` y agrega el siguiente código:

```typescript
import { describe, it, expect } from "vitest";
import request from "supertest";
import { app } from "../libs/server";

describe("GET /api/health-check", () => {
  it("should return { status: 'ready' }", async () => {
    const response = await request(app).get("/api/health-check");
    
    expect(response.status).toBe(200);
    expect(response.body).toHaveProperty("status", "ready");
  });
});
```

### Agregar el Script de Pruebas en `package.json`

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
 ✓ src/tests/health-check.test.ts (1 test) 28ms
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
    { id: 1, title: "Laptop", brand: "Apple", category: "Electronics", price: 1299.99, stock: 10 },
    { id: 2, title: "Smartphone", brand: "Samsung", category: "Electronics", price: 899.99, stock: 20 },
    { id: 3, title: "Tablet", brand: "Amazon", category: "Electronics", price: 299.99, stock: 5 },
    { id: 4, title: "Smartwatch", brand: "Fitbit", category: "Electronics", price: 199.99, stock: 15 },
    { id: 5, title: "Headphones", brand: "Sony", category: "Electronics", price: 99.99, stock: 30 },
    { id: 6, title: "Backpack", brand: "North Face", category: "Fashion", price: 79.99, stock: 25 },
    { id: 7, title: "Sneakers", brand: "Nike", category: "Fashion", price: 129.99, stock: 40 },
    { id: 8, title: "T-shirt", brand: "Adidas", category: "Fashion", price: 29.99, stock: 50 },
    { id: 9, title: "Jeans", brand: "Levi's", category: "Fashion", price: 59.99, stock: 20 },
    { id: 10, title: "Sunglasses", brand: "Ray-Ban", category: "Fashion", price: 149.99, stock: 10 }
];
```

> 💡 Este archivo nos será de utiiidad para simular una base de datos de productos hasta que implementemos la conexión con una base de datos real.

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
import express from "express";
import cors from "cors";

// Rutas
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

Agrega pruebas automatizadas para la ruta `/api/products`. Crea un archivo `src/tests/products.test.ts` y agrega el siguiente código:

```typescript
import { describe, it, expect } from "vitest";
import request from "supertest";
import { app } from "../libs/server";
import { products } from "../data/products";

describe("GET /api/products", () => {
  it("should return a list of products", async () => {
    const response = await request(app).get("/api/products");
    
    expect(response.status).toBe(200);
    // ⚠️ Introducimos un error intencional en la prueba
    expect(response.body).not.toEqual(products);
  });
});
```
📚 ¿ Qué es TDD? El Desarrollo Guiado por Pruebas (TDD) es una metodología de desarrollo de software en la que las pruebas se escriben antes del código de producción. El ciclo de TDD generalmente sigue estos pasos:

Escribir una prueba que falle: Escribir una prueba automatizada para una nueva funcionalidad que aún no está implementada.
Escribir el código mínimo para pasar la prueba: Implementar el código necesario para que la prueba pase.
Refactorizar el código: Mejorar el código asegurándose de que todas las pruebas sigan pasando.
En este caso, hemos introducido un error intencional en la prueba para que falle. El siguiente paso es corregir el código para que la prueba pase.

### Corregir la Prueba

Corrige la prueba en `src/tests/products.test.ts` para que pase correctamente. Lee atentamente el código de la prueba, ejecuta las pruebas y asegúrate de que pasen correctamente. 

 ## 🎉 ¡Felicitaciones!

Haz avanzado mucho y ya tiene la estructura básica de tu API REST y los conocimientos necesarios para agregar nuevas rutas y funcionalidades. A partir de ahora las intrucciones serán menos precisas y tendrás que investigar y probar por tu cuenta. Las proximas tareas serán más parecidas a requeriemientos de un cliente y tendrás que implementarlos por tu cuenta, pero siempre especificaremos los criterios de aceptación que deberás cumplir.

## Paso 6: Implementar un Endpoint para Crear Productos

En este paso, vamos a implementar un endpoint POST /api/products que permita crear un nuevo producto. El endpoint recibirá los datos del producto en el cuerpo de la solicitud y devolverá el producto creado con un ID único.

Los pasos a seguir son los siguientes:
1. Crear la ruta POST /api/products en el archivo src/routes/products.ts.
2. Recuperar del body de la solicitud los datos del producto a crear.
3. Generar un ID único para el nuevo producto. Por ahora puedes usar la longitud del array + 1 como ID.
4. Agregar el nuevo producto al array de productos usando el método push.
5. Devolver el producto creado con el código de estado 201 (Created).
6. Verifica que el GET /api/products devuelva las lista de productos con el nuevo producto creado.
7. Agregar pruebas automatizadas para el endpoint POST /api/products.


Comencemos creando primero las pruebas unitarias, crea el archivo `src/tests/products.post.test.ts` y agrega el siguiente código:

```typescript
import { describe, it, expect } from "vitest";
import request from "supertest";
import { app } from "../libs/server";

describe("POST /api/products", () => {
    it("should create a new product", async () => {
      const newProduct = {
        title: "Smart Speaker",
        brand: "Google",
        category: "Electronics",
        price: 99.99,
        stock: 15
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
