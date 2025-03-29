Pages: https://dinastino.github.io/Simulacro_Redes/   
Respositorio: https://github.com/Dinastino/Simulacro_Redes.git

# Simulacro_Redes

## Ejercio 1: Comparación entre el Modelo OSI y el Modelo TCP/IP
### Características

- **Número de capas**:
  - Modelo OSI: 7 capas (Aplicación, Presentación, Sesión, Transporte, Red, Enlace de Datos, Física).
  - Modelo TCP/IP: 4 capas (Aplicación, Transporte, Internet, Acceso a la Red).

- **Enfoque**:
  - Modelo OSI: Modelo teórico, diseñado como referencia conceptual para el diseño de redes.
  - Modelo TCP/IP: Modelo práctico, basado en la arquitectura de Internet y en protocolos reales.

- **Capa de aplicación**:
  - Modelo OSI: Se divide en tres capas: Aplicación, Presentación y Sesión.
  - Modelo TCP/IP: Agrupa las funciones de estas tres en una única capa de Aplicación.

- **Transporte extremo a extremo**:
  - Modelo OSI: Solo soporta comunicación orientada a conexión.
  - Modelo TCP/IP: Soporta comunicación orientada a conexión (TCP) y sin conexión (UDP).

- **Manejo del control de flujo y errores**:
  - Modelo OSI: Estas funciones pueden repetirse en diferentes capas, lo que puede generar ineficiencia.
  - Modelo TCP/IP: Maneja control de flujo y errores de manera más simplificada dentro de las capas de Transporte e Internet.

- **Uso en la actualidad**:
  - Modelo OSI:Modelo de referencia para entender el funcionamiento de las redes.
  -Modelo TCP/IP: Modelo ampliamente implementado en Internet y redes reales.


### Ventajas y Limitaciones de Cada Modelo

#### Ventajas del Modelo OSI:
- Claridad conceptual: Define con precisión las funciones de cada capa.
- Modularidad: Permite diseñar y desarrollar cada capa de manera independiente.
- Estandarización: Define protocolos estandarizados internacionalmente.

#### Limitaciones del Modelo OSI:
- No implementado directamente en redes reales: Fue diseñado como referencia y no como un conjunto de protocolos específicos.
- Mayor ineficiencia: Algunas funciones, como control de flujo y direccionamiento, se repiten en varias capas.

-----

#### Ventajas del Modelo TCP/IP:
- Modelo práctico y ampliamente adoptado: Es la base de Internet y de la mayoría de redes modernas.
- Eficiente y flexible: Soporta tanto comunicación orientada a conexión (TCP) como no orientada a conexión (UDP).
- Escalabilidad: Permite la conexión entre redes heterogéneas.

#### Limitaciones del Modelo TCP/IP:
- Menos modular: No separa claramente conceptos como servicio, interfaz y protocolo, lo que puede ser problemático desde el punto de vista de ingeniería del software.
- Menor claridad en la división de funciones: Agrupa varias funciones en capas menos definidas en comparación con OSI.

---

## Ejercicio 2: Función de la Capa de Transporte

La capa de transporte es responsable de proporcionar comunicación extremo a extremo entre dispositivos en una red. Su función principal es garantizar que los datos lleguen correctamente desde el origen hasta el destino, independientemente de la red utilizada.

### 1. Capa de Transporte en el Modelo OSI

En el modelo OSI, la capa de transporte cumple las siguientes funciones:

- Abstrae a las capas superiores de los cambios tecnológicos en las capas inferiores (física, enlace y red).
- Proporciona comunicación punto a punto libre de errores, asegurando que los mensajes lleguen en el orden correcto y sin pérdidas.
- Soporta dos tipos de comunicación:
  - Mensajes punto a punto libres de errores, garantizando la entrega ordenada de los datos.
  - Mensajes aislados, donde no se garantiza el orden de entrega.
- Opera desde el nodo inicial hasta el nodo final, asegurando una transmisión confiable.
- Segmentación de datos, dividiendo la información en segmentos o datagramas según el contexto.

El modelo OSI solo soporta comunicación orientada a conexión en la capa de transporte, lo que limita algunas aplicaciones que requieren transmisión rápida sin garantía de entrega.

----

### 2. Capa de Transporte en el Modelo TCP/IP

En el modelo TCP/IP, la capa de transporte tiene dos protocolos principales:

#### TCP (Transmission Control Protocol)
- Orientado a conexión, lo que significa que se establece una sesión antes de la transmisión de datos.
- Fiabilidad: Garantiza la entrega ordenada y sin errores del flujo de datos.
- Gestión del control de flujo, evitando que un receptor lento se sature con demasiados datos.
- Se usa en aplicaciones como:
  - HTTP/HTTPS (Navegación web)
  - SMTP/IMAP/POP3 (Correo electrónico)

#### UDP (User Datagram Protocol)
- No orientado a conexión, por lo que no establece sesiones previas.
- No confiable, ya que no garantiza la entrega de los paquetes ni su orden.
- Útil para aplicaciones donde la velocidad es prioritaria sobre la fiabilidad, como:
  - Streaming de video
  - VoIP (llamadas por Internet)
  - Juegos en línea

## Ejrcicio 3: TCP vs. UDP

TCP (Transmission Control Protocol) y UDP (User Datagram Protocol) son protocolos de transporte en la capa 4 del modelo OSI. A continuación, se comparan en distintos aspectos clave:

#### 1. Orientación a conexión
- **TCP**: Es un protocolo orientado a conexión, lo que significa que antes de transmitir datos, establece una conexión entre el emisor y el receptor mediante un proceso llamado *three-way handshake* (SYN, SYN-ACK, ACK).
- **UDP**: Es un protocolo sin conexión (*connectionless*), lo que implica que no requiere establecer una conexión previa antes de enviar los datos.

#### 2. Fiabilidad y control de errores
- **TCP**: Proporciona fiabilidad mediante la verificación de errores, control de flujo y retransmisión de paquetes perdidos. También garantiza que los datos lleguen en el orden correcto.
- **UDP**: No ofrece mecanismos de control de errores ni de retransmisión. Si un paquete se pierde o llega dañado, no hay reenvío automático.

#### 3. Velocidad y orden de entrega
- **TCP**: Es más lento debido a sus mecanismos de control, como la verificación de errores y la gestión del flujo de datos. Sin embargo, garantiza que los datos lleguen en el orden correcto.
- **UDP**: Es más rápido porque no tiene sobrecarga de control de flujo ni confirmación de entrega. Sin embargo, los paquetes pueden llegar desordenados o perderse.

#### 4. Ejemplos de aplicaciones
- **TCP**: Se usa en aplicaciones que requieren fiabilidad y entrega ordenada de datos, como:
  - Navegación web (HTTP/HTTPS)
  - Transferencia de archivos (FTP)
  - Correo electrónico (SMTP, IMAP, POP3)
  - Protocolos de control remoto (SSH, Telnet)

- **UDP**: Se emplea en aplicaciones donde la velocidad es más importante que la fiabilidad, como:
  - Streaming de video y audio (Netflix, YouTube, VoIP)
  - Juegos en línea
  - Servicios de DNS (Domain Name System)
  - Protocolo de transmisión de video en tiempo real (RTP)

## Ejercicio 4: Protocolo para Transferencia de Archivos
### a) ¿Qué protocolo de la capa de aplicación se utiliza tradicionalmente para la transferencia de archivos en redes TCP/IP?

El protocolo de la capa de aplicación utilizado tradicionalmente para la transferencia de archivos en redes TCP/IP es **FTP (File Transfer Protocol)**. Este protocolo permite la transferencia de archivos entre un cliente y un servidor, utilizando los puertos 20 y 21 para la comunicación.

### b) Menciona al menos dos alternativas a este protocolo, resaltando sus diferencias principales en cuanto a seguridad o funcionalidad.

1. **SFTP (Secure File Transfer Protocol)**  
   - A diferencia de FTP, SFTP utiliza el protocolo **SSH (Secure Shell)** para cifrar la transferencia de archivos, proporcionando mayor seguridad.  
   - Opera sobre un solo puerto (por defecto, el puerto 22), lo que facilita la configuración en cortafuegos y NAT.  
   - Proporciona autenticación segura y cifrado de datos, evitando ataques de tipo "man-in-the-middle".

2. **HTTP/HTTPS (HyperText Transfer Protocol / Secure)**  
   - Aunque no está diseñado exclusivamente para la transferencia de archivos, **HTTP** y **HTTPS** se utilizan ampliamente para descargar archivos desde servidores web.  
   - **HTTPS** añade seguridad mediante **TLS/SSL**, cifrando los datos transmitidos.  
   - Es ideal para transferencias en entornos donde los navegadores web son la principal interfaz de acceso a archivos.








