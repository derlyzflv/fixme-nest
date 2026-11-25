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
|---|---|---|---|---|---|---|
| 0 | `src/ejemplo/ejemplo.service.ts` | 10 | Typo | Fila de ejemplo, eliminarla. | VS Code lo marcó en rojo. | Corregí el nombre del modelo. |
| 1 | `src/libro/libro.service.ts` | — | Sintaxis | No se accedía correctamente al modelo Libro de Prisma. | Al revisar el código, vi que el nombre utilizado no era el correcto. | Cambié el nombre por el correcto para que funcionara. |
| 2 | `src/libro/libro.service.ts` | — | Lógica | No se comprobaba que el autor y la categoría existieran. | Revisando el código, me di cuenta de que faltaba comprobar esos datos. | Agregué una comprobación antes de guardar el libro. |
| 3 | `src/libro/libro.service.ts` | — | Lógica | No se evitaba que un libro tuviera el mismo ISBN que otro. | Revisando la parte donde se registran y actualizan los libros. | Agregué una validación para evitar ISBN repetidos. |
| 4 | `src/libro/libro.controller.ts` | — | Sintaxis | Los ID no se validaban correctamente. | Al revisar las rutas del controlador, vi que faltaba validar los ID. | Agregué una validación para asegurar que fueran números enteros. |
| 5 | `src/libro/dto/create-libro.dto.ts` | — | Lógica | Faltaban validaciones en los datos del libro. | Revisando el DTO, vi que algunos datos no tenían las validaciones necesarias. | Agregué validaciones para comprobar que los datos fueran correctos. |

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
|---|---|---|---|---|---|---|
| 0 | `src/ejemplo/ejemplo.service.ts` | 10 | Typo | Fila de ejemplo, eliminarla. | VS Code lo marcó en rojo. | Corregí el nombre del modelo. |
| 1 | `src/prestamo/prestamo.service.ts` | — | Lógica | El conteo de préstamos activos estaba incorrecto. | Al revisar el código, vi que contaba los préstamos que ya habían sido devueltos. | Cambié la condición para contar solo los préstamos que no se han devuelto. |
| 2 | `src/prestamo/prestamo.service.ts` | — | Lógica | La consulta de préstamos vencidos estaba incorrecta. | Revisando el código, vi que la fecha se estaba comparando de manera incorrecta. | Cambié la condición para buscar los préstamos cuya fecha límite ya pasó y que aún no se han devuelto. |
| 3 | `src/prestamo/utils/fechas.ts` | — | Lógica | El cálculo de fechas del préstamo estaba incorrecto. | Revisando las funciones que calculan y revisan las fechas del préstamo. | Corregí el cálculo de la fecha límite y la forma de comprobar si está vencido. |
| 4 | `src/prestamo/prestamo.service.ts` | — | Lógica | No se comprobaba correctamente si había libros disponibles. | Revisando cómo se registraba un préstamo, vi que faltaba comprobar el stock. | Agregué una comprobación para evitar prestar libros cuando no hay disponibles. |
| 5 | `src/prestamo/prestamo.service.ts` | — | Lógica | Al devolver un libro, no se actualizaban correctamente los datos. | Revisando el código de devolución, vi que faltaba actualizar el préstamo y el stock. | Agregué la actualización de la devolución y del stock del libro. |
| 6 | `src/prestamo/prestamo.service.ts` | — | Lógica | No se respetaba el límite de préstamos activos por socio. | Revisando el registro de préstamos, vi que faltaba comprobar el límite. | Agregué una validación para permitir máximo 3 préstamos activos por socio. |
| 7 | `src/prestamo/prestamo.controller.ts` | — | Sintaxis | Los ID de las rutas no se validaban correctamente. | Revisando el controlador, vi que faltaba validar los ID recibidos. | Agregué una validación para que los ID fueran números enteros. |
| 8 | `src/prestamo/prestamo.controller.ts` | — | Sintaxis | La ruta de préstamos vencidos podía confundirse con otras rutas. | Revisando las rutas del controlador, vi que era necesario acomodarlas. | Coloqué la ruta de vencidos antes de la ruta que recibe un ID. |
| 9 | `src/prestamo/prestamo.service.ts` | — | Lógica | Los préstamos no se mostraban ordenados por fecha. | Revisando la consulta que muestra todos los préstamos. | Agregué el orden para mostrar primero los préstamos más recientes. |
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