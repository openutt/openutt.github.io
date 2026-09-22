# Contribuir a OpenUTT

Gracias por querer contribuir a la iniciativa de OpenUTT :D
Para contribuir a este repositorio hay distintas maneras y cosas a tener en cuenta.

## Antes de empezar

- Cuenta de [GitHub](https://github.com) y `git` configurado.
- [Hugo **extended** ≥ 0.158](https://gohugo.io/installation/) y [Go](https://go.dev/) para construir el sitio en tu máquina.
- Comandos del día a día:

  ```bash
  hugo server -D        # dev en http://localhost:1313, con recarga en vivo
  hugo --gc --minify    # build completo local; el CI corre solo hugo --minify
  ```

## Dos caminos de contribución

### 1. Sumar o actualizar un proyecto del índice

El proceso completo (plantilla, campos y PR) está en **[Agregar un proyecto](https://openutt.github.io/agregar-proyecto/)**.
Requisitos mínimos del repositorio enlazado: README funcional, LICENSE, `.gitignore` sin claves y sin secretos en el historial.

### 2. Cambiar el sitio (contenido, diseño o configuración)

1. Crea una rama con nombre descriptivo (`docs-…`, `fix-…`, `feat-…`).
2. Haz el cambio y verifícalo en local con `hugo server` (página afectada, claro y oscuro).
3. Commit con prefijo conventional en inglés e imperativo: `docs:`, `fix:`, `feat:`, `refactor:`.
4. Abre el Pull Request contra `main`, con el título igual al del commit. La [plantilla de PR](.github/pull_request_template.md) default se carga sola; si tocaste layouts, menú o configuración, cambia al checklist técnico desde el enlace del final de esa plantilla.
5. Espera la revisión y el merge: al mergear, GitHub Actions construye y publica el sitio solo. Nunca edites `gh-pages` ni `public/` a mano.

## Convenciones del sitio
- **Idioma**: español en todo el contenido.
- **Front matter TOML** (`+++`) con `date` y `lastmod`; `_index.md` para secciones y listas, `index.md` para páginas y bundles (una carpeta siempre termina en `index.md`).
- **Taxonomías reservadas**: `estado`, `cuatrimestre` y `tecnologias` existen solo en el índice de proyectos; no reutilices esos campos en otras secciones.
- **Búsqueda**: solo indexa el texto renderizado (título, description, cuerpo) — lo que deba encontrarse va en la description o en el cuerpo, no en metadatos.
- **Shortcodes existentes**: reutiliza `pinned`, `proyecto-meta` y `wide-image` antes de crear algo nuevo.
- **Nunca edites** archivos generados: `public/`, `resources/`, `.hugo_build.lock`.
- **Sin datos personales** de estudiantes ni terceros, y **sin secretos** en el diff.

## Checklist técnico (layouts, menú, configuración)
- `hugo --gc --minify` compila sin errores (Hugo **extended** ≥ 0.158).
- Revisado con `hugo server` en claro y en oscuro.
- Si toca layouts o menú: probado en angosto (<640px) y ancho (≥640px).
- Sin clases Tailwind concatenadas en templates o shortcodes (el theme solo emite clases literales).
- Sin cambios en archivos generados.
- 
## Reglas de revisión

Alguien del equipo de OpenUTT revisará tu Pull Request, agregará comentarios y solicitará cambios si es necesario y aprobará el merge.

## Licencia
Al contribuir, aceptas que tu aportación se publique bajo la [licencia MIT](LICENSE) del repositorio.
