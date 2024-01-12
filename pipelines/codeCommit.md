# AWS Code commit

Es un servicio adminsitrado por amazon que permite crear un repositorio estilo github para almacenar allí nuestro código, crear merge requests y en general todas las cosas que se pueden hacer en otras plataformas.

Las ventajas que puede suponer utilizar este servicio es que está dentro de nuestra cuenta de amazon y el código es completamente privado, lo cual favorece la seguridad de la aplicación.

Sin embargo para implementar cosas como pipelines de continuous integration o continuous delivery no es estrictamente necesario utilizar code commit, porque los demás servicios dentro de amazon para estos fines son integrables con Github, Gitlab etc.