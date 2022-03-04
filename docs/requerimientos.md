# Levantamiento de requerimientos

En el desarrollo de software, independientemente del tamaño del mismo, el levantamiento de requerimientos es una etapa tan critica como la codifciación. Un mal levantamiento del requerimientos hace que se incremente los tiempos de implementación, los costos y puede llevar al fracaso del proyecto. Es una fase colaborativa donde se tienen que involucrar todos los componentes interesados en el proyecto. Además de obtener la información necesaria para el desarrollo del software nos da la oportinudad de crear una buena relación con el usuario y de generar empatía con el mismo, también es importante destacar que en esta etapa la responsabilidad de hacer un buen levantamiento de requerimientos es comportida. De nada nos sirve tener un una encuesta parfectamente diseñada si el cliente luego no la contesta, miente, omite información, etc.     

Aunque se han creado diferentes métodos para realizar un mejor levantamiento de requerimientos, ésta sigue siendo una de las etapas con mayor cantidad de errores en los proyectos de
software debido, principalmente, a que existe un grave problema de comunicación entre el cliente y el desarrollador ya que ambos manejan un lenguaje totalmente diferente. [^1]

## Técnicas para el levantameinto de requerimientos

Para el levantamiento de requerimientos existen diferentes métodos, a continuación se muestran algunos de los métodos

### Entrevistas

* Son el método más común para el levantamiento de requerimientos. 
* Generalmente se realizan con los usuarios claves.
* Usar preguntas abiertas para obtener información faltante.
* User preguntas cerradas para confirmar o validar información.
* Dependiendo de los entrevistados pueden sugerir cosas contradictorias. Debido a la percepción de necesidades personales.
* No dejan ver el funcionamiento global de la organización o aplicación.

### Prototipos

* Facilitan que el usuario pueda comprender mejor cómo quedará finalmente el aplicativo al poder visualizar algunas vistas del desarrollo del proyecto de software.
* Puede llegar a excluir ciertos requerimientos ya que limita al cliente a lo que está viendo.
* Significa un esfuerzo adicional y por lo tanto un sobrecosto al proyecto en la medida en que el prototipo inicial no satisfaga las necesidades planteadas y se deba iniciar desde cero. 

### Herremientas UML

* Es un conjunto de estándares para la diagramación del sistema a desarrollar.
* Al ser visual permite una fácil visualización del sistema a un nivel macro pero también a un nivel atómico.
* Lenguaje técnico alejado de la terminología de negocio y difícil de entender por las personas de negocio.

### Modelado de procesos

* Es un conjunto de estándares para la diagramación de los diferentes procesos existentes en la organización.
* Es más comprensible para los usuarios finales comprender los requerimientos necesarios para la creación del sistema.
* Maneja una representación visual común para los usuarios finales que permite que el lenguaje utilizado no sea técnico y pueda haber una comunicación eficaz entre ambas partes.

### Observación

* Consiste en estudiar el entorno de trabajo de los usuarios, clientes e interesados de proyecto (Stakeholders).
* Es una técnica útil cuando se está documentando la situación actual de procesos de negocio.
* En observación pasiva, el observador no hace preguntas, limitándose solo a tomar notas y a no interferir en el desempeño normal de las operaciones.
* En observación activa, el observador puede conversar con el usuario.

### Encuestas o cuestionarios

* Es una técnica útil para recopilar eficientemente los requerimientos de muchas personas.
* La clave para el éxito es que tengan un propósito y audiencia claramente definida, con preguntas claras y concisas.
* Deben enfocarse en los objetivos de negocio que se necesitan identificar.
* Pueden apoyarse con entrevistas de seguimiento con usuarios individuales.

### Mesas de trabajo

* Es una técnica efectiva para obtener información rápidamente de varias personas.
* Se pueden combinar con otras técnicas como pueden ser las entrevistas y cuestionarios.

### Tormentas de ideas

* Es una sesión de trabajo estructurada orientada para obtener la mayor cantidad de ideas posibles.
* Las reglas son importantes, por ejemplo los criterios para evaluar ideas y asignarles un puntaje, no permitir las críticas a las ideas y limitar el tiempo de discusión.
* En una primera fase, se deben identificar la mayor cantidad de ideas, para luego evaluarlas. Todas las ideas deben ser consideradas y deben limitarse que una idea se le ahogue o critique antes de tener tiempo de desarrollarla.

## Especificación de requerimientos de software

Toda la información recogida durenta el levantamiento de requerimientos puede ser incluida en una especificación de requerimientos de software. 

Al levantamiento de requerimientos le sigue el análisis de los mismos, por medio de técnicas como el modelado de procesos, casos de uso, prototipos, etc. [^2]

El documento de requerimientos de software, es el lugar donde se da descripción a las características y requisitos de un software, producto, programa o conjunto de programas. Los requisitos se expresan en lenguaje natural, sin consideraciones ni términos técnicos.

La especificación de requisitos de software es el resultado del levantamiento de información con el usuario o cliente del producto. Son un método para una comunicación más concisa y clara entre los encargados de desarrollar el software y el área de negocio o clientes que usaran el producto. El estándar IEEE 830 indica como debe ser el formato y la organización de un buen documento de requisitos [^3]. A continuación veremos algunas de las seccione de la especificación.

### Propósito

Se describen cuales componentes o partes del alcance del producto están incluidas en el documento, estableciendo si cubre la totalidad del software, sólo una parte del sistema, subsistema o subgrupo de procesos y se especificará a quien va dirigido el documento.

Se describe el objetivo principal del proyecto.

##### Ejemplo

El proyecto del segundo cuatrimestre tiene como objetivo desarrollar ...

Esta app permitirá tanto la consulta de información, ... así como la comunicación o reporte de incidencias ...

Tiene X objetivos principales. ... dotar a los habitantes de un servicio que facilite la consulta de datos ..., para facilitar el mantenimiento del espacio público ya que los habitantes
dispondrán de una herramienta que permita detectar incidencias y comunicarlas al ayuntamiento ....

### Alcance

Descripción corta del alcance del software que se está especificando, incluyendo: se explicará lo que el sistema hará y lo que no hará, los beneficios que brinda al área de negocio y organización, los objetivos y metas que se esperan alcanzar. Se puede hacer referencia a otros documentos de nivel superior. 

##### Ejemplo

El límite geográfico del proyecto, ....

Se mostrarán los servicios públicos del municipio ....

... dado que la introducción de coordenadas puede ser automática (GPS) o manual (introducidas por el usuario), las incidencias
situadas en el exterior del municipio serán consideradas de errores en la introducción manual ...

### Definiciones

Descripción de términos, acrónimos y siglas necesarias para el entendimiento del documento de requerimientos de software.

##### Ejemplo

* **Geolocalización**: Capacidad de situar mediante coordenadas la ubicación real de un elemento, persona u objeto.
* **GLONASS**: Es el sistema de posicionamiento global desarrollado por la Federación Rusa.

### Descripción del proyecto

En esta sección se describen todos aquellos factores que afectan al producto y a sus requisitos. No se describen los requisitos, sino su contexto. Normalmente, esta sección consta de las siguientes subsecciones: Perspectiva del producto, funciones del producto, características de los usuarios, restricciones, factores que se asumen y futuros requisitos.

#### Funciones del producto u objetivos

Se mostrará un resumen, a grandes rasgos, de las funciones del futuro sistema. Por ejemplo, para un programa de contabilidad, mostrará que el sistema soportará el
mantenimiento de cuentas, el estado de las cuentas y facilitará la facturación, sin mencionar en detalle que cada una de estas funciones.

Las funciones deberán mostrarse de forma organizada, y pueden utilizarse gráficos, siempre y cuando dichos gráficos reflejen las relaciones entre funciones y no el diseño del sistema.

##### Ejemplo

Las finalidades de la GeoApp se pueden agrupar en dos grupos. ... permitir la visualización de los datos .... el aplicativo permita que los usuarios puedan ...

Grupos y necesidades:

* Ayuntamiento de Sant Boi de Llobregat
    * Mostrar información 
    * Recibir incidencias de la vía pública
    * ....
* Usuarios
    * Consultar información
    * Detectar e informar sobre incidencias en la vía pública
    * ....

#### Características de los Usuarios

Se describen las características generales de los usuarios del producto, incluyendo nivel educacional, experiencia y experiencia técnica. La clasificación puede ser en función a la frecuencia de uso, grupo de funcionalidades utilizadas, privilegios de seguridad, nivel de experiencia y otros parámetros.

##### Ejemplo

En general se espera que los usuarios sean de varios tipos. En primer lugar, individuos con interés en la consulta de los datos ... Vecinos del pueblo ... todos aquellos habitantes
que sientan interés en colaborar con el consistorio en la detección y resolución de las incidencias. 

... también cabe destacar un segundo actor que tendrá acceso a todos los datos existentes en el sistema. Este corresponde al administrador ...

#### Restricciones

Se describen aquellas limitaciones que se imponen sobre los desarrolladores del producto. Por ejemplo limitaciones de hardware, funciones de control, leguajes de programación, etc.

##### Ejemplo

Para el correcto funcionamiento será totalmente necesario disponer de conexión a internet. ... Permitir el uso del GPS ... No hay control de usuarios ...

#### Suposiciones y Dependencias

Se describen los factores que pueden afectar a los requisitos. Por ejemplo si cambian ciertos detalles técnicos como el sistema operativo, etc.

##### Ejemplo

Para el correcto funcionamiento del sistema será necesaria la existencia de un administrador que se encarga de la información .... Disponer de un servicio WMS ...

#### Requisitos Específicos

Contiene los requisitos a un nivel de detalle suficiente como para permitir a los diseñadores diseñar un sistema que satisfaga estos requisitos, y que permita al equipo de pruebas planificar y realizar las pruebas que demuestren si el sistema satisface, o no, los requisitos. Todo requisito aquí especificado describirá comportamientos externos del sistema, perceptibles por parte de los usuarios, operadores y otros sistemas. Esta es la sección más larga e importante. Deberán aplicarse los siguientes principios:

* El documento debería ser perfectamente legible por personas de muy distintas formaciones e intereses.
* Deberán referenciarse aquellos documentos relevantes que poseen alguna influencia sobre los requisitos.
* Todo requisito deberá ser unívocamente identificable mediante algún código o sistema de numeración adecuado.

Se considera **requerimiento** a:

* Una condición o capacidad requerida por el usuario para solventar un problema o alcanzar un objetivo.
* Una condición o capacidad que debe disponer el sistema o parte del sistema para satisfacer un contrato.
* Una representación documentada de una condición o capacidad.

El conjunto de requerimientos debe mantener las siguientes propiedades:

* **Único**: Cada requerimiento tiene que ser declarado una sola vez.
* **Normalizado**: Los requerimientos no se han de entrelazar.
* **Interdependiente**: Se han de definir explícitamente las relaciones entre los requerimientos individuales, para formar el sistema completo.
* **Completo**: las especificaciones de requerimientos han de incluir todos los requerimientos expresados por el cliente, así como aquellos necesarios para la definición e implantación del sistema.
* **Consistente**: las especificaciones de requerimientos ha de ser consistentes y sin contradicciones en el detalle, estilo de declaración y en la presentación.
* **Acotado**: Se han de identificar los límites, el alcance y el contexto de los requerimientos.
* **Modificable**: Debería ser modificable.
* **Configurable**: las versiones han de ser mantenidas a lo largo del tiempo.
* **Granular**: Ha de incluir diferentes niveles de abstracción.  

##### Requerimientos funcionales

*“Los requerimientos funcionales son las descripciones explicitas del comportamiento que debe tener una solución de software y que información debe manejar.”* [^4]

Expresan las capacidades o cualidades que debe tener la solución para satisfacer los requerimientos, cuál debe ser el comportamiento de la solución y que información debe manejar. Definen los criterios que este debe cumplir para que este sea adecuado para su propósito (Fitness-for-purpose).

##### Requerimientos no funcionales

Con frecuencia, los requerimientos no funcionales son ignorados o subestimados en la fase de análisis de requerimientos. Los requerimientos no funcionales son los que especifican criterios para evaluar la operación de un servicio de tecnología de información, en contraste con los requerimientos funcionales que especifican los comportamientos específicos. [^5]

Requerimientos no funcionales especifican los criterios que debe cumplir para que sea adecuado para su uso (Fitness-for-use).

Se pueden clasificar en dos categorías:

* Cualidades observables en tiempo de ejecución, como por ejemplo la usabilidad, interfaz y la seguridad.
* Cualidades relacionadas con la evolución del sistema, como por ejemplo Mantenibilidad, Comprobabilidad, Extensibilidad y Escalabilidad, las cuales están inmersas en la estructura del sistema de software.

#### Requisitos Futuros

Se describen futuras mejoras al sistema, que podrán analizarse e implementarse en un futuro.

## Referencias

[^1]: Henry León Pérez Virgen, Carlos Alberto Salamando Mejía, Luz Stella Valencia Ayala - *Levantamiento de requerimientos basados en el conocimiento del proceso* - 2012.
[^2]: http://www.pmoinformatica.com/2016/08/tecnicas-levantamiento-requerimientos.html
[^3]: https://www.fdi.ucm.es/profesor/gmendez/docs/is0809/ieee830.pdf
[^4]: http://www.pmoinformatica.com/2018/05/que-es-requerimiento-funcional.html
[^5]: http://www.pmoinformatica.com/2013/01/requerimientos-no-funcionales-porque.html
