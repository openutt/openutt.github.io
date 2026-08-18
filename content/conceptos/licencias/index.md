+++
date = '2026-08-15T22:02:14-07:00'
draft = false
title = 'Licencias Open Source'
description = 'Lista de licencias open source y guía para elegir la adecuada para tu proyecto.'
+++

## Licencias Aprobadas por la OSI

{{< alert "edit" >}}

Retomado de [Open Source Licenses](https://opensource.org/licenses)

{{< /alert >}}

La Open Source Initiative enlista una gran cantidad de licencias que han sido aprobadas por ellos las cuales cumplen todas las características de [[Definición Oficial Open Source]]. En la categoría de _“Populares o con Comunidad Fuerte“,_ que muy probablemente han llegado a encontrarse en algún proyecto, encontramos:

| License Name | SPDX ID |
| --- | --- |
| [Apache License, Version 2.0](https://opensource.org/license/apache-2-0) | Apache-2.0 |
| [Common Development and Distribution License 1.0](https://opensource.org/license/cddl-1-0) | CDDL-1.0 |
| [Eclipse Public License version 2.0](https://opensource.org/license/epl-2-0) | EPL-2.0 |
| [GNU General Public License version 2](https://opensource.org/license/gpl-2-0) | GPL-2.0 |
| [GNU General Public License version 3](https://opensource.org/license/gpl-3-0) | GPL-3.0 |
| [GNU Lesser General Public License version 2.1](https://opensource.org/license/lgpl-2-1) | LGPL-2.1 |
| [GNU Lesser General Public License version 3](https://opensource.org/license/lgpl-3-0) | LGPL-3.0 |
| [GNU Library General Public License version 2](https://opensource.org/license/lgpl-2-0) | LGPL-2.0 |
| [Mozilla Public License 2.0](https://opensource.org/license/mpl-2-0) | MPL-2.0 |
| [The 2-Clause BSD License](https://opensource.org/license/bsd-2-clause) | BSD-2-Clause |
| [The 3-Clause BSD License](https://opensource.org/license/bsd-3-clause) | BSD-3-Clause |
| [The MIT License](https://opensource.org/license/mit) | MIT |

Aun así, se ve un poco confuso cuál usar o sus diferencias. En el 90% de las ocasiones, lo que principalmente importa es el **copyleft**

## Copyleft

Según la _Free Software Fundation_

> El copyleft es un método general para liberar un programa u otro tipo de trabajo (_en el sentido de libertad, no de gratuidad_), que requiere que **todas las versiones modificadas y extendidas sean también libres**. - [_¿Qué es el copyleft?_](https://www.gnu.org/licenses/copyleft.es.html)

Es decir, el **copyleft** es una característica de licencias en el cual impide que alguien pueda modificar un software con licencia Open Source, hacerlo privado y sacar provecho de él.

Las licencias _copyleft_ obliga a los _forks_ de un proyecto open source **también sean Open Source** si es que van a distribuir su fork/modificación. Un gran ejemplo es Linux.

## ¿Cual licencia usar?

Hay una gran cantidad de licencias OS para cada caso específico. Para la mayoría de casos, este diagrama simplifica cual usar

{{< mermaid >}}
flowchart TD
    A[¿Quieres impedir que cualquiera pueda crear versiones privativas?]

    A -->|No| B[¿Necesitas protección explícita de patentes?]

    B -->|No| MIT(MIT)
    B -->|Sí| APACHE(Apache License 2.0)

    A -->|Sí| C[¿El software se usará principalmente como servicio web/SaaS?]

    C -->|No| GPL(GPLv3)
    C -->|Sí| AGPL(AGPLv3)

    MIT --> MITDESC[Máxima simplicidad y adopción]
    APACHE --> APACHEDESC[Permisiva + protección de patentes]
    GPL --> GPLDESC[Copyleft para software distribuido]
    AGPL --> AGPLDESC[Copyleft también para SaaS]
{{< /mermaid >}}
