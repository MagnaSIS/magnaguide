# Sistema de información normalizado para un proyecto en Magna SIS


## Esquema general

[![](https://docs.google.com/drawings/d/1cWFzESKB95219659yr3Jx4KYYPJC-pm0JPzU88oEeoM/pub?w=962&h=450)](https://docs.google.com/drawings/d/1cWFzESKB95219659yr3Jx4KYYPJC-pm0JPzU88oEeoM/edit?usp=sharing)
Clic en la imagen para editarla

## Descripción y nomenclatura


* ### Directorio del proyecto (regexp: /[EIM]\d{3}/ ):
Es el directorio raíz del proyecto donde se integran todos los documentos relacionados con el proyecto o, en su caso, enlaces e información referente a recursos externos al sistema de información. La carpeta del proyecto debe ser nombrada con el código identificativo del proyecto, una letra (I, proyecto interno, E, proyecto externo o M, proyecto de mantenimiento) seguida del número del proyecto en tres dígitos, que reflejará el número de proyectos totales de ese tipo realizados en Magna SIS y en orden consecutivo de creación. El mantener el mismo formato (X000) permite localizar y ordenar fácilmente los proyectos.

  * #### Planificación:
Directorio para recopilar aquello relacionado con la planificación y el seguimiento y control del proyecto como el Acta de constitución, el documento de Planificación y la hoja de Seguimiento y Control.

    * ##### Acta de constitución (regexp: /AC - [EIM]\d{3}/ )
Se nombra con las iniciales mayúsculas AC seguidas de un guión y el código identificativo del proyecto.

    * ##### Planificación (regexp: /PL - [EIM]\d{3}/ )
Se nombra con las iniciales mayúsculas PL seguidas de un guión y el código identificativo del proyecto.

    * #####Seguimiento y Control (regexp: /SC - [EIM]\d{3}/ )
Se nombra con las iniciales mayúsculas SC seguidas de un guión y el código identificativo del proyecto.

  * ####Producto
Directorio donde almacenar todos aquellos recursos integrados en el producto. En caso de tratarse de un recurso externo como, por ejemplo, una página web, se deben indicar los enlaces y credenciales correspondientes que permitan acceder al recurso.

    * #####Copias de seguridad (regexp: /CS\d{4}/\d{2}/\d{2} - [EIM]\d{3}/ )
Se nombran utilizando las iniciales mayúsculas CS seguidas de la fecha en formato AAAA/MM/DD y terminando en un guión junto al código del proyecto. Se recomienda incluir las copias de seguridad en dentro de un subdirectorio "Copias de Seguridad".

  * ####Activos
En este directorio se recogen aquellos recursos útiles para el proyecto pero que no estén explícitamente incluidos en el producto final, como pueden ser las lecciones aprendidas, una comparativa de diferentes servicios de hosting, una encuesta para concretar aspectos del producto o una serie de clips de vídeo que aún no han sido editados para el producto final.

  * ####Reuniones
Lugar donde recoger los recursos generados en las reuniones, principalmente las actas de reunión.

    * #####Actas de reunión (regexp: /AR\d{4}/\d{2}/\d{2} - [EIM]\d{3}/ )
Se nombran con las iniciales mayúsculas AR seguidas de la fecha en formato AAAA/MM/DD y terminando en un guión junto al código del proyecto.

  * ####Público
En este directorio solo se encontrarán aquellos recursos que se quieran compartir con personas ajenas al proyecto y a la organización, como pueden ser el cliente u otros interesados, de manera que solo exista acceso “público” a este apartado del sistema de información. Aquí se puede encontrar, entre otras cosas, el Acta de Conformidad del proyecto.

    * #####Acta de conformidad del proyecto (regexp: /CF - [EIM]\d{3}/ )
Documento nombrado con las iniciales mayúsculas CF seguidas de un guión y el código identificativo del proyecto.


## Lecciones Aprendidas
**regexp: /CF - [EIM]\d{3}/**

Este apartado del sistema de información tiene un tratamiento específico por la importancia de cara a Magna SIS y la tendencia al descuido en la ejecución del proyecto.

Las Lecciones Aprendidas son aquellas reflexiones, conclusiones, consejos o pautas obtenidos tras realizar una tarea o actividad y que pueden ser útiles de cara a realizar la misma tarea o actividad en el futuro. Tienen que ser redactadas de manera que puedan ser comprendidas por otras personas y con el detalle suficiente para conocer su contexto.

Ejemplos de LLAA:
"La versión A del software B tiene C problemas, mientras que la versión D los subsana a cambio de perder E funcionalidades."
"Los alumnos tiene una carga de trabajo superior los meses de Diciembre y Mayo y complica la disponibilidad de cara proyectos de Magna SIS."

Contraejemplos:
"Es importante cumplir los plazos del proyecto."
"Hay que tener en cuenta a los intereses de la empresa durante el proyecto."

Una forma de identificar cuáles NO son LLAA es invertir el sentido de la frase y ver si tiene sentido o no. Por ejemplo, en el primer contraejemplo "Es importante cumplir los plazos del proyecto.", si invertimos su significado obtenemos "No es importante cumplir los plazos del proyecto.", lo cual es obvio que no tiene sentido y de lo que se concluye que no es una lección aprendida.

El documento de LLAA durante el desarrollo de un proyecto en Magna SIS deberá localizarse en la carpeta de "Activos" y las Lecciones Aprendidas que se vayan generando deberán incluir el autor y la fecha de las mismas, y clasificarse en, al menos, los siguientes apartados: "Dirección", "Planificacción", "Relación con el cliente" y "Aspectos técnicos". Podrán incluirse más apartados o subapartados ya que, por ejemplo, el apartado "Aspectos técnicos" podría ser más útil en proyectos con gran cantidad de LLAA si se ordenan por categorías (Framework, Alojamiento, Sistema Operativo...).


## Reestrucutración en el cierre del proyecto

No es lo mismo la utilidad del sistema de información durante el desarrollo del proyecto que una vez éste ha finalizado. Por eso, es importante reestructurar el sistema de información una vez se ha finalizado. Se recomienda que la estructura del sistema de información durante la ejecución se "vuelque" de forma inalterada dentro de un subdirectorio llamado "SIE" (Sistema de Información en Ejecución) y del  cual se extraigan los documentos más relevantes de cara a una futura consulta: Lecciones Aprendidas, Planificación, Acta de Constitución y documento de Seguimiento y Control, quedando la estrucutra de la siguiente manera:

[![](https://docs.google.com/drawings/d/1h3_T12SkvY_K0bo1m6bVeoj0tcn8nFyANIZ64RXtZfQ/pub?w=963&amp;h=541)](https://docs.google.com/drawings/d/1h3_T12SkvY_K0bo1m6bVeoj0tcn8nFyANIZ64RXtZfQ/edit?usp=sharing)
Clic en la imagen para editarla







