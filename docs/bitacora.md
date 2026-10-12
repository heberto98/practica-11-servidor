
# Bitácora — Servidor con pruebas

## Bloque A — Permisos
Se corrigió la eliminación de avisos para que cada profesor solamente pueda borrar sus propias publicaciones. Se agregaron pruebas de permisos para comprobar los casos permitidos y rechazados.

Resultado: 14 pruebas aprobadas y 1 omitida.

## Bloque B — Publicaciones duplicadas
Se implementó el uso de Idempotency-Key para evitar que los reintentos de una misma publicación generen avisos duplicados. También se agregaron pruebas para verificar el comportamiento con claves repetidas y diferentes usuarios.

Resultado: 17 pruebas aprobadas.

## Bloque C — Imágenes huérfanas
Se implementó una función para identificar y eliminar imágenes que no están asociadas a ningún aviso y que tienen más de una hora almacenadas. Se verificó que las imágenes utilizadas y las recientes no se eliminen.

Resultado: 19 pruebas aprobadas. La ejecución manual de limpieza reportó 0 imágenes huérfanas eliminadas.

## Bloque D — Matriz de trazabilidad
Se guardó la evidencia detallada de pytest en docs/evidencia/pytest-servidor.txt y se preparó la matriz de trazabilidad en docs/matriz-trazabilidad.md.

Resultado: 19 pruebas aprobadas. Se documentaron los requisitos cumplidos, parcialmente cumplidos y pendientes.

## Pendientes
- Integrar Idempotency-Key en la aplicación Android.
- Automatizar la ejecución periódica de la limpieza de imágenes huérfanas.
- Verificar los reportes de pruebas de Android y sus evidencias.
