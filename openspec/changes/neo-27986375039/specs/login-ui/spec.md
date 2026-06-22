## ADDED Requirements

### Requirement: Condorito illustration in login left panel
The login screen's left panel SHALL display a Condorito illustration, served from
`public/images/condorito.png` via `<img src="/images/condorito.png" />`, positioned alongside or
below the existing Uko logo within the "Hi, Welcome Back!" block.

#### Scenario: Visiting the login page on desktop
- **WHEN** a user navigates to the login page on a viewport wide enough to show the left panel
  (`lg` breakpoint or above)
- **THEN** the left panel renders the Uko logo and the Condorito illustration together inside the
  "Hi, Welcome Back!" block, styled with Tailwind utility classes consistent with the surrounding
  content (e.g. spacing/height classes similar to the existing logo image)

#### Scenario: Login form remains unaffected
- **WHEN** a user submits valid credentials on the login form
- **THEN** the authentication flow (`useAuth().login`) and redirect behavior continue to work
  exactly as before, since the Condorito illustration is a purely visual addition to the left
  panel and does not modify the form, validation schema, or `onSubmit` handler

### Requirement: Condorito asset served as a static public file
The Condorito illustration SHALL be added under `public/images/condorito.png` so it is served as
a static asset by Vite/Railway without requiring any build-time import or bundler processing.

#### Scenario: Building the app for production
- **WHEN** the project is built with `yarn build`
- **THEN** `public/images/condorito.png` is copied as-is into `dist/images/condorito.png` and
  remains reachable at `/images/condorito.png` in the deployed app, with no `vue-tsc` type errors
  introduced by the change
