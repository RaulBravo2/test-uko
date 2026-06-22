# Add Condorito illustration to Login left panel

## Why

El pedido de @rbravomillacaris es decorar el panel izquierdo de la pantalla de login
(`src/pages/sessions/Login.vue`, bloque "Hi, Welcome Back!") con una ilustración de Condorito,
junto al logo de Uko, para darle un toque distintivo/local a la pantalla de bienvenida sin tocar
el flujo de autenticación.

## What Changes

- Agregar un asset estático `public/images/condorito.png` (illustration de Condorito) siguiendo
  la convención existente de `public/images/illustration/` para imágenes servidas directamente
  por Vite/Railway.
- Modificar `src/pages/sessions/Login.vue` para renderizar `<img src="/images/condorito.png" ... />`
  dentro del bloque izquierdo (`Hi, Welcome Back!`), debajo/junto al logo de Uko existente
  (`<img src="/logos/uko.png" ... />`), usando clases utilitarias de Tailwind consistentes con el
  resto del bloque (margenes, tamaño responsive) y sin alterar el formulario de login ni la lógica
  de `useAuth`.
- No se modifica ninguna ruta, store, composable ni el mock de API: es un cambio puramente visual
  en una página existente.

## Impact

- Affected specs: `login-ui` (nueva capability, no existía spec previa para esta pantalla).
- Affected code: `src/pages/sessions/Login.vue`, nuevo asset en `public/images/condorito.png`.
- Sin impacto en autenticación, rutas, stores ni mocks.
