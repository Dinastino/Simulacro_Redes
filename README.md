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