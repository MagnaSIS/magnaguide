# Sistema de información normalizado para un proyecto en Magna SIS


## Esquema general

[![](https://docs.google.com/drawings/d/1cWFzESKB95219659yr3Jx4KYYPJC-pm0JPzU88oEeoM/pub?w=962&h=450)](https://docs.google.com/drawings/d/1cWFzESKB95219659yr3Jx4KYYPJC-pm0JPzU88oEeoM/edit?usp=sharing)
Clic en la imagen para editarla

## Descripción y nomenclatura

* **Directorio del proyecto** (regexp: /[EIM]\d{3}/ ):
Es el directorio raíz del proyecto donde se integran todos los documentos relacionados con el proyecto o, en su caso, enlaces e información referente a recursos externos al sistema de información. La carpeta del proyecto debe ser nombrada con el código identificativo del proyecto, una letra (I, proyecto interno, E, proyecto externo o M, proyecto de mantenimiento) seguida del número del proyecto en tres dígitos, que reflejará el número de proyectos totales de ese tipo realizados en Magna SIS y en orden consecutivo de creación. El mantener el mismo formato (X000) permite localizar y ordenar fácilmente los proyectos.

  * **Planificación**:
Directorio para recopilar aquello relacionado con la planificación y el seguimiento y control del proyecto como el Acta de constitución, el documento de Planificación y la hoja de Seguimiento y Control.

    * **Acta de constitución** (regexp: /AC - [EIM]\d{3}/ )
Se nombra con las iniciales mayúsculas AC seguidas de un guión y el código identificativo del proyecto.

    * **Planificación** (regexp: /PL - [EIM]\d{3}/ ):
Se nombra con las iniciales mayúsculas PL seguidas de un guión y el código identificativo del proyecto.

    * **Seguimiento y Control** (regexp: /SC - [EIM]\d{3}/ ):
Se nombra con las iniciales mayúsculas SC seguidas de un guión y el código identificativo del proyecto.

  * **Producto**:
Directorio donde almacenar todos aquellos recursos integrados en el producto. En caso de tratarse de un recurso externo como, por ejemplo, una página web, se deben indicar los enlaces y credenciales correspondientes que permitan acceder al recurso.

    * **Copias de seguridad** (regexp: /CS\d{4}/\d{2}/\d{2} - [EIM]\d{3}/ ): 
Se nombran utilizando las iniciales mayúsculas CS seguidas de la fecha en formato AAAA/MM/DD y terminando en un guión junto al código del proyecto.

  * **Activos**:
En este directorio se recogen aquellos recursos útiles para el proyecto pero que no estén explícitamente incluidos en el producto final, como puede ser una comparativa de diferentes servicios de hosting, una encuesta para concretar aspectos del producto o una serie de clips de vídeo que aún no han sido editados para el producto final.

  * **Reuniones**:
Lugar donde recoger los recursos generados en las reuniones, principalmente las actas de reunión.

    * **Actas de reunión** (regexp: /AR\d{4}/\d{2}/\d{2} - [EIM]\d{3}/ ):
Se nombran con las iniciales mayúsculas AR seguidas de la fecha en formato AAAA/MM/DD y terminando en un guión junto al código del proyecto.

  * **Público**:
En este directorio solo se encontrarán aquellos recursos que se quieran compartir con personas ajenas al proyecto y a la organización, como pueden ser el cliente u otros interesados, de manera que solo exista acceso “público” a este apartado del sistema de información. Aquí se puede encontrar, entre otras cosas, el Acta de Conformidad del proyecto.

    * **Acta de conformidad del proyecto** (regexp: /CF - [EIM]\d{3}/ ):
Documento nombrado con las iniciales mayúsculas CF seguidas de un guión y el código identificativo del proyecto.







