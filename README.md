# 📦 api-stock

Este es un repositorio educativo diseñado para aprender paso a paso cómo construir una API REST moderna para control de inventario utilizando TypeScript, Express v5, Prisma ORM y PostgreSQL.

## Propósito

Este proyecto está estructurado como una guía práctica de aprendizaje. Al seguir las instrucciones paso a paso, aprenderás a construir una API profesional mientras aplicas las mejores prácticas de desarrollo moderno. El objetivo es proporcionarte las habilidades necesarias para convertirte en un desarrollador backend moderno y competente.

### Herramientas Necesarias
- [Visual Studio Code](https://code.visualstudio.com/)
- [GitHub](https://github.com/) (para control de versiones)
- [ChatGPT](https://chat.openai.com/) (como asistente de aprendizaje)
- [Node.js y npm](https://nodejs.org/)

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
npx tsc --init
```

Esto creará un archivo tsconfig.json en tu proyecto. A continuación, te muestro un ejemplo de un archivo tsconfig.json optimizado para una aplicación Node.js:

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
Ahora, vamos a agregar algunos scripts útiles en nuestro archivo package.json. Abre el archivo package.json y agrega los siguientes scripts en la sección "scripts":

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

### Hello World en consola

Para verificar que todo está configurado correctamente, vamos a crear un simple "Hello World" en la consola. Crea un archivo src/index.ts con el siguiente contenido:

```typescript
console.log("Hello, World!");
```

Ahora, ejecuta el siguiente comando en tu terminal:

```bash
npm run dev
```

Deberías ver el mensaje "Hello, World!" impreso en la consola. Si ves este mensaje, ¡tu configuración de TypeScript está lista y funcionando! Ahora, puedes avanzar al siguiente paso.

## Paso 3: Configuración del Servidor Express y primer endpoint
En este paso, vamos a instalar Express y CORS, y crearemos un endpoint /api/health-check que devolverá { status: "ready" }.

### Instalar Dependencias
Ejecuta el siguiente comando en tu terminal para instalar Express y CORS:

```bash
npm install express cors
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
  res.json({ status: "ready" });
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
  console.log(`✅ Server running at http://localhost:${PORT}`);
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
{ "status": "ready" }
```

¡Felicidades! Has creado tu primer endpoint en Express. Ahora, puedes avanzar al siguiente paso para implementar más funcionalidades en tu API.
