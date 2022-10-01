# TA 1 - Programación Concurrente

![](https://github.com/aelvismorales/TA_PrograConcurrente/blob/main/Assets/upc_logo.png)
#### Universidad Peruana de Ciencias Aplicadas
##### Carrera:
 Ciencias de la Computación
 ##### Ciclo:
 2022-02
 ##### Curso:
 Programación Concurrente
 ##### Tema:
 Investigación sobre como implementar herramientas colaborativas
 ##### Profesor:
 Canaval Sánchez, Luis Martin
 ##### Integrantes:
  Cristopher Elvs Morales Montero - 201820751
  Aldo Jhair Gomez Lozano - 201822450
  ##### Septiembre - 2022

Introducción:
============

Actualmente, uno de los perfiles más requeridos en el mundo laboral es el de ser capaz de trabajar en equipo. Específicamente, en el área de la computación, los proyectos de software requieren que un amplio número de personas trabajen simultáneamente en el desarrollo del producto. Para ello, se emplean herramientas colaborativas como GitHub, con el fin de poder gestionar los proyectos que involucren a personas que no comparten un espacio de trabajo determinado. Por otro lado, existen otros tipos de herramientas colaborativas como, google docs o google colab que son procesadores de texto en línea con un objetivo bastante similar a GitHub. A continuación se realizará una breve descripción acerca de los tipos de herramientas colaborativas más comunes.

**1. ¿Qué es un editor de texto en línea - colaborativos?**

Un editor de texto colaborativo admite varios documentos en una misma sesión. Asimismo, permite la participación de múltiples usuarios para trabajar en un determinado contenido a la misma vez.

..1. **Editores de texto más usados**
* Collab Edit: Es un editor de texto online pensado para programar de forma colaborativa. Soporta lenguajes como JAVA, JS, PYTHON, CSS, C + +, PHP y más. 
* Write Url: Permite crear y editar textos en tiempo real y de forma colaborativa
* Stack Edit: Es un procesador de texto que trabaja principalmente con formato MarkDown
* Google Docs: Es uno de los mejores procesadores de texto online que existe. Se pueden crear tanto documentos, como hojas de cálculo o presentaciones.

..2. **Ventajas y desventajas**
| Ventajas                  | Desventajas|
|---------------------------|------------|
|Edición fácil de contenido |Posibilidad de archivos corruptos|
|Compartir información de forma más sencilla|Plagio de información|
|Multiplataforma|Posibilidad de pérdida de información|

**Técnicas aplicadas para el desarrollo de Editores de Texto en Línea:**
* **Operational Transformation (OT) :** Es una tecnología la cual permite una variedad de funcionalidades de colaboración en sistemas de software de colaboración avanzados.  Esta técnica se inventó originalmente para el mantenimiento de la coherencia y el control de la concurrencia en la edición colaborativa de documentos de texto sin formato, pero sus capacidades se han ampliado y también sus aplicaciones los cuales pueden incluir deshacer grupos, bloqueo, resolución de conflictos, notificación y comprensión de operaciones.

* **Conflict Free replicated data type (CRDT):** Estos son un tipo de dato abstracto el cual se encuentra diseñado para poder replicarlo en múltiples máquinas o procesos. Estos datos se utilizan en sistemas de replicación que siguen una estrategia optimista.
El utilizar este tipo de datos simplifica los sistemas de almacenamiento de datos distribuidos, dado que agrega autonomía y consistencia, dado que cada réplica puede actualizarse sin la necesidad de sincronizarse con otras réplicas, de forma independiente y concurrente.

**Conceptos Teóricos aplicados para el desarrollo de Editores de Texto en Línea:**
* **Funciones de transformación:** Estas funciones transforman las operaciones para que termine con secuencias de operaciones que terminarán en el mismo resultado.
![](https://www.aha.io/1c4199875214246383d366a8a1d96ab5/transform-lower-right.png)

* **Cursor:** Si el documento es una lista de cosas, el cursor es una posición en esa matriz
![](https://www.aha.io/2580497c48afc8f4e42e7c26937c5ae5/cursor-position-1.png)

* **Deshacer y Rehacer:** Contienen operaciones invertidas que se transforman cada vez que entra una operación remota
![](https://www.aha.io/f2d50e520c0fbf9b101cf10f82f6fccb/undo-remove-s-4.png)

**Retos Técnicos en el desarrollo de un editor de texto en línea:**

* El tiempo de latencia de comunicación, esto se debe a que la velocidad de comunicación es muy limitada, en donde se crea el dilema en el cual el usuario necesita tener su propia edición incorporada. El verdadero reto dentro de la edición es el cómo aplicar los cambios realizados por otros usuarios, cuando estas versiones modificadas nunca existieron de manera local en su propio documento.

* La sincronización de los documentos, es decir, si dos personas escriben al mismo tiempo en los documentos esto puede ocasionar conflictos, dado que la realización del cambio de una persona, puede ser distinta a la de otra, lo cual implica un resultado no esperado a causa de una mala unión en los datos. Por ello, los datos deberían de ser idempotentes y conmutativos, en la cual, la primera, es la acción de realizar una misma acción varias veces y aun así conseguir el mismo resultado y la segunda, es una propiedad en la que no importe el orden de los cambios, el resultado final será el mismo. Además, se utiliza la generación global de identificadores únicos de cada letra.

Herramientas de software que se utilizan para un posible desarrollo de un editor de texto en línea:
* En la mayoría de los casos como por ejemplo el de Google Docs, se utilizaron lenguajes como Java y C++ para realizar el backend, gestión de base de datos, y Javascript, html y css para el frontend

_REFERENCIAS BIBLIOGRÁFICAS_


Strickland, J. (s.f). How google docs works. Recuperado de [https://computer.howstuffworks.com/internet/basics/google-docs5.htm](https://computer.howstuffworks.com/internet/basics/google-docs5.htm) Consultado el 20 de septiembre de 2022

Weiss, J. (2018). How to Build a Collaborative Text Editor Using Rails. Recuperado de  [https://www.aha.io/engineering/articles/how-to-build-collaborative-text-editor-rails](https://www.aha.io/engineering/articles/how-to-build-collaborative-text-editor-rails) Consultado el 20 de septiembre de 2020

Wikipedia (s.f) . Collaborative real-time editor . Recuperado de [Collaborative real-time editor - Wikipedia](https://en.wikipedia.org/wiki/Collaborative_real-time_editor)  Consultado el 28 de septiembre de 2022

Digital Freepen (2017).  A simple approach to building a real-time collaborative text editor. Recuperado de [A simple approach to building a real-time collaborative text editor - Digital Freepen](https://digitalfreepen.com/2017/10/06/simple-real-time-collaborative-text-editor.html) Consultado el 28 de septiembre de 2022
