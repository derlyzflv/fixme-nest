# Errores encontrados

**Nombre:**
**Fecha:**

Prisma Schema :Derlyz

> Tipos válidos: `Typo` (editor en rojo) · `Sintaxis` · `Terminal` (prisma / arranque / endpoint / tests) · `Lógica`

| # | Archivo | Línea | Tipo | ¿Qué estaba mal? | ¿Cómo lo detectaste? | ¿Cómo lo solucionaste? |
| --- | --- | --- | --- | --- | --- | --- |
| 0 | `src/ejemplo/ejemplo.service.ts` | 10 | Typo | _(fila de ejemplo, bórrala) se llamaba `this.prisma.usuaro` en vez de `this.prisma.usuario`_ | _VS Code lo marcó en rojo: "Property 'usuaro' does not exist"_ | _corregí el nombre del modelo_ |
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
| 5 | | | | | | |


<!-- Agrega todas las filas que necesites -->

Modulo AUTORES: Leonardo

| # | Archivo | Línea | Tipo | ¿Qué estaba mal? | ¿Cómo lo detectaste? | ¿Cómo lo solucionaste? |
| --- | --- | --- | --- | --- | --- | --- |
| 0 | `src/ejemplo/ejemplo.service.ts` | 10 | Typo | _(fila de ejemplo, bórrala) se llamaba `this.prisma.usuaro` en vez de `this.prisma.usuario`_ | _VS Code lo marcó en rojo: "Property 'usuaro' does not exist"_ | _corregí el nombre del modelo_ |
1	src/autor/autor.controller.ts	Typo	Se utilizaba @Gett() en lugar de @Get().
2	src/autor/dto/create-autor.dto.ts	Typo	Se utilizaba @IsOptinal() en lugar de @IsOptional().
3	src/autor/autor.service.ts	Lógica	La condición de findOne() estaba invertida: lanzaba 404 cuando el autor sí existía.
4	src/autor/autor.module.ts	Terminal	Faltaba importar PrismaModule para que el módulo pudiera inyectar PrismaService.


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

Modulo Categoria: Sara

| # | Archivo | Línea | Tipo | ¿Qué estaba mal? | ¿Cómo lo detectaste? | ¿Cómo lo solucionaste? |
| ---         | ---   | ---  | ---              |                  --- |                    --- | --- |
| 1 |src/categoria/categoria.service.ts |26 |faltaba una coma |me salia en rojo |colocando la coma | |
| 2 |src/categoria/categoria.module.ts |6 |agreagar el provider | al leer el codigo |colocando el provider | |
| 3 |src/main.ts |15|falataba un parentesis |marcaba rojo |colocando el parentesis | |
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
el provider por que en un momento me paso desapercibido, hasta que me hice la pregunta de si
no faltaba un objeto dentro para el provider.
2. ¿Qué herramienta te ayudó más (editor, terminal, Swagger/Postman, tests)?
terminal
3. ¿Qué harías para evitar este tipo de errores en tus propios proyectos?
chequear dos veces para asegurarme de haber escrito  todo segun los requerimientos.
