# integrador
proyecto integrador 

 **Introduccion**.
*La robótica hoy en día ha avanzado significativamente en las últimas décadas, permitiendo la creación de sistemas que imitan la anatomía y los movimientos humanos. Esta no solo tiene aplicaciones en la industria del entretenimiento y la educación, sino que también se extiende a extensos campos. En este contexto, el desarrollo de un esqueleto humanoide robótico que pueda emular los movimientos humanos se presenta como un desafío técnico y científico con una gran relevancia.\\
El presente proyecto se centra en el diseño y la implementación de un esqueleto humanoide robótico en 3D, equipado con servomotores que permiten la imitación de movimientos humanos. A pesar de que la replicación de estos movimientos no es completamente precisa y se enfrenta a un ligero retraso en la respuesta, el sistema demuestra una notable capacidad para emular la dinámica del cuerpo humano. Para lograr esta imitación, se ha integrado un sistema de visión por computadora que permite al robot detectar puntos clave del cuerpo, como muñecas, codos y hombros, facilitando así la sincronización de los movimientos.\\
La comunicación entre el sistema de visión y los actuadores del robot se realiza a través de una conexión Wi-Fi y Bluetooth, lo que permite una transmisión de datos eficiente, aunque con ciertas limitaciones en la sincronización. Además, se ha incorporado un módulo ESP32 y una pantalla LCD, que mejoran la interacción y el control del sistema, ofreciendo una interfaz más amigable para el usuario. Este proyecto no solo busca avanzar en la robótica humanoide, sino también explorar las posibilidades de interacción entre humanos y máquinas, abriendo nuevas vías para el desarrollo de tecnologías asistivas y de entretenimiento*.

***Marco teórico***.

**Servomotor SG90:** *Un servomotor es un tipo especial de motor que
permite controlar la posición del eje en un momento dado. Esta diseñado
para moverse determinada cantidad de grados y luego mantenerse fijo en
una posición. En otras palabras, es un actuador rotativo o motor que
permite un control preciso en términos de posición angular, aceleración y
velocidad*.

**Puente H:** *Es un circuito electrónico que permite invertir la polaridad
de tensión aplicada a una carga.*
**Motorreductor:** *Es un sistema que combina un reductor de velocidad
y un motor. Estos van unidos en una sola pieza y se usa para reducir la
velocidad de un equipo de forma automática*.

**Pantalla LCD ST7920 gráfica (128×64):** *Es un tipo de pantalla de
cristal líquido que consta de 128 columnas y 64 filas de píxeles, lo que da
como resultado un total de 8192 píxeles. Estos píxeles se pueden contro-
lar individualmente para mostrar texto, imágenes e incluso animaciones
simples*.

**ESP32:** *Es un microcontrolador desarrollado por Espressif Systems que
integra conectividad Wi-Fi y Bluetooth en un solo chip. Equipado con un
procesador de doble núcleo de 32 bits, el ESP32 es altamente eficiente en
términos de consumo de energía y rendimiento. Además, cuenta con uno
conector micro USB para comunicación y alimentación*.

**Fuente de alimentación 9v:** *Se utilizó una batería externa para sumi-
nistrar la energía necesaria a todos los componentes del robot*.

**SIPEED MaixDuino:** *es una placa de desarrollo que utiliza el módulo
M1Al como unidad central. Este módulo incorpora un procesador de doble
núcleo de 64 bits y 8 MB de SRAM. Además, está equipada con un módulo
ESP32 (Wi-Fi+Bluetooth integrado), que se conecta fácilmente a internet*.




**Reconocimiento eficiente usando MediaPipe OpenCV**

*La visión por computadora es un campo que permite a los equipos infor-
máticos interpretar y comprender su entorno. A través del uso de algoritmos
avanzados y técnicas de aprendizaje automático, estos sistemas son capaces de
analizar imágenes y videos para llevar a cabo tareas complejas, como la detec-
ción de rostros y cuerpos humanos. En el desarrollo de este proyecto, se empleó
la biblioteca OpenCV debido a su eficiencia en el procesamiento de video.
La función cv2.VideoCapture() es esencial para capturar un vídeo desde una
cámara, basta con crear un objeto que contenga dicha función y pasar como
argumento el índice de cámara (0 para la cámara predeterminada)*.

*La estimación de la postura humana es el proceso de detección y seguimien-
to de puntos de referencia del cuerpo humano en imágenes y vídeos, para esta
técnica de visión artificial se utilizó MediaPipe. Los puntos clave detectados
suelen incluir articulaciones como codos, rodillas, hombros y tobillos.
MediaPipe es un marco de aprendizaje automático multiplataforma y de código
abierto. Uno de sus modelos, MediaPipe Stance, es capaz de identificar hasta
33 puntos de referencia en 3D del cuerpo humano, como la cabeza, los hombros,
los codos, las muñecas, las manos y las caderas, lo que permite estimar con
precisión la postura de una persona*.
*A continuación, se describen los pasos para la detección de puntos de refe-
rencia utilizando MediaPipe:*
*1. Inicialización de MediaPipe Pose: Se importa y se inicializa el modelo
mp_pose.Pose() de MediaPipe para detectar los puntos de referencia del
cuerpo humano*.
*2. Detección de puntos de referencia (landmarks): El marco de video
se convierte a formato RGB (cv2.cvtColor(frame, cv2.COLOR_BGR2RGB))
para que pueda ser procesado por MediaPipe*.
*3. Comprobación de detección de cuerpo: Si results.pose_landmarks
contiene datos, significa que MediaPipe ha detectado al menos un cuerpo
humano*.
*4. Conexiones de la parte superior del cuerpo: Para cada par de pun-
tos, se obtienen sus coordenadas y se traza una línea entre ellos utilizando
cv2.line(), visualizando así las conexiones entre esos puntos del cuerpo.
5. Dibujo de puntos de referencia: Para cada punto de referencia*.

**Comunicación python-LCD128x64 ST7920**
*Python en un entorno utilizado con Spyder que puede enviar datos a un
microcontrolador a través de comunicación serial. Este microcontrolador procesa
esos datos y los utiliza para mostrar información en una pantalla LCD ST7920.
SPI es el protocolo utilizado entre el microcontrolador y la pantalla para la
comunicación rápida y eficiente*.

**Código de reconocimiento facial**
*Este proyecto combina reconocimiento facial con visualización en pantalla
LCD, asi como Python con OpenCV este se encarga de realizar el reconocimiento
facial y Python envía el nombre de la persona reconocida al microcontrolador
(ESP32) a través de comunicación serial donde muestra el nombre en la pantalla
LCD*.
**Demostración de reconocimiento de rostros**
*Se muestra un mensaje de la persona que esta detectando en el algoritmo
diseñado en python y este mismo se visualiza en la cara del robot para que
muestre el nombre entre otros diseños*.

**Seguimiento de persona con Arduino IDE**
*Este código está diseñado para controlar un robot móvil que sigue a una
persona utilizando un sensor ultrasónico y sensores infrarrojos. El robot ajusta
su dirección de movimiento en función de la posición de la persona, girando
hacia donde ella se mueve*.
*NewPing: Es una bliblioteca que facilita la interacción con el sensor ultrasó-
nico, que mide la distancia a un objeto*.
**Lógica de Control**
*Lectura de Sensores Infrarrojos: Se leen los valores de los sensores in-
frarrojos izquierdo y derecho*.
*Si el objeto está demasiado cerca (menos de 15 cm), se detienen los mo-
tores.
Si el objeto está demasiado lejos (más de 25 cm), el robot avanza hacia
adelante*.
*Si la distancia es adecuada (entre 15 cm y 25 cm), se verifica la información
de los sensores infrarrojos para mantense pendientes*.

**Medición de Distancia:** *Se mide la distancia a la persona utilizando el
sensor ultrasónico y se imprime en el monitor serial*.

**Reconocimiento de rostro con micropython**
*En esta sección se utiliza un nuevo ide MaixPy es un firmware de Mi-
croPython diseñado para placas de desarrollo como la Sipeed Maix Bit y Maix-
CAM. Proporciona una base para el procesamiento de AIoT (Internet de las
cosas con inteligencia artificial) y el procesamiento de imágenes en dispositi-
vos de bordes. Incluye una variedad de bibliotecas de funciones a las que los
desarrolladores pueden llamar directamente y utiliza la sintaxis de scripts de
MicroPython, permitiendo a los desarrolladores editar scripts en tiempo real en
su computadora y cargarlos en la placa de desarrollo*.

**Intalación de Firmware MaixPy**
*La instalación es esencial para que los dispositivos funcionen correctamente
y comunicarse con elementos de un sistema más amplio, sin interactuar direc-
tamente con el usuario*.
 **Configuración de kflash-gui**
*Es una interfaz gráfica de usuario (GUI) para la herramienta kflash.py, que
se utiliza para descargar (o quemar) firmware en dispositivos K210. Es una he-
rramienta cruzada de plataforma que permite a los usuarios seleccionar archivos
binarios o kfpkg, y establecer la dirección de destino para el firmware. También
soporta la fusión de múltiples archivos binarios en uno solo y la conversión de
archivos kfpkg a binarios*.
**Interface Maixpy**
*Se crea el primer código de prueba para observar la conexión de SIPEED
MaixDuino y observar el funcionamiento de la cámara en el ide maixpy, donde
se estara migrando los algoritmos realizados para la detección de rostros*.


