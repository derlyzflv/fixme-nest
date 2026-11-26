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
| 0 | `src/ejemplo/ejemplo.service.ts` | 10 | Typo | _(fila de ejemplo, bórrala) se llamaba `this.prisma.usuaro` en vez de `this.prisma.usuario`_ | _VS Code lo marcó en rojo: "Property 'usuaro' does not exist"_ | _corregí el nombre del modelo_ |
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
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

## Reflexión final

1. ¿Qué tipo de error te costó más encontrar y por qué?
2. ¿Qué herramienta te ayudó más (editor, terminal, Swagger/Postman, tests)?
3. ¿Qué harías para evitar este tipo de errores en tus propios proyectos?
