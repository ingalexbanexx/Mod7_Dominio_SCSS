# Mod7_Dominio_SCSS

## Estructura
- `scss/main.scss`: entrada de compilación.
- `scss/utilities/_variables.scss`: variables Sass reutilizables.
- `scss/utilities/_mixins.scss`: mixins reutilizables.
- `scss/base/_base.scss`: estilos globales.
- `scss/base/_tipografia.scss`: tipografía.
- `scss/layout/_header.scss`: encabezado y marca.
- `scss/layout/_footer.scss`: pie de página.
- `scss/layout/_nav.scss`: navegación.
- `scss/components/_buttons.scss`: botones.
- `scss/components/_cards.scss`: tarjetas y componentes repetibles.
- `scss/components/_legacy.scss`: CSS original conservado íntegro para no alterar la cascada durante la primera compilación.
- `css/styles.css`: archivo generado que siguen cargando los HTML.

## Instalar Sass
Desde la raíz del proyecto:
npm init -y
npm install --save-dev sass

## Compilar una vez
npx sass scss/main.scss css/styles.css

## Compilar en modo observación
npx sass --watch scss/main.scss:css/styles.css