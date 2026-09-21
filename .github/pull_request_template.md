<!--
Gracias contribuir a la iniciativa de OpenUTT :D
Título del PR:
  proyectos: <nombre>   → agregar o actualizar una entrada del índice
  docs: | fix: | feat:  → cualquier otro cambio del sitio
Proceso completo: https://openutt.github.io/agregar-proyecto/
-->

## Qué cambia y por qué
(Qué problema resuelve o qué mejora trae)

## Tipo de cambio
- [ ] Entrada del índice de proyectos
- [ ] Contenido (texto, páginas, imágenes)
- [ ] Diseño o configuración (layouts, menú, params)
- [ ] Corrección (bug, enlace roto, errata)

## Checklist
- [ ] El título sigue la convención (y si agrega un proyecto, empieza con `proyectos: <nombre>`)
- [ ] Solo si agrega una entrada: copié `content/proyectos/PLANTILLA/` a `content/proyectos/<slug>/index.md` y llené los campos obligatorios (estado, autores, cuatrimestre, tecnologías, repo), con `draft = false`
- [ ] Solo si agrega una entrada: `estado` es `activo`, `abandonado` o `completado`; tecnologías en minúsculas
- [ ] Solo si agrega una entrada: el repo enlazado cumple los requisitos mínimos (README, LICENSE, `.gitignore`, sin secretos)
- [ ] Sin datos personales de estudiantes ni terceros
- [ ] Sin secretos en el diff
- [ ] Actualicé `lastmod` si edité contenido que ya existía
- [ ] Si toqué layouts, menú o configuración: lo revisé con `hugo server`
- [ ] No incluí archivos generados (`public/`, `resources/`)
- [ ] Confirmo que soy autor/a del proyecto o cuento con permiso de quien lo es

<!-- Para quien revisa: comparar contra content/proyectos/PLANTILLA/ y verificar los requisitos mínimos del repo enlazado. -->

---
¿Tocas layouts, menú o configuración del sitio? Cambia el checklist por el
[checklist técnico →](?expand=1&template=pagina.md)
