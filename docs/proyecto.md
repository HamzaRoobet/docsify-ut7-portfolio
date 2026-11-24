# Proyecto: Portfolio técnico con Docsify y GitHub Pages

Este sitio es en sí mismo el proyecto de la actividad **A72/A73 - Docsify** del módulo SIS.

## Herramientas usadas

| Herramienta | Uso |
|---|---|
| Node.js | Entorno de ejecución para pnpm y docsify-cli |
| pnpm | Gestor de paquetes |
| docsify-cli | Generación y servidor local del sitio |
| GitHub Pages | Publicación del sitio estático |
| GitHub Actions | Despliegue automático al hacer `push` a `main` |

```bash
docsify init ./docs
docsify serve ./docs
```

> [!TIP]
> El sitio se sirve en local en `http://localhost:3000` mientras se edita, y se publica automáticamente en GitHub Pages cada vez que se hace push a la rama `main`.
