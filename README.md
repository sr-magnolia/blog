# blog

Sitio personal construido con [Hugo](https://gohugo.io/) y el tema [Blowfish](https://blowfish.page/).

## Requisitos

- [Hugo](https://gohugo.io/installation/) (versión extendida recomendada)
- Git

## Instalación

```bash
git clone --recurse-submodules <url-del-repo>
cd blog
```

## Uso

### Servidor local

```bash
hugo server
```

Abre `http://localhost:1313` en tu navegador. Los cambios se reflejan en tiempo real.

### Crear un nuevo post

```bash
hugo new posts/nombre-del-post.md
```

El archivo se crea en `content/posts/` con el front matter básico. Edítalo y cambia `draft: true` a `draft: false` cuando esté listo para publicar.

### Generar el sitio

```bash
hugo
```

El sitio estático se genera en la carpeta `public/`.

## Estructura

```
content/
  posts/       # artículos del blog
  menu/        # páginas estáticas (acerca de, etc.)
config/
  _default/    # configuración principal (hugo.toml, params.toml, menu.toml)
assets/
  img/         # imágenes del sitio
themes/
  blowfish/    # tema del sitio (submódulo git)
```

## Despliegue

El sitio se despliega automáticamente en AWS Amplify al hacer push a la rama principal. La configuración está en `amplify.yml`.
