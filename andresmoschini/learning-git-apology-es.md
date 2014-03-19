---
layout: default
title: Apología del aprendizaje de Git
---

Git es muy poderoso y está bueno poder _sacarle el jugo_.

Hay varias experiencias de proyectos en los que las operaciones _"avanzadas"_ (nótese las comillas) las hacía un grupo limitado de personas, eso suele terminar en la generación de un cuello de botella. Esa es una de las razones por la que es importante que todos entendamos Git.

Por otro lado, Git es muy flexible, nos da una libertad mucho más amplia que otros sistemas de control de versiones, nos permite trabajar más cómodos, más felices. De los que trabajaron con TFS, ¿quién no sufrió esperando que responda? ¿quién no maldijo al no poder aplicar un _shelve_ en un _branch_ distinto que el original? 

_GitHub_ además nos da acceso a una comunidad de software, donde nosotros podemos compartir nuestros proyectos y participar en proyectos de otros.

Aprender a usar Git puede no ser tan fácil, hay muchas formas de hacer lo mismo, por eso yo no confío en que se pueda dar una capacitación muy efectiva. Nosotros estamos acostumbrados a aprender, hagámoslo ahora.

Mis recomendaciones:

* Es más importante entender el "lenguaje de Git" (su forma de modelar la historia) y sus posibilidades, que los comandos o como hacer cosas. Si sabemos que algo se puede hacer, es fácil luego descubrir como hacerlo. 
* Recordar que con Git nunca es necesario decir "Deberías haber hecho XXX antes de YYY."
* Una forma práctica de aprender es: mirar el gráfico actual; imaginar el gráfico que uno desea obtener; aplicar las operaciones; comprobar el gráfico resultante; si no es el deseado, analizar las razones e intentarlo nuevamente.
* Más allá de que usemos un cliente gráfico, tratar de expresarnos en términos de comandos, de esa forma es más fácil compartir nuestro aprendizaje.
* No estoy muy seguro de que esto sea cierto para todos, pero creo que en general, utilizar [GitHub for Windows](/migration-to-git/3-working-with-git/git-clients.html#github_for_windows) no es una buena idea para quien intenta aprender Git: No muestra el gráfico, realiza operaciones por detrás y además no soporta otros _remotes_ más que `origin`. Creo que [Git Extensions](/migration-to-git/3-working-with-git/git-clients.html#git_extensions) es una buena opción.