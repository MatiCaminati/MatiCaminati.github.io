# <center>  Universidad Nacional de Río Cuarto </center>

## <center> Facultad de Ingeniería </center>

<p align="center"> 

![UNRC, Facultad de Ingeniería, Departamento de Telecomunicaciones](\Imagenes\caratula.jpg) 

</p>

## <center> Aplicaciones TCP/IP (Cod. 0052) </center>

## <center> ‘PARKING 4.0 RIO IV’ </center>

Docentes: 

* Anunziata, Daniel
* Solivellas, Pablo

Alumna/o/s:

* Caminati, Matías 
* Del Sole, Franco

Año académico: 5to (quinto) año

___

##  1.  Resumen

El proyecto tiene como objetivo agilizar el tráfico de la ciudad de Río Cuarto, enfocándose en la agilidad al momento de estacionar en lugares con gran circulación. Es un problema común la búsqueda de un lugar de estacionamiento al momento de desplazarse por la ciudad, más aún en los lugares de mayor circulación, derivando en estacionamiento saturado, pagar altas tarifas, mayor impacto ambiental, estacionamiento en la calle o fuera de la calle, uso inadecuado del estacionamiento existente, etc.

Con este proyecto se busca agilizar el estacionamiento a través de una aplicación en el que el usuario pueda observar en un mapa los slots disponibles para estacionamiento en tiempo real en las calles de la ciudad, y los agentes puedan observar situaciones particulares para un mejor control de tránsito. Además, la recolección de ciertos datos , permitirán más usos para el futuro. 

___

##   2. Tabla de contenidos 

___

##  3. Introducción 

El Departamento de Asuntos Económicos y Sociales de la ONU predice que todo el crecimiento de la población mundial vivirá en las áreas urbanas. Y se prevé que la tasa de crecimiento alcance 68% en 2050. Esto no implica solo problemas para los gobiernos, sino también una realidad cotidiana para los ciudadanos. La búsqueda de estacionamiento resultará en una gran pérdida de tiempo, dinero y mayor contaminación.

Al profundizar más en esta problemática, se aprecia la necesidad de un sistema inteligente de IoT que permita actuar sobre esta y brinde una solución pertinente.

Específicmente en la ciudad de Río Cuarto, ciudad en donde los actores de este informe se desenvuelven, la única solución presente es un mayor control por parte de agentes de tránsito, campañas de concientización y la propia capacidad de manejo de la gente. Muchas veces, alguno de estos factores no se ejercen de manera correcta o las personas no colaboran a que el tráfico sea un entorno amigable para los actores de la vía pública.

En el siguiente informe se detalla una solución a lo planteado anteriormente la cual toma esta problemática y la soluciona con la implementación de una aplicación ‘Parking 4.0’. En primer lugar se detallan los objetivos de la presente y luego los requerimientos de alto y bajo nivel que el mismo debe cumplir. Luego se describe la etapa de diseño del software haciendo una descripción más profunda de la funcionalidad del mismo y cómo llevarlo a cabo para posteriormente detallar como fue implementado, seguido de la etapa de ‘testing’ en la cual se analiza el correcto funcionamiento de todas las etapas del proyecto. Finalmente, en la conclusión se exponen ideas finales del producto y los potenciales que este posee en caso de un funcionamiento exitoso con el tiempo.

___

##  4. Objetivos 

Desarrollar una solución con el uso de IoT para resolver el problema de estacionamiento en la ciudad de Río Cuarto, con la integración de los conceptos vistos en la materia de Aplicaciones TCP/IP, y el uso de nuevas herramientas facilitadoras.

___

##  5. Requerimientos 

###   5.1. Requerimientos Generales - Alto Nivel 

####   5.1.1. Características Generales 

####   5.1.2. Interaz de usuario  

####   5.1.3. Persistencia de datos 

###   5.2. Requerimientos Generales - Bajo Nivel 

####   5.2.1. Usuarios del sistema 
####   5.2.2. Interaz de usuario  
####   5.2.3. Persistencia de datos 

___

##  6. Diseño del Sistema 

 Para llevar a cabo el diseño del Software requerido se opta por la Arquitectura basada en componentes con nivel de detalle. En el mismo se descompone el sistema en unidades componentes que deben tener especificadas sus entradas y salidas prescindiendo de una descripción detallada de su implementación, relacionándolos a través de conectores que especifican y gobiernan la interacción entre los mismos. Estos componentes deben encapsular funcionalidades y comportamientos, y cumplir con ciertas características como ser reutilizables en diferentes situaciones y aplicaciones, extensibles a partir de componentes existentes  para proporcionar un nuevo comportamiento y no ser específicos del contexto. Así esta metodología proporciona un mayor nivel de abstracción y divide el problema en subproblemas, cada uno asociado con una unidad componente facilitando el desarrollo del sistema pedido. Se especifican tres niveles de detalle.
- Nivel 0 (L0): Sistema simplificado con un solo objeto o bloque que describe el proyecto. Una entrada y una salida. (Opcional)
- Nivel 1 (L1): Se expande el bloque del Nivel 0 detallando a gran escala el mismo.
- Nivel 2 (L2): Se describe a mayor detalle cada bloque del nivel anterior. Exponiendo de forma resumida las tecnologías que se van a utilizar para lograr la integración.
- Nivel 3 (L3): Se documentan las decisiones realizadas por el grupo de implementación para poder llevar a cabo los requerimientos generales.

###   6.1. Nivel 0 (L0) 

![Nivel 0](\Imagenes\sis_level0.jpg)

####  Sistema 
Se encarga de recibir la información generada por los sensores y procesar la información que llega a los diferentes usuarios.
- Entrada: información de los sensores, indicando si hay un objeto o no en la posición correspondiente.
- Salida: Mapa con información sobre la disponibilidad de los diferentes slots de estacionamiento en las calles de la ciudad. Para demás usuarios se muestran gráficas con valores estadísticos.
