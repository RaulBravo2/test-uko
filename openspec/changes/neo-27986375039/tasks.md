## 1. Asset

- [x] 1.1 Agregar el archivo de imagen en `public/images/condorito.png` (PNG, fondo transparente
      si es posible, tamaño razonable para web, p.ej. <= 200px de alto).

## 2. UI

- [x] 2.1 En `src/pages/sessions/Login.vue`, agregar `<img src="/images/condorito.png" ... />`
      dentro del bloque izquierdo (`Hi, Welcome Back!`), junto/debajo del logo de Uko
      (`<img src="/logos/uko.png" ... />`).
- [x] 2.2 Aplicar clases utilitarias de Tailwind consistentes con el resto del bloque (alto,
      margen, comportamiento responsive) y un `alt` descriptivo (p.ej. `alt="Condorito"`).
- [x] 2.3 Verificar visualmente que el logo de Uko, el texto y la nueva ilustración conviven sin
      solaparse en los breakpoints `lg`/`xl`.

## 3. Verificación

- [x] 3.1 Ejecutar `yarn build` (type-check + build) y confirmar que termina sin errores.
- [x] 3.2 Confirmar que `dist/images/condorito.png` existe tras el build.
