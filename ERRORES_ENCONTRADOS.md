# Errores encontrados

**Nombre:**
**Fecha:**

Prisma Schema :Derlyz

> Tipos válidos: `Typo` (editor en rojo) · `Sintaxis` · `Terminal` (prisma / arranque / endpoint / tests) · `Lógica`

| # | Archivo | Línea | Tipo | ¿Qué estaba mal? | ¿Cómo lo detectaste? | ¿Cómo lo solucionaste? |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | `prisma/schema.prisma` | 12 | Typo | Se llamaba `Strng` en vez de `String` en el campo `nombre` del modelo `Autor` | VS Code lo marcó en rojo / `npx prisma generate`: *"Error: Type "Strng" is neither a built-in type, nor refers to another model, composite type, or enum."* | Corregí el tipo de dato a `String` |
| 2 | `prisma/schema.prisma` | 63 | Typo | Se llamaba `references: [ID]` en vez de `references: [id]` en la relación `socio` del modelo `Prestamo` | VS Code lo marcó en rojo / `npx prisma generate`: *"Error validating: The argument `references` must refer only to existing fields in the related model `Socio`. The following fields do not exist in the related model: ID"* | Corregí el argumento a `references: [id]` |
| 3 | `prisma.config.ts` | 10 | Terminal | Se llamaba `process.env['DATABASE_ULR']` en vez de `process.env['DATABASE_URL']` | Al ejecutar comandos de Prisma (`npx prisma migrate dev`) | Corregí el nombre de la variable de entorno a `DATABASE_URL` |
| 4 | `src/prisma/prisma.service.ts` | 6 | Typo | Se llamaba `extends PrismaClien` en vez de `extends PrismaClient` | VS Code lo marcó en rojo: *"Cannot find name 'PrismaClien'. Did you mean 'PrismaClient'?"* | Corregí el nombre de la clase a `PrismaClient` |
| 5 | | | | | | |


<!-- Agrega todas las filas que necesites -->

Modulo AUTORES: Leonardo

| # | Archivo | Línea | Tipo | ¿Qué estaba mal? | ¿Cómo lo detectaste? | ¿Cómo lo solucionaste? |
| --- | --- | --- | --- | --- | --- | --- |
| 0 | `src/ejemplo/ejemplo.service.ts` | 10 | Typo | _(fila de ejemplo, bórrala) se llamaba `this.prisma.usuaro` en vez de `this.prisma.usuario`_ | _VS Code lo marcó en rojo: "Property 'usuaro' does not exist"_ | _corregí el nombre del modelo_ |
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
| 5 | | | | | | |


Modulo LIBROS: Oscar

| # | Archivo | Línea | Tipo | ¿Qué estaba mal? | ¿Cómo lo detectaste? | ¿Cómo lo solucionaste? |
| --- | --- | --- | --- | --- | --- | --- |
| 0 | `src/ejemplo/ejemplo.service.ts` | 10 | Typo | _(fila de ejemplo, bórrala) se llamaba `this.prisma.usuaro` en vez de `this.prisma.usuario`_ | _VS Code lo marcó en rojo: "Property 'usuaro' does not exist"_ | _corregí el nombre del modelo_ |
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
| 5 | | | | | | |

Modulo Socios: Derlyz

| # | Archivo | Línea | Tipo | ¿Qué estaba mal? | ¿Cómo lo detectaste? | ¿Cómo lo solucionaste? |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | `src/socio/socio.module.ts` | 3 | Sintaxis | Al import `from './socio.service'` le faltaba la extensión `.js` requerida | VS Code lo marcó en rojo *"No se encuentra el módulo "./socio.service" ni sus declaraciones de tipos correspondientes."* | Cambié el import a `from './socio.service.js'` |
| 2 | `src/socio/socio.controller.ts` | 26 | Sintaxis | Faltaba la llave de cierre `}` en el método `findAll()` | VS Code lo marcó en rojo *"Se esperaba '}'."* | Agregué la llave de cierre `}` al método `findAll()` |
| 3 | `src/socio/dto/create-socio.dto.ts` | 2 | Typo | `IsEmail` se estaba importando desde `'class-transformer'` en lugar de `'class-validator'` | VS Code lo marcó en rojo: *"El módulo '"class-transformer"' no tiene ningún miembro 'IsEmail' exportado."* | Moví `IsEmail` al import de `'class-validator'` |
| 4 | `src/socio/socio.service.ts` | 26 | Lógica | En `findAll()` filtraba con `where: { activo: false }` en vez de `{ activo: true }`, incumpliendo la regla de listar **solo los socios activos** | Al revisar las reglas de negocio del README / al ejecutar tests o `GET /socios` | Cambié el filtro a `where: { activo: true }` |
| 5 | | | | | | |

Modulo Prestamos: Oscar

| # | Archivo | Línea | Tipo | ¿Qué estaba mal? | ¿Cómo lo detectaste? | ¿Cómo lo solucionaste? |
| --- | --- | --- | --- | --- | --- | --- |
| 0 | `src/ejemplo/ejemplo.service.ts` | 10 | Typo | _(fila de ejemplo, bórrala) se llamaba `this.prisma.usuaro` en vez de `this.prisma.usuario`_ | _VS Code lo marcó en rojo: "Property 'usuaro' does not exist"_ | _corregí el nombre del modelo_ |
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
| 5 | | | | | | |

Modulo Prestamos: Sara

| # | Archivo | Línea | Tipo | ¿Qué estaba mal? | ¿Cómo lo detectaste? | ¿Cómo lo solucionaste? |
| --- | --- | --- | --- | --- | --- | --- |
| 0 | `src/ejemplo/ejemplo.service.ts` | 10 | Typo | _(fila de ejemplo, bórrala) se llamaba `this.prisma.usuaro` en vez de `this.prisma.usuario`_ | _VS Code lo marcó en rojo: "Property 'usuaro' does not exist"_ | _corregí el nombre del modelo_ |
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
| 5 | | | | | | |

Main, Module App, PrismaModule: Derlyz

| # | Archivo | Línea | Tipo | ¿Qué estaba mal? | ¿Cómo lo detectaste? | ¿Cómo lo solucionaste? |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | `src/main.ts` | 15 | Sintaxis | Faltaba el paréntesis de cierre `)` en `app.useGlobalPipes(...)` (solo había un `;`) | VS Code lo marcó en rojo / `npm run build`: *"')' expected"* | Agregué el paréntesis de cierre `);` |
| 2 | `src/app.module.ts` | 18 | Terminal | `PrestamoModule` estaba importado en el archivo pero no registrado dentro del array `imports: [...]` de `@Module` | El editor marcaba `PrestamoModule` como no usado) | Agregué `PrestamoModule` al arreglo `imports` de `AppModule` |
| 3 | `src/prisma/prisma.module.ts` | 4 | Terminal | Faltaba el decorador `@Global()` en `PrismaModule`, impidiendo que `SocioModule` y los demás módulos pudieran inyectar `PrismaService` | Al arrancar `npm run start:dev`: *"Nest can't resolve dependencies of the SocioService (?). Please make sure that the argument PrismaService at index [0] is available"* | Importé y agregué `@Global()` encima de `@Module` en `PrismaModule` |

## Reflexión final

1. ¿Qué tipo de error te costó más encontrar y por qué?
2. ¿Qué herramienta te ayudó más (editor, terminal, Swagger/Postman, tests)?
3. ¿Qué harías para evitar este tipo de errores en tus propios proyectos?
