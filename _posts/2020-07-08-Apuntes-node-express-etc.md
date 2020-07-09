---
layout: post
title: Apuntes varios sobre Node, Express y todo lo demás
date: 2020-07-08
---
# Apuntes varios sobre Node, Express y todo lo demás

## Packaje.json

### Dependencias y versiones 

#### Semantic versioning

    "somepackage" : 1.2.0

Significa que la versión **major** es la 1, que la **minor** es la 2 y la de "patch" es la 0.

Los números de la **major** cambian cuando deja de haber compatibilidad con versiones anteriores. Los de la **minor** aumentan cuando se incorporan características sin perder compatibilidad hacia atrás. Y los de la versión **patch** se incrementan cuando se corrigen bugs manteniendo la compatibilidad previa.

    "somepackage" : ~1.2.0

El **~** indica que se instale la versión **patch** más actual.

    "somepackage" : ^1.2.0

El **^** indica que se instale la versión **minor** más actual.

Fuente: *Managing packages with npm - FreeCodeCamp [https://www.freecodecamp.org/learn/apis-and-microservices/managing-packages-with-npm/]*


## Protección contra ciertas vulnerabilidades - Uso de HelmetJS

Contra "Cross-site scripting" (XSS):

    helmet.xssFilter()

Contra "[MIME][mime] sniffing" o husmeo de tipo de medio:

    helmet.noSniff()

MIME es un acrónimo para "Multipurpose Internet Mail Extensions".

Contra la exposición en el header de la tecnología en uso:

    helmet.hidePoweredBy()

O mentir acerca de la tecnología usada:

    helmet.hidePoweredBy({ setTo: 'PHP 4.2.0' })

Contra "Clickjacking attacks":

Por ejemplo:

    helmet.frameguard({ action: 'sameorigin' })

Contra DNS prefetching por parte del navegador:

    helmet.dnsPrefetchControl()


[mime]: https://en.wikipedia.org/wiki/Media_type

[HelmetJS Docs](https://helmetjs.github.io/docs/)
