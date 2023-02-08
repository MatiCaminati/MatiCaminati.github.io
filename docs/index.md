# **<center>  Universidad Nacional de Río Cuarto </center>**

## <center> Facultad de Ingeniería </center>


<img src="\Imagenes\caratula.jpg"
     alt="UNRC"
     style="float: center; margin-center: 100px;" />


## <center> Aplicaciones TCP/IP (Cod. 0052) </center>

## **<center> ‘PARKING 4.0 RIO IV’ </center>**

<u> Docentes: </u> 

* Anunziata, Daniel
* Solivellas, Pablo

<u> Alumna/o/s:</u>

* Caminati, Matías 
* Del Sole, Franco

<u> Año académico:</u> 5to (quinto) año

___

##  1.  Resumen

El proyecto tiene como objetivo agilizar el tráfico de la ciudad de Río Cuarto, enfocándose en la agilidad al momento de estacionar en lugares con gran circulación. Es un problema común la búsqueda de un lugar de estacionamiento al momento de desplazarse por la ciudad, más aún en los lugares de mayor circulación, derivando en estacionamiento saturado, pagar altas tarifas, mayor impacto ambiental, estacionamiento en la calle o fuera de la calle, uso inadecuado del estacionamiento existente, etc.

En primer lugar se desarrolla una breve introudcción a la situación analizada y se plantearán los objetivos del proyecto. Luego se detallarán los requerimientos de alto y bajo nivel que el mismo debe cumplir. Seguirá la etapa de diseño del software haciendo una descripción más profunda de la funcionalidad del mismo y cómo llevarlo a cabo para posteriormente detallar como fue implementado, seguido de la etapa de ‘testing’ en la cual se analiza el correcto funcionamiento de todas las etapas del proyecto. Finalmente, en la conclusión se exponen ideas finales del producto y los potenciales que este posee en caso de un funcionamiento exitoso con el tiempo.

___

##  2. Tabla de contenidos 
- [1. Resumen](#1-resumen)
- [2. Tabla de contenidos](#2-tabla-de-contenidos)
- [3. Introducción](#3-introducción)
- [4. Objetivos](#4-objetivos)
- [5. Requerimientos](#5-requerimientos)
    - [5.1. Requerimientos generales - Alto Nivel](#51-requerimientos-generales---alto-nivel)
        - [5.1.1. Características generales](#511-características-generales)
        - [5.1.2. Interfaz de usuario](#512-interaz-de-usuario)
        - [5.1.3. Persistencia de datos](#513-persistencia-de-datos)
    - [5.2. Requerimientos generales - Bajo Nivel](#52-requerimientos-generales---bajo-nivel)
        - [5.2.1. Características del sistema](#521-características-del-sistema)
        - [5.2.2. Interfaz de usuario](#522-interfaz-de-usuario)
        - [5.2.3. Persistencia de datos](#523-persistencia-de-datos)
- [6. Diseño](#6-diseño-del-sistema)
    - [6.1. Nivel 0](#61-nivel-0-l0)
    - [6.2. Nivel 1](#62-nivel-1-l1)
    - [6.3. Nivel 2](#63-nivel-2-l2)
- [7. Implementación](#7-implementación)
    - [7.1. Implemetación real teórica](#71-implementación-real-teórica)
    - [7.2. Implemetación mediante una simulación del entorno](#72-implementación-mediante-una-simulación-del-entorno)
- [8. Plan de ensayos](#8-plan-de-ensayos)
- [9. Análisis de resultados](#9-análisis-de-resultados)
- [10. Conclusión](#10-conclusión)
- [11. Anexos](#11-anexos)

___

##  3. Introducción 

El Departamento de Asuntos Económicos y Sociales de la ONU predice que todo el crecimiento de la población mundial vivirá en las áreas urbanas. Y se prevé que la tasa de crecimiento alcance 68% en 2050. Esto no implica solo problemas para los gobiernos, sino también una realidad cotidiana para los ciudadanos. La búsqueda de estacionamiento resultará en una gran pérdida de tiempo, dinero y mayor contaminación.

Al profundizar más en esta problemática, se aprecia la necesidad de un sistema inteligente de IoT que permita actuar sobre esta y brinde una solución pertinente.

Específicmente en la ciudad de Río Cuarto, ciudad en donde los actores de este informe se desenvuelven, la única solución presente es un mayor control por parte de agentes de tránsito, campañas de concientización y la propia capacidad de manejo de la gente. Muchas veces, alguno de estos factores no se ejercen de manera correcta o las personas no colaboran a que el tráfico sea un entorno amigable para los actores de la vía pública.

En el siguiente informe se detalla una solución a lo planteado anteriormente la cual toma esta problemática y la soluciona con la implementación de una aplicación ‘Parking 4.0’, que permite observar en un mapa los slots disponibles para estacionamiento en tiempo real en las calles de la ciudad, y también permita a los agentes observar situaciones particulares para un mejor control de tránsito. Además, la recolección de ciertos datos , permitirán más usos para el futuro. 

___

##  4. Objetivos 

Desarrollar una solución con el uso de IoT para resolver el problema de estacionamiento en la ciudad de Río Cuarto, con la integración de los conceptos vistos en la materia de Aplicaciones TCP/IP, y el uso de nuevas herramientas facilitadoras.

___

##  5. Requerimientos 

###   **5.1. Requerimientos Generales - Alto Nivel** 

####   ***5.1.1. Características Generales*** 

| Código | INT_GRAL_0001 | Nombre | Interfaz de entrada/salida |
|---|:---:|---|:---:|
| Descripción | Se requiere la creación de un sistema que, al seleccionar el tipo de usuario, se redireccione a una interfaz gráfica que visualice las funciones del mismo, mediante un acceso con credenciales en caso de seleccionar un usuario específico.  |  |  |
| Prioridad | 1 | Rel. | - |
| Trazabilidad | - | Ref. | - |

| Código | US_GRAL_0001 | Nombre | Usuarios del Sistema |
|---|:---:|---|:---:|
| Descripción | El producto deberá permitir que sea utilizado por 2 tipos de usuario: El “usuario común”, con acceso a las funciones básicas. Estos son: conductores y agentes de tránsito. El administrador, que contará con acceso a la totalidad de las funciones. |  |  |
| Prioridad | 1 | Rel. | - |
| Trazabilidad | - | Ref. | - |

| Código | BD_GRAL_0001 | Nombre | Base de Datos |
|---|:---:|---|:---:|
| Descripción | El sistema deberá poseer una base de datos que permita el almacenamiento de la información de los sensores ubicados en los diferentes slots de almacenamiento. |  |  |
| Prioridad | 1 | Rel. | - |
| Trazabilidad | - | Ref. | - |

####   ***5.1.2. Interfaz de usuario***  

| Código | USR_INT_0001 | Nombre | Interfaz de Administrador |
|---|:---:|---|:---:|
| Descripción | Los administradores tendrán acceso a la nube, de modo que posean una interfaz que les permita visualizar y analizar los siguientes datos de los sensores: disponibilidad (presencia o no de un vehículo),  cambiar el estado de los slots en el mapa manualmente en caso de malfuncionamiento, cantidad de slots ocupados, diferentes estadísticos de los slots según se requiera por parte de sus superiores. |  |  |
| Prioridad | 1 | Rel. | US_GRAL_0001 |
| Trazabilidad | - | Ref. | - |

| Código | USR_INT_0002 | Nombre | Interfaz de Usuario |
|---|:---:|---|:---:|
| Descripción | El sistema debe proveer una interfaz en donde se seleccione el tipo de usuario, para ser redireccionado a la visualización de la información, mediante credenciales pertinentes en caso de pertenecer al usuario común Agente de Tránsito. |  |  |
| Prioridad | 1 | Rel. | US_GRAL_0001 |
| Trazabilidad | - | Ref. | - |

####   ***5.1.3. Persistencia de datos*** 

El sistema ofrece soporte para datos propios del sistema.

| Código | CFG_SIS_0001 | Nombre | Configuración sistema |
|---|:---:|---|:---:|
| Descripción | El sistema proveerá archivos de configuración a los usuarios administradores con la información necesaria para realizar: configuración del sistema, configuración de la interfaz gráfica, configuración de los sensores, mantenimiento del sistema |  |  |
| Prioridad |  1 | Rel. | INT_GRAL_0001 US_GRAL_0001 BD_GRAL_0001  |
| Trazabilidad | - | Ref. | - |

###   **5.2. Requerimientos Generales - Bajo Nivel** 

Esta sección describe los requerimientos del sistema relativos a las funcionalidades o requerimientos generales (alto nivel) que requieren mayor especificidad.

####   ***5.2.1. Características del sistema*** 

| Código | INT_LL_0001 | Nombre | Interfaz sistema |
|---|:---:|:---:|:---:|
| Descripción | El sistema debe poseer un menú de selección de usuario común, entiéndase, conductor o agente de tránsito. Mediante la selección de uno de estos se los redirecciona a los paneles de visualización correspondientes. Para el caso de los agentes de tránsito, en la misma página de visualización se le requerirá el ingreso de credenciales previamente brindado por el usuario administrador. |  |  |
| Prioridad | 1  | Rel. | INT_GRAL_0001 |
| Trazabilidad | - | Ref. | - |

| Código | INT_LL_0002 | Nombre | Cuenta Usuarios Comunes - Agentes de tránsito |
|---|:---:|---|---|
| Descripción | Los usuarios comunes referentes a los agentes de tránsito, deben contar con credenciales para poder acceder a la visualización de las funciones del sistema. Estas credenciales son generadas por el administrador mediante el servidor y sin posibilidad de ser modificadas por el usuario común. |  |  |
| Prioridad | 1 | Rel. | USR_GRAL_0001 |
| Trazabilidad | - | Ref. | - |

####   ***5.2.2. Interfaz de usuario*** 

| Código | INT_LL_0003 | Nombre | Interfaz de sistema |
|---|:---:|---|:---:|
| Descripción | Se vizualizará  inicialmente una instancia para poder seleccionar el usuario. Una vez seleccinado se redireccionará a una página que permita observar un mapa con los sensores y su disponibilidad. Se mostrarán además, para el caso de usuarios comunes correspondiente a los agentes de tránsito, diferentes gráficas con estadísticos que se soliciten al administrador, a modo de brindar información útil a los agentes para los controles de tránsito. |  |  |
| Prioridad | 1  | Rel. | USR_INT_0002 |
| Trazabilidad | - | Ref. | - |

####   ***5.2.3. Persistencia de datos*** 

| Código | BD_LL_0001 | Nombre | Base de datos |
|---|:---:|---|:---:|
| Descripción | Se debe contar con archivos que permitan: configuración del sistema, con un formato que permita al adminsitrador modificar de manera simple los datos; configuración de la interfaz gráfica, con el formato que le permita al administrador la amyor facilidad de modificar la interfaz gráfica de las funciones; configuración de los sensores, mediante un formato .xslx para almacenar los datos de sensores y poder conectarse al servidor; mantenimiento del sistema. |  |  |
| Prioridad | 1 | Rel. | CFG_SIS_0001 |
| Trazabilidad | - | Ref. | - |

___

##  6. Diseño del Sistema 

 Para llevar a cabo el diseño del Software requerido se opta por la Arquitectura basada en componentes con nivel de detalle. En el mismo se descompone el sistema en unidades componentes que deben tener especificadas sus entradas y salidas prescindiendo de una descripción detallada de su implementación, relacionándolos a través de conectores que especifican y gobiernan la interacción entre los mismos. Estos componentes deben encapsular funcionalidades y comportamientos, y cumplir con ciertas características como ser reutilizables en diferentes situaciones y aplicaciones, extensibles a partir de componentes existentes  para proporcionar un nuevo comportamiento y no ser específicos del contexto. Así esta metodología proporciona un mayor nivel de abstracción y divide el problema en subproblemas, cada uno asociado con una unidad componente facilitando el desarrollo del sistema pedido. Se especifican tres niveles de detalle.
- Nivel 0 (L0): Sistema simplificado con un solo objeto o bloque que describe el proyecto. Una entrada y una salida. (Opcional)
- Nivel 1 (L1): Se expande el bloque del Nivel 0 detallando a gran escala el mismo.
- Nivel 2 (L2): Se describe a mayor detalle cada bloque del nivel anterior. Exponiendo de forma resumida las tecnologías que se van a utilizar para lograr la integración.
- Nivel 3 (L3): Se documentan las decisiones realizadas por el grupo de implementación para poder llevar a cabo los requerimientos generales.

###   **6.1. Nivel 0 (L0)**

<img src="\Imagenes\sis_level0.jpg" width="250" height="80">

####  ***Sistema*** 
Se encarga de recibir la información generada por los sensores y procesar la información que llega a los diferentes usuarios.
- Entrada: información de los sensores, indicando si hay un objeto o no en la posición correspondiente.
- Salida: Mapa con información sobre la disponibilidad de los diferentes slots de estacionamiento en las calles de la ciudad. Para demás usuarios se muestran gráficas con valores estadísticos.

###   **6.2. Nivel 1 (L1)**

<img src="\Imagenes\sis_level1.jpg" width="250" height="118">

#### ***Sensores PlacePod***

PlacePod es un sensor “in-ground” o “montado en superficie” que comunicado con un gateway provee data en tiempo real de estacionamiento sobre un Área de Red Ancha de Baja Potencia (LPWAN). Brinda precisión total en detección de vehículos en espacios de estacionamiento, hasta 10 años de vida de batería y es estable en fluctuaciones de temperatura y en ambientes hostiles.
* Entrada: valores True o False, según se detecte presencia o no, respectivamente, de objetos, vehículos en este caso.

* Salida: mensajes con protocolo MQTT que siguen el standard Cayenne Low Power Payload (LPP) Format cada cierto tiempo con destino a:
    * Centro de monitoreo:
        * ID para cada sensor.
        * Estado del slot correspondiente al sensor.
        * Datos estadísticos.

    * Visualización del estado de los slots mediante mapa: Cada slot está representado por un punto en el mapa, que se pintará de color rojo o verde, según el espacio esté ocupado o libre, respectivamente. Además, está la posibilidad de indicar la zona con colores según sea la congestión de vehículos aparcados en la misma.

#### ***Arquitectura de red***

Para la implementación se utilizará una red Lora, que es compatible con estos sensores, por lo que es necesario montar una red privada. Este modelo fue seleccionado ya que estos sensores poseen compatibilidad con este modelo de comunicación.
Con Lora se envía esa información hacia la aplicación de manejo de IoT, Thingsboard, que permite manejar la información y utilizar paneles para mostrar la información estadística que se desee mostrar con las opciones que la plataforma permite.

#### ***Aplicación***

* Administrador: Soporte técnico a todo el sistema. Interactúa con la base de datos.
    * Entrada: Credenciales (usuario, contraseña).
    * Salida: por medio de una Interfaz gráfica:
        * Agregar/quitar sensores.
        * Agregar/quitar/editar paneles de visualización de la información.
        * Editar parámetros de los sensores y de las zonas en la que estos se encuentran agrupados.

* Agente de tránsito: Solo disponible para vista.
    * Entrada: Credenciales (usuario, contraseña).
    * Salida: por medio de una Interfaz gráfica:
        * Visualización de mapa con estado de los sensores e información extra mediante gráficas de valores estadísticos importantes.

* Usuario común: Solo disponible para vista.
    * Entrada: libre acceso.
    * Salida: por medio de una Interfaz gráfica:
        * *Visualización de mapa con estado de los sensores.


#### ***Centro de Monitoreo*** 

La aplicación Thingsboard es la encargada de cumplir la función de monitoreo, ya que permite recibir la información de los sensores y procesar los valores obtenidos. La base de datos consta de:
* ID de cada sensor (calle correspondiente y número de slot).
* Disponibilidad (ocupado o libre)
* Entrada: mensaje protocolo MQTT enviado por el sensor con protocolo LPP.
* Salida: por medio de una interfaz gráfica: mapa/gráficos para visualización actual del sistema.

###   **6.3. Nivel 2 (L2)**

#### ***ACA VA COMO FUNCIONARIA TODO EN LA REALIDAD (explicar como se comunica el sensor con el gateway de ahi manda la info)*** 

#### ***Aplicación***

<img src="\Imagenes\sis_level2_app.jpg" width="250" height="70">

Se desarrolla mediante Android Studio la aplicación que permitirá brindar la información proveniente de los sensores a diferentes usuarios ya específicados previamente. Se eligió este modelo ya que mediante ThingsBoard y su visualización de paneles, con un simple WebView se puede imprimir en pantalla la información procesada.

##  7. Implementación

Con lo que respecta a la implementación, es necesario aclarar que no se cuenta con los elementos “reales” para la realización, entiéndase sensores PlacePod, servidor específico de estos mismos que almacena la información; por lo que fue necesario simular todo el escenario real con herramientas auxiliares para representar la implementación del sistema. Esto implica también limitaciones al momento del cumplimiento de los ítems presentados en la etapa de diseño.

Lo primero que se pensó es cuál iba a ser el servidor que iba a recibir y procesar toda la información. En un primer momento se pensó en Cayenne, pero se presentaron muchas limitaciones al momento de mostrar los paneles necesarios, ya que era necesario contar con el sensor específico para mostrar la información como se requiere, por lo que el servidor utilizado finalmente fue Thingsboard Cloud Edition, que permitirá recibir la información pertinente, procesarla creando los paneles de visualización que muestren la información requerida para los diferentes usuarios y gestione el acceso a ellos.

Los datos que se envían al servidor se trata de datos simulados mediante el uso de una computadora de placa única Raspberry Pi, que ejecuta un script en lenguaje python y además, toma valores mediante un sensado en una maqueta representativa. También se encarga de enviar los datos al servidor mediante conexiones mediante MQTT.

Una vez hecho esto, se creó una aplicación con el software Android Studio, que permite la visualización desde una aplicación móvil de los paneles creados en Thingsboard.

###   **7.1. Implementación real teórica**

En este apartado se desarrolla cómo sería el proceso de implementación del sistema en caso de que se vaya a llevar a cabo. La explicación se denota de manera simple, ya que , como se estableció anteriormente, al no contar con el equipamiento real, la información con la que se cuenta es la que se encuentra en las páginas de los equipos o sistemas a usar sin conocer las consideraciones que se deben tener al momento de implementarlo en una situación real.

El primer paso para la implementación de este sistema, es preparar la ciudad. Específicamente, se trata de preparar las calles con slots bien específicos de estacionamiento, permitiendo así marcar la zona de detección de cada uno de los vehículos. Esto quiere decir, que para que el sistema funcione bien correctamente, los ciudadanos deberán respetar también estos espacios asignados, y estacionar correctamente en los espacios delimitados.

Con el primer paso realizado, ya se puede proceder a la activación de los sensores. Como se manifestó en la parte de diseño, los equipos elegidos son los sensores PlacePod "In-Ground", que enviarán una señal de RF a un gateway con LoRa para manejar esa información en un servidor/nube y luego se mostrará en una aplicación. Todo el proceso esta resumido en la documentación del manual de usuario de forma general, por lo que se ampliará brevemente cómo se debe implementar, apoyándose en la documentación, ya que así se pueden apreciar mejor aspectos técnicos que son requeridos[[1]](#1).

<img src="\Imagenes\impl_real.jpg" width="250" height="75">

Como estos sensores requieren de una conexión a un gateway, previamente se debe contar con un LoRa Network Gateway ya funcional. El tipo de LoRa que estos sensores requieren es del tipo Clase A.

Ahora sí, para la instalación de los sensores primero se debe fijar en el identificador de cada sensor, para poder identificarlo con cada slot, esto es mediante el código presente en la parte inferior de los mismos, donde se puede ver algo como esto:

<img src="\Imagenes\code_PP.jpg" width="250" height="116">

Una vez identificado los sensores y emparejados con la ubicación correspondiente, se pasa a la activación y calibración de los mismos. El proceso se encuentra explicado de manera más detallada y técnica en la documentación de la página de los sensores, que se enxará junto con este informa apra su visualización. Pero para dejar al lector con una idea, mediante una aplicación es posible activarlos, seleccionar la frecuencia de trabajo, la radio frecuencia a la que enviarán información a un gateway específico, calibraciones, etc[[2]](#2).

Con los sensores activados, calibrados y una vez verificado que se tiene salida hacia el gateway, se procede a la instalación de los sensores en la calle. Todo los detalles técnicos de cómo se debe instalar el sensor con las precauciones necesarias y los elementos aptos, se encuentran también en la documentación de la página correspondiente a los sensores[[3]](#3).

Con los sensores funcionales y calibrados, restaría poseer un entorno que permita visualizar toda la información generada por los sensores. La misma empresa distribuidora de sensores brinda una página que posee una interfaz gráfica con información completa de los sensores, con un mapa interactivo y gráficas de valores estadísticos. Esta interfaz está solo disponible para el administrador, pero tiene la posibilidad de generar dashboards, para generar la interfaz de los usuarios. Para más información se recomienda leer la documentación correspondiente[[4]](#4).

Para la visualización por parte de los dashboard de los usuarios, al usar cayenne, mediante la app de Cayenne Devices seguramente sea posible la visulización de la interfaz creada. Al no contar con los sensores, no se cuenta con la posibilidad de asegurar esto, pero con la documentación, se considera que es la opción que se opta en este sistema.

###   **7.2. Implementación mediante una simulación del entorno**

Para la implementación práctica del sistema, al no contar con  se usó la plataforma Thingsboard, el lenguaje de programación python, computadora de placa única Raspberry Pi y Android Studio.

El primer paso fue simular el comportamiento de los sensores mediante un script de python, el cual primero debe cargar la credencial de los dispositivos. Aquí es necesario crear los sensores en la pestaña de dispositivos, en donde a cada sensor se le asigna un nombre, un token de acceso (que es la contraseña que permite crear el cliente para enviarle información) y atributos que permitirán mostrar la información más adelante, estos son la latitud y longitud de cada uno de ellos (elegidas manualmente en este caso, por ser algo representativo). Con los dispositivos generados y los tokens de acceso asignados, ya es posible establecer una conexión con el servidor, mediante el protocolo MQTT.

Una vez que la conexión se establece, ya puede enviarse información, por lo que es necesario simular los datos que enviaría un sensor PlacePod. Para ello, en archivos de lenguaje python, mediante la generación de un vector de 6 valores 1/0 de forma aleatoria, se representó un sensor que está detectando o no presencia de objetos, respectivamente. Este vector que junta la información generada, es enviado al servidor mediante una función específica que se extrae de la documentación de Thingsboard. Esto no se hace en todo momento, sino que la información se envía cada cierto tiempo, ya que se considera que en la realidad, los datos no se actualizan en tiempo real, será cada cierto tiempo a determinar.

En resumen, este código:
* Conecta los sensores al servidor mediante credenciales.
* Simula el comportamiento de los sensores.
* Envía la información al servidor.

Luego se decidió implementar una forma más visible de lo que realiza el sistema, por lo que, con el uso de una Raspberry Pi se creó una maqueta.

<img src="\Imagenes\maq1.jpg" width="200" height="250"> 

<img src="\Imagenes\maq4.jpg" width="200" height="200">

En la Raspberry, se colocaron 6 LEDs y 2 sensores infrarrojos. La idea fue, mediante un script en python, simular el comportamiento de 4 sensores, que, según su estado generado de forma aleatoria, se prenden o apagan. Para los 2 sensores extras, se usaron los sensores infrarrojos que, según tengan o no objetos enfrente, encenderán los led correspondientes.
Este código también conecta con el servidor, pero esta vez envía los datos simulados de los 4 sensores y lo que generan los 2 infrarrojos (presencia o no de objetos).

<img src="\Imagenes\maq3.jpg" width="200" height="250">

<img src="\Imagenes\maq2.jpg" width="200" height="200">

<img src="\Imagenes\maq5.jpg" width="200" height="250">

En el caso real, la idea sería la creación de sensores magnéticos, que son más confiables a la hora de estar en ambientes extremos.

Con los dispositivos creados y ya enviada su información con el código explicado anteriormente, se maneja la información mediante el uso de Paneles, en la página de ThingsBoard. Aquí se muestra la información de los sensores, mediante mapas y gráficos, creando diferentes instancias para usuarios y agentes. 

El mapa mostrará los puntos donde se ubican los sensores, de diferente color según su estado, rojo si está ocupado y verde si está libre; y un perímetro específico coloreado según la ocupación, de modo que se pueden ver las zonas más congestionadas, para saber donde puede haber más lugares disponibles, en caso del usuario, o saber en dónde se deben realizar más controles (caso del agente). En los gráficos se muestran, en las distintas calles, la cantidad de slots que están ocupados a lo largo del tiempo.

Una vez que está todo diseñado, se crean links de acceso para los usuarios comunes, para que solo tengan permisos de vista. Para los agentes se les crea una credencial especial para que puedan ingresar a los paneles correspondientes, de modo que la visualización para ellos, es solo accesible mediante un acceso con usuario y contraseña.

Lo que aquí se realiza con ThingsBoard, en realidad se debería aplicar con un servidor LoRa tipo A, con una activación tipo OTAA (elegidos según el tipo de sistema que se quiere emplear). Se repite que, al no contar con lo necesario para realizarlo, la información fue enviada directamente al servidor.

Una vez que se verifica que todo funciona, se usa Android Studio para la visualización de los paneles de Thingsboard mediante una aplicación. 

<img src="\Imagenes\impl_app.jpg" width="175" height="200">

<img src="\Imagenes\impl_app_2.jpg" width="150" height="250">

Esta consta de un menú de inicio en el que se selecciona el tipo de usuario: agente o conductor. Según sea el usuario que se elija, se mostrarán en pantalla los paneles de Thingsboard correspondientes[[5]](#5).

<img src="\Imagenes\impl_app_inicio.jpg" width="150" height="250">

##  8. Plan de ensayos

Por último se realizó el testing al sistema desarrollado a lo largo del informe. En esta etapa se buscó evaluar y mejorar la calidad del producto a lo largo del proceso verificando el sistema mientras se ejecuta. A continuación se adjunta el documento de ensayos en el cual se muestran distintos casos de prueba en función a los requerimientos y el diseño del sistema.

## 9. Análisis de resultados



##  10. Conclusión



##  11. Anexos

#### [1] ####
*PNI PlacePod Vehicle Detection Sensor User Manual:* <https://placepod.com/wp-content/uploads/2022/02/PNI-PlacePod-Vehicle-Detection-Sensor-User-Manual-V4.1.pdf>

#### [2] ####
*PlacePod Sensor Utility Andriod User Manual:* <https://placepod.com/wp-content/uploads/2022/01/PlacePod-Sensor-Utility-Android-User-Manual.pdf>

#### [3] ####
*PlacePod Sensor Smart Parking Sensor Installation Guide:* <https://placepod.com/wp-content/uploads/2022/01/PlacePod-Smart-Parking-Sensor-Installation-Guide-V2.1.pdf>

#### [4] ####
*PNI Sensor Parking Management App User Manual:* <https://placepod.com/wp-content/uploads/2022/02/PNI-Sensor-Parking-Management-App-User-Manual-Feb2022.pdf>

#### [5] #### 
*Repositorio Git con el código python simulador de los sensores, archivos .json de paneles de thingsboard y archivo de la aplicación creada:* <https://github.com/MatiCaminati/Parking4.0.git>


