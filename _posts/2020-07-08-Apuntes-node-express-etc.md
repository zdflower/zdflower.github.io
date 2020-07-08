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
