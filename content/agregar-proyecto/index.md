+++
title = 'Agregar un proyecto'
description = 'Cómo sumar tu proyecto cuatrimestral al índice de OpenUTT.'
draft = false
+++

# Agregar un proyecto

Si quieres que tu proyecto aparezca en el [índice](/proyectos/), sigue este proceso.

## Estados

- **Activo**: se está desarrollando actualmente.
- **Completado**: terminó su ciclo y cumplió sus requisitos.
- **Abandonado**: se conserva como referencia para que otra generación lo retome.

El estado es obligatorio y lo eliges tú — un proyecto ya abandonado también puede entrar.

## Flujo

1. Copia la carpeta [PLANTILLA](https://github.com/openutt/openutt.github.io/tree/main/content/proyectos/PLANTILLA) a `content/proyectos/<slug>/index.md` (en GitHub: fork + Add file, o edición web) y completa los campos: nombre, autores, cuatrimestre, tecnologías, estado, repo, demo (si aplica) y una descripción breve.
2. Abre un PR a [openutt/openutt.github.io](https://github.com/openutt/openutt.github.io) con título `proyectos: <nombre>`.
3. Revisamos que el repo enlazado cumpla los requisitos mínimos (abajo) y lo mergeamos.
4. Al mergear, el sitio se regenera y el proyecto aparece en el índice.
5. Cambios de estado posteriores (p. ej. al abandonarse) son PRs igual de simples.

## Requisitos de ingreso (por proyecto)

- README con qué es el proyecto y cómo levantarlo (instalación + comandos).
- LICENSE definida (estándar del índice: MIT).
- `.gitignore` que excluya `.env`, claves y artefactos locales.
- Sin secretos en el historial (si el repo fue privado antes, revisar y rotar lo filtrado).
- Entrada en el índice con todos los campos de la plantilla.
