# Mod7_Dominio_SCSS — arquitectura inicial segura

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
```bash
npm init -y
npm install --save-dev sass
```

## Compilar una vez
```bash
npx sass scss/main.scss css/styles.css
```

## Compilar en modo observación
```bash
npx sass --watch scss/main.scss:css/styles.css
```

## Importante
Esta es una etapa de transición segura: conserva la hoja original completa para que el diseño no cambie al empezar a usar Sass. Para que la rúbrica considere terminada la refactorización modular, migrá progresivamente bloques de `_legacy.scss` a los parciales correspondientes, eliminando cada bloque del original al moverlo y verificando la salida después de cada cambio. No dejes reglas duplicadas en ambos lugares.
