# Reflexión de decisión CSS

Decidimos usar CSS Grid (`grid-template-columns: repeat(2, 1fr)` y luego
`repeat(3, 1fr)`) para la cuadrícula de "Nuestra solución", en vez de
Flexbox con `flex-wrap`, aunque al principio Flexbox parecía más simple.
La razón fue el comportamiento cuando las tres tarjetas tienen alturas de
contenido distintas: con `flex-wrap`, cada fila se ajusta de forma
independiente y las columnas no quedan alineadas verticalmente si el
texto de una tarjeta es más largo que el de las otras. Grid, en cambio,
define explícitamente las columnas de toda la cuadrícula, así que las
tres tarjetas quedan alineadas sin fijar una altura manual ni agregar
JavaScript para igualarlas. También usamos un enfoque mobile-first con
`min-width` en las media queries, en vez de `max-width`, porque así los
estilos base ya son el diseño móvil, y cada breakpoint solo agrega lo
que cambia en vez de sobrescribir reglas más específicas.