---
title: Encontrada vulnerabilidad en Postgres
link: https://www.postgresql.org/support/security/CVE-2024-0985/
toc: false
tags:
    - anuncios
---

Se descubre una vulnerabilidad en postgresql que sigo sin poder traducir correctamente. Textualmente dice:
> Late privilege drop in REFRESH MATERIALIZED VIEW CONCURRENTLY in PostgreSQL allows an object creator to execute arbitrary SQL functions as the command issuer.

Que básicamente viene a decir que posibilita a un atacante el ejecutar funciones sql arbitraria, al menos según el post original de la gente de postgres, aunque otros parecen referir que podría ejecutarse código sql arbitrario.

Como sea, las versiones afectadas son de las `12` a las `15`. Para referencia, `Debian 12` usa la versión `15` y `Debian 11` usa la `14`.

La vulnerabilidad fue encontrada el 8 de febrero, Debian publicó ayer 14 de febrero los fixes:
* [\[SECURITY\] \[DSA 5622-1\] postgresql-13 security update](https://lists.debian.org/debian-security-announce/2024/msg00029.html)
* [\[SECURITY\] \[DSA 5623-1\] postgresql-15 security update](https://lists.debian.org/debian-security-announce/2024/msg00030.html)

Como siempre, la recomendación es tener configurados los repositorios security en Debian y revisar siempre por actualizaciones

La noticia original puede leerse [acá](https://www.postgresql.org/support/security/CVE-2024-0985/)