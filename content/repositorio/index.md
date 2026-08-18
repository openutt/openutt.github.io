+++
date = '2026-06-15'
lastmod = '2026-08-16'
draft = false
title = 'Plan de repositorio'
description = 'Plan para la gestión de repositorios de OpenUTT.'
url = '/propuesta/repositorio/'
+++
> [OpenUTT Github Org](https://github.com/openutt)
# Enfoque

Para esta iniciativa, es necesario tener un **lugar público donde** se guarden y den a conocer los proyectos que forman parte de OpenUTT. El enfoque se divide en **tres niveles** que no se excluyen entre sí: los proyectos importantes viven dentro de la organización, mientras que la mayoría de los proyectos estudiantiles se dan a conocer a través de un índice público.

## Niveles

### 1. Repositorios de la organización

Proyectos **internos**, creados **por y para la UTT**, que OpenUTT mantiene directamente (transferidos o creados dentro de la org).

- Software que usa la universidad (sistemas internos)
- Proyectos importantes y activos

**Ventajas:**
- La organización da una buena impresión al tener grandes proyectos
- Facilidad para buscar o analizar proyectos

### 2. Índice / catálogo de proyectos

Un **catálogo público** que enlista los proyectos de **otros equipos y estudiantes**, enlazándolos a sus cuentas **sin moverlos** de donde viven.

- Da visibilidad a todos los proyectos
- No requiere que el estudiante transfiera su repositorio (solo un enlace)
- Los proyectos abandonados se conservan como referencia para reutilizarlos

**Ventajas:**
- Organización se ve viva
- Equipos ven sus proyectos siendo parte de _algo_ dentro de la universidad
- Muchos proyectos para poder investigar y estudiar

### 3. Portal web (GitHub Pages)

El índice se publica como un **sitio web** (GitHub Pages) para que cualquiera pueda ver y explorar los proyectos sin necesidad de una cuenta.

- Accesible desde un navegador
- Generado desde el mismo índice (una sola fuente de verdad)

## Estructura de la organización

```
openutt/
├── .github/              ← README de la org (puerta de entrada)
├── (proyectos internos)  ← software de y para la UTT
└── portal/               ← índice + GitHub Pages
```

## Criterio de promoción

Un proyecto puede pasar del **índice** a la **organización** cuando:
- La universidad lo usa de forma real, o
- Lo mantiene más de una persona de forma activa

---

Se decidió usar _Github_ debido a su gran uso en el mercado y estándar en alojar proyectos Open Source.
