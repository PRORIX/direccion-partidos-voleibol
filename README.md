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

![Diagrama inicial drawio](https://github.com/user-attachments/assets/aff375c6-7172-4ca8-98b2-aec6a2963349)

### Actores

|  Actor | Federación  |
|---|---|
| Descripción  | Miembro de la federación de voleibol |
| Características  | Tienen altos permisos en la app |
| Relaciones |   |
| Referencias | Borrar equipo, crear liga, borar liga, gestionar liga, ver partidos |   
|  Notas |  _Notas adicionales_ |
| Autor  | prorix |
|Fecha | 11.11.24 |

|  Actor | Árbitro  |
|---|---|
| Descripción  | Cuerpo del arbitraje de las ligas |
| Características  | Tiene los permisos necesarios para gestionar un partido |
| Relaciones | Entrenador  |
| Referencias | Registrar datos partido, iniciar partido, finalizar partido, abrir disponibilidad de añadir rotaciones iniciales, ver datos avanzados de los partidos, ver partidos |   
|  Notas |  _Notas adicionales_ |
| Autor  | prorix |
|Fecha | 11.11.24 |

|  Actor | Entrenador  |
|---|---|
| Descripción  | Creador de equipos de voleibol |
| Características  | Puede crear equipos y tener pequeños permisos en los partidos |
| Relaciones | Arbitro |
| Referencias | Registrar rotación inicial, crear equipo, ver partidos |   
|  Notas |  _Notas adicionales_ |
| Autor  | prorix |
|Fecha | 11.11.24 |

|  Actor | Usuario  |
|---|---|
| Descripción  | Usuario común de la app |
| Características  | Usuario sin permisos de la app |
| Relaciones |  |
| Referencias | ver partidos |   
|  Notas |  _Notas adicionales_ |
| Autor  | prorix |
|Fecha | 11.11.24 |


### Casos de uso

|  Caso de Uso	CU | Borrar equipo  |
  |---|---|
  | Fuentes  | _Documento que sustenta el caso de uso_  |
  | Actor  | Federación |
  | Descripción | Borra un equipo que no deba existir más |
  | Flujo básico | 1. Acceder al menú de administración, 2. Localizar el equipo, 3. Rellenar el formulario de eliminación.  |
  | Pre-condiciones | El equipo debe ser eliminado con motivos justificantes. |  
  | Post-condiciones  | El equipo es eliminado de todas las ligas y competencias a las que pertenece |  
  |  Requerimientos | No se puede eliminar un equipo sin motivo aparente. |
  |  Notas |  _Notas adicionales_ |
  | Autor  | prorix |
  |Fecha | 11.11.24 |

  |  Caso de Uso	CU | Crear liga  |
  |---|---|
  | Fuentes  | _Documento que sustenta el caso de uso_  |
  | Actor  | Federación |
  | Descripción | Se crea una nueva liga |
  | Flujo básico | 1. Acceder al menú de administración, 2. Rellenar el formulario de creación de liga. |
  | Pre-condiciones | Se necesita una liga nueva |  
  | Post-condiciones  | La liga se añade al sistema |  
  |  Requerimientos | La liga debe tener inicialmente al menos 5 equipos |
  |  Notas |  _Notas adicionales_ |
  | Autor  | prorix |
  |Fecha | 11.11.24 |

  |  Caso de Uso	CU | Borrar liga  |
  |---|---|
  | Fuentes  | _Documento que sustenta el caso de uso_  |
  | Actor  | Federación |
  | Descripción | Se borra una liga |
  | Flujo básico | 1. Acceder al menú de administración, 2. Rellenar el formulario de eliminación de liga. |
  | Pre-condiciones | Se necesita eliminar una liga |  
  | Post-condiciones  | La liga se elimina del sistema |  
  |  Requerimientos | La liga debe tener menos de 8 equipos |
  |  Notas |  _Notas adicionales_ |
  | Autor  | prorix |
  |Fecha | 11.11.24 |

  |  Caso de Uso	CU | Gestionar liga  |
  |---|---|
  | Fuentes  | _Documento que sustenta el caso de uso_  |
  | Actor  | Federación |
  | Descripción | Gestión general de la liga (Añadir equipos, quitarlos, etc.) |
  | Flujo básico | 1. Acceder al menú de administración, 2. Acceder a la liga, 3. Acceder al sistema de gestión. |
  | Pre-condiciones |  |  
  | Post-condiciones  | Se efectúan los cambios realizados |  
  |  Requerimientos |  |
  |  Notas |  _Notas adicionales_ |
  | Autor  | prorix |
  |Fecha | 11.11.24 |

  |  Caso de Uso	CU | Registrar datos partido  |
  |---|---|
  | Fuentes  | _Documento que sustenta el caso de uso_  |
  | Actor  | Árbitro |
  | Descripción | Se añaden datos a tiempo real del partido que se está gestionando |
  | Flujo básico | 1. Acceder al menú de gestión de partido con el código de uso único, 2. Registrar los datos necesarios. |
  | Pre-condiciones | Se está jugando un partido |  
  | Post-condiciones  |  |  
  |  Requerimientos |  |
  |  Notas |  _Notas adicionales_ |
  | Autor  | prorix |
  |Fecha | 11.11.24 |

  |  Caso de Uso	CU | Iniciar partido  |
  |---|---|
  | Fuentes  | _Documento que sustenta el caso de uso_  |
  | Actor  | Árbitro |
  | Descripción | Un partido se da por iniciado en la APP |
  | Flujo básico | 1. Acceder al menú de gestión de partido con el código de uso único, 2. Iniciar el partido. |
  | Pre-condiciones |  |  
  | Post-condiciones  | EL partido se inicia |  
  |  Requerimientos | Debe ser la hora acordada para el partido |
  |  Notas |  _Notas adicionales_ |
  | Autor  | prorix |
  |Fecha | 11.11.24 |

  |  Caso de Uso	CU | Finalizar partido  |
  |---|---|
  | Fuentes  | _Documento que sustenta el caso de uso_  |
  | Actor  | Árbitro |
  | Descripción | Un partido se da por finalizado en la APP |
  | Flujo básico | 1. Acceder al menú de gestión de partido con el código de uso único, 2. Finalizar el partido. |
  | Pre-condiciones | El partido está iniciado |  
  | Post-condiciones  | El partido se finaliza |  
  |  Requerimientos | El partido debe haber acabado |
  |  Notas |  _Notas adicionales_ |
  | Autor  | prorix |
  |Fecha | 11.11.24 |

  |  Caso de Uso	CU | Abrir disponibilidad de añadir rotaciones iniciales  |
  |---|---|
  | Fuentes  | _Documento que sustenta el caso de uso_  |
  | Actor  | Árbitro |
  | Descripción | Se añaden datos a tiempo real del partido que se está gestionando |
  | Flujo básico | 1. Acceder al menú de gestión de partido con el código de uso único, 2. Iniciar el modo DARI (Disponible para Añadir Rotaciones Iniciales). |
  | Pre-condiciones | Se está jugando un partido |  
  | Post-condiciones  |  |  
  |  Requerimientos |  |
  |  Notas |  _Notas adicionales_ |
  | Autor  | prorix |
  |Fecha | 11.11.24 |

