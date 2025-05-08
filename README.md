# integrador
proyecto integrador 

 **Introduccion**.
*La robótica hoy en día ha avanzado significativamente en las últimas décadas, permitiendo la creación de sistemas que imitan la anatomía y los movimientos humanos. Esta no solo tiene aplicaciones en la industria del entretenimiento y la educación, sino que también se extiende a extensos campos. En este contexto, el desarrollo de un esqueleto humanoide robótico que pueda emular los movimientos humanos se presenta como un desafío técnico y científico con una gran relevancia.\\
El presente proyecto se centra en el diseño y la implementación de un esqueleto humanoide robótico en 3D, equipado con servomotores que permiten la imitación de movimientos humanos. A pesar de que la replicación de estos movimientos no es completamente precisa y se enfrenta a un ligero retraso en la respuesta, el sistema demuestra una notable capacidad para emular la dinámica del cuerpo humano. Para lograr esta imitación, se ha integrado un sistema de visión por computadora que permite al robot detectar puntos clave del cuerpo, como muñecas, codos y hombros, facilitando así la sincronización de los movimientos.\\
La comunicación entre el sistema de visión y los actuadores del robot se realiza a través de una conexión Wi-Fi y Bluetooth, lo que permite una transmisión de datos eficiente, aunque con ciertas limitaciones en la sincronización. Además, se ha incorporado un módulo ESP32 y una pantalla LCD, que mejoran la interacción y el control del sistema, ofreciendo una interfaz más amigable para el usuario. Este proyecto no solo busca avanzar en la robótica humanoide, sino también explorar las posibilidades de interacción entre humanos y máquinas, abriendo nuevas vías para el desarrollo de tecnologías asistivas y de entretenimiento*.

***Marco teórico***.

Servomotor SG90: Un servomotor es un tipo especial de motor que
permite controlar la posición del eje en un momento dado. Esta diseñado
para moverse determinada cantidad de grados y luego mantenerse fijo en
una posición. En otras palabras, es un actuador rotativo o motor que
permite un control preciso en términos de posición angular, aceleración y
velocidad.
Figura 4.1: Microservomotor SG90.
Puente H: Es un circuito electrónico que permite invertir la polaridad
de tensión aplicada a una carga.
Figura 4.2: Puente H: L298N.
8
Motorreductor: Es un sistema que combina un reductor de velocidad
y un motor. Estos van unidos en una sola pieza y se usa para reducir la
velocidad de un equipo de forma automática.
Figura 4.3: Motorreductor con caja reductora.
Pantalla LCD ST7920 gráfica (128×64): es un tipo de pantalla de
cristal líquido que consta de 128 columnas y 64 filas de píxeles, lo que da
como resultado un total de 8192 píxeles. Estos píxeles se pueden contro-
lar individualmente para mostrar texto, imágenes e incluso animaciones
simples.
Figura 4.4: Pantalla gráfica LCD 128x64.
ESP32: es un microcontrolador desarrollado por Espressif Systems que
integra conectividad Wi-Fi y Bluetooth en un solo chip. Equipado con un
procesador de doble núcleo de 32 bits, el ESP32 es altamente eficiente en
términos de consumo de energía y rendimiento. Además, cuenta con uno
conector micro USB para comunicación y alimentación.
Figura 4.5: Placa de desarrollo ESP32.
Fuente de alimentación 9v: se utilizó una batería externa para sumi-
nistrar la energía necesaria a todos los componentes del robot.
9
SIPEED MaixDuino: es una placa de desarrollo que utiliza el módulo
M1Al como unidad central. Este módulo incorpora un procesador de doble
núcleo de 64 bits y 8 MB de SRAM. Además, está equipada con un módulo
ESP32 (Wi-Fi+Bluetooth integrado), que se conecta fácilmente a internet.
