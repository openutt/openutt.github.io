+++
date = '2026-08-17T22:00:26-07:00'
draft = false
title = 'Derechos de autor en el Open Source'
+++

Cuando alguien contribuye código a un proyecto open source, **mantiene los derechos de autor sobre su código**. La licencia del proyecto (MIT, Apache, GPL, etc.) otorga permisos a otros, pero no transfiere la propiedad. Esto tiene implicaciones importantes para la gobernanza del proyecto.


## ¿Qué pasa con el código de un contributor?

- El contributor **es dueño** de sus contribuciones por defecto (en la mayoría de jurisdicciones, incluyendo EE.UU. y México)
- La licencia del proyecto le da al proyecto el derecho de **usar, modificar y redistribuir** ese código, pero no le quita la autoría
- El contributor **puede relicenciar** su propio código bajo otra licencia simultáneamente (licencia dual)
- Si el contributor trabajó para una empresa, el **empleador** puede ser el titular del copyright (varía por jurisdicción)

> En la mayoría de jurisdicciones (ej. EE.UU.), cuando los desarrolladores crean software como parte de sus labores, el copyright pertenece al empleador, no al individuo.
> — [FINOS: CLAs and DCOs](https://osr.finos.org/docs/bok/artifacts/clas-and-dcos)


## Sin CLA ni DCO: riesgos legales

Si un proyecto **no tiene** un CLA ni DCO, no hay evidencia documentada de que el contributor dio permiso para usar su código bajo la licencia del proyecto. Esto significa:

- **El autor puede exigir la remoción** de su código en cualquier momento
- **Sin licencia, el código es propiedad exclusiva** del autor por defecto — incluso si está publicado en GitHub
- No hay forma de demostrar consentimiento ante una disputa legal
- La carga de la prueba recae en el proyecto

> Sin una licencia o acuerdo, las contribuciones son propiedad exclusiva de sus autores. Nadie — ni siquiera el mantenedor del proyecto — puede usar, copiar, distribuir o modificar esas contribuciones.
> — [Open Source Guides: The Legal Side of Open Source](https://opensource.guide/legal/)


## DCO (Developer Certificate of Origin)

Mecanismo **ligero** introducido por la Linux Foundation en 2004. El contributor firma su commit con un `Signed-off-by:` certificando que tiene derecho a enviar el código.

**Cómo funciona:**

```bash
git commit -s -m "feat: mi contribución"
# Resultado en el commit:
# Signed-off-by: Juan Pérez <juan@email.com>
```

**Qué implica:**

- El contributor certifica que es su creación original o que tiene licencia para enviarla
- **No cede derechos** — solo garantiza que no está plagiando
- Es de buena fe y confianza comunitaria
- No requiere abogado ni documento legal separado

**Lo usa:** Linux kernel, Kubernetes, Docker, GitLab, Chef

> El DCO es un mecanismo ligero que dice: "Sí, tengo derecho a enviar esto, y entiendo que lo usarán". Solo requiere firmar el commit de git. No necesita leer ni entender un documento legal extenso.
> — [Opensource.com: CLA vs DCO](https://opensource.com/article/18/3/cla-vs-dco-whats-difference)


## CLA (Contributor License Agreement)

Mecanismo **formal** donde el contributor firma un contrato legal antes de contribuir. No es estandarizado — varía entre proyectos.

**Dos tipos principales:**

- **ICLA (Individual):** el contributor firma como persona
- **CCLA (Corporate):** la empresa firma en nombre de sus empleados

**Qué puede incluir:**

- Cesión de copyright al proyecto/organización
- Licencia irrevocable para usar el código
- Renuncia a reclamaciones por patentes
- Permiso para relicenciar el código en el futuro

**Lo usan:** Apache Software Foundation, Google, Microsoft, Facebook/Meta, Django

> Las CLAs pueden otorgar al proyecto el derecho de relicenciar el código después. Esto puede ser útil si la licencia actual resulta inadecuada y no puedes contactar a las cientos de personas que contribuyeron. Por supuesto, también existe el riesgo de que el proyecto tome una dirección que los contributors consideren inaceptable.
> — [Opensource.com: CLA vs DCO](https://opensource.com/article/18/3/cla-vs-dco-whats-difference)


## Comparativa

| Aspecto | Sin CLA/DCO | DCO | CLA |
|---|---|---|---|
| **Barrier de entrada** | Ninguna | Mínima (sign-off) | Alta (documento legal) |
| **Protección del proyecto** | Ninguna | Moderada | Alta |
| **El contributor cede derechos** | No | No | Depende del CLA |
| **Permite relicenciar** | No | No | Sí (si el CLA lo incluye) |
| **Evidencia de consentimiento** | No | Sí (en git) | Sí (contrato firmado) |
| **Costo administrativo** | Cero | Bajo | Alto (abogados, seguimiento) |
| **Riesgo de remoción de código** | Alto | Bajo | Mínimo |


## Casos reales de disputas

| Caso | Qué pasó |
|---|---|
| **Elastic vs AWS (2021)** | Amazon tomó código Elasticsearch (Apache 2.0) y creó OpenSearch. Elastic cambió la licencia a SSPL por venganza |
| **MongoDB vs AWS (2019)** | MongoDB cambió de AGPL a SSPL cuando AWS lanzó Atlas como servicio competitivo |
| **CentOS vs SCO** | SCO demandó a Red Hat alegando que código Unix fue incluido ilegalmente |

Estos casos muestran que incluso con licencias claras, las disputes pueden surgir. Sin un CLA/DCO, el proyecto está aún más expuesto.


## Fuentes

1. [Open Source Guides — The Legal Side of Open Source](https://opensource.guide/legal/) — Guía oficial de GitHub sobre licencias y aspectos legales
2. [Opensource.com — CLA vs DCO: What's the difference?](https://opensource.com/article/18/3/cla-vs-dco-whats-difference) — Comparativa por Ben Cotton (Fedora/Red Hat)
3. [FINOS — CLAs and DCOs](https://osr.finos.org/docs/bok/artifacts/clas-and-dcos) — Análisis técnico de la Open Source Readiness Board
4. [Developer Certificate of Origin — Texto oficial v1.1](https://developercertificate.org/)
5. [Apache Software Foundation — ICLA](https://www.apache.org/licenses/icla.pdf) — Ejemplo de CLA individual
