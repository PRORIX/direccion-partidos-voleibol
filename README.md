# direccion-partidos-voleibol

## información de la aplicación

ABSOLUT VOLLEY será una aplicación accesible para todos en un partido de voleibol, servirá para controlar, dirigir y visualizar datos en un partido de voleibol (Rotaciones, puntuación, amonestaciones a los jugadores, direcciones de los equipos, ... ) Así como el control de las propias ligas, guardando los resultados de cada uno (Equipo ganador y resultado, registrando tanto los sets como los resultados de cada uno). En función del resultado de cada partido se añadirán los puntos correspondientes en la liga correspondiente de forma automática. Pero también puede ser utilizada con otros objetivos, cada usuario tendrá la funcion que justo necesita.


## Especificación de actores y operaciones

#### Federación

Los miembros de la federación crean las ligas y gestionan las mismas, los puntos de los equipos se añaden automáticamente cuando un partido termina pero, estos pueden añadir equipos en las ligas, eliminarlos, y aplicar cambios que quizás se hayan añadido de manera errónea.


#### Árbitros

Los árbitros podrán ver el estado actual del partido (Rotaciones, puntuación, amonestaciones a los jugadors, direcciones de los equipos, ... ) dado que ellos serán los que añadirán los puntos cada vez que un equipo haga un punto en el partido, y registrará todas las amonestaciones y datos necesarios del partido (Tarjetas, expulsiones, etc.). Así como dar un partido por comenzado y finalizado.


#### Entenadores

Los entrenadores podrán crear equipos en la aplicación y publicarlos, durante los partidos tendrán la posibiliad de visualizar la información del partido, y desde la aplicación tendrán el permiso de registrar la rotación inicial con la que saldrá el equipo al inicio de cada set (Tendrán la opción habilitada cuando el árbitro lo haga posible).


#### Usuarios

El resto de actores podrán solamente acceder a la información del partido, tendrán un menú donde aparecerán todos los partidos que se están jugando actualmente y accederán a la información para poder ver la puntuación de los mismos, también podrán elegir equipos como favoritos y recibirán notificaciones cada vez que un partido de su equipo favorito de comienzo.



### Operaciones por actor

#### Federación
<li>Borrar equipo</li>
<li>Crear liga</li>
<li>Gestionar liga</li>

#### Árbitro
<li>Registrar datos partido</li>
<li>Iniciar partido</li>
<li>Finalizar partido</li>
<li>Abrir disponibilidad de añadir rotaciones iniciales</li>
<li>Ver datos avanzados del partido</li>

#### Entrenador
<li>Registrar rotación inicial</li>

#### Usuario
<li>Ver partidos</li>


### Diagrama casos de uso


