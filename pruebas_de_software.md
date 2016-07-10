# Pruebas de Software

Aunque las pruebas forman parte del propio desarrollo, ya que deben realizarse de manera sistemática durante el mismo, merecen una atención especial ya que permiten, en mayor o menor medida, asegurar la calidad del software.


## Pruebas estáticas, de verificación
El testeo estático se refiere a aquel que se hace sin ejecutar el código. En este tipo de testeo está enfocado a buscar errores de sintaxis, conceptuales y facilitar las refactorizaciones. Parte de este trabajo lo pueden realizar los propios **entornos de desarrollo (IDE)** por lo que puede resultar interesante exigir al equipo de desarrollo trabajar con software de este tipo.  Por otro lado, inspecciones del código con métodos como la **revisión por pares** ayuda, primero, a localizar errores que han pasado desapercibidos para quien ha escrito el código y, segundo, estimular la refactorización, resultando en un código más lógico, legible, mantenible, escalable…

La revisión por pares consiste en que el código escrito por un desarrollador sea revisado por otro (si hay tres desarrolladores, A, B y C, B revisa a A, C revisa a B y A revisa a C). También puede ser conveniente que, si es posible, se intercalen las personas revisoras en sucesivas sesiones ya que puede ser más enriquecedor al contar con diferentes opiniones. La revisión por pares puede fomentar y hacer consciente la creación de un código más legible y acompañado de comentarios suficientes para que otro desarrollador lo entienda con facilidad. Debe resultar en una recolección de los errores y sugerencias, que puede ser de la siguiente forma:

    "Desarrollador A (nombre)

      Sesión D1/MM/AAAA
      Revisor: B (nombre)

        Commit: (id)
		Archivo: archivo.py
		Observaciones: Texto indicando las observaciones y concretando sobre qué línea del código se refieren para facilitar la búsqueda.
		Solución aportada: Decisión tomada por el desarrollador A con respecto a la observación.

		Commit: (id)
		Archivo: archivo.py
		Observaciones: (...)
		Solución aportada: (...)

		(...)

      Sesión D2/MM/AAAA
      Revisor: C (nombre)

		Commit: (id)
		Archivo: archivo.py
		Observaciones: (...)
		Solución aportada: (...)

		(...)"

Estas revisiones por pares se deberían hacer de forma sistemática al final de cada etapa, que podría ser el final de una sesión de trabajo, un commit, el completado de un caso de uso, de una función… Tras una breve reflexión, quizás, lo más adecuado sería hacer la revisión cada commit, ya que un commit debería hacerse siempre y cuando se considere que se ha completado una parte del desarrollo de forma íntegra, que tiene sentido en sí misma. Además, ya que atender cada commit por parte del desarrollador compañero interrumpiría el trabajo del mismo, puede ser conveniente atender todos los commit realizados durante la sesión de trabajo al final de la misma, reservando siempre un margen de tiempo para dicha tarea.


#### Conclusiones
* Utilización de entorno IDE para el desarrollo.
* Revisión por pares cada commit/sesión de trabajo.


## Pruebas dinámicas, de validación
Testeo realizado ejecutando el propio código. Puede realizarse sin que el desarrollo esté 100% completado ejecutando partes del código de forma independiente.

### [Pruebas de caja blanca](https://en.wikipedia.org/wiki/White-box_testing)
Pruebas caracterizadas por conocer y tener en cuenta el código del software. Se puede aplicar a [nivel de unidad](https://en.wikipedia.org/wiki/Unit_testing) (la parte ejecutable más pequeña del software, generalmente una función o procedimiento, aunque en programación orientada a objetos puede tratarse tanto de una clase/interfaz entera como de un método individual), a [nivel de integración](https://en.wikipedia.org/wiki/Integration_testing) (combinando en grupo varios módulos unitarios de software) o a [nivel de sistema](https://en.wikipedia.org/wiki/System_testing) (testeo del sistema en su totalidad, incluyendo el software completo y su entorno de ejecución). Sin embargo, suele realizarse generalmente a nivel unitario, ya que este tipo de testeo aplicado a nivel de módulo o sistema aumentaría, de forma general, en exceso el coste de desarrollo por su complejidad y detalle, dejando esas estructuras para ser probadas mediante “caja negra”.

Dentro de las pruebas de caja blanca existen varias técnicas pero una de las más utilizadas es la del “code coverage”. El code coverage consiste en diseñar las pruebas de manera que comprueben todos los flujos de ejecución posibles del código. Este tipo de pruebas permite evaluar el 100% del código pero, por el contrario, no aseguran el correcto funcionamiento del software para diferentes condiciones o “inputs” del programa. Así mismo, tampoco sirven para asegurar que todos los casos de uso o funcionalidades hayan sido implementadas. Además, al tratarse de pruebas diseñadas en base al código, cambios en éste pueden requerir de cambios en las propias pruebas. Debido a ello, este tipo de pruebas puede resultar en un alto coste operativo si cada cambio realizado en el código debe resultar en, al menos, una revisión de las pruebas, si no en un rediseño. Quizás podría ser adecuado plantear pruebas de este tipo cada vez que se realice una versión “mayor” del software, candidata a versión estable. También puede ser de gran utilidad en esta tarea contar con alguna herramienta de “dubugging” que permita comprobar el “camino” que está tomando la ejecución.





