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

---

### Ventajas y Limitaciones de Cada Modelo

#### Ventajas del Modelo OSI:
- Claridad conceptual: Define con precisión las funciones de cada capa.
- Modularidad: Permite diseñar y desarrollar cada capa de manera independiente.
- Estandarización: Define protocolos estandarizados internacionalmente.

#### Limitaciones del Modelo OSI:
- No implementado directamente en redes reales: Fue diseñado como referencia y no como un conjunto de protocolos específicos.
- Mayor ineficiencia: Algunas funciones, como control de flujo y direccionamiento, se repiten en varias capas.

---

#### Ventajas del Modelo TCP/IP:
- Modelo práctico y ampliamente adoptado: Es la base de Internet y de la mayoría de redes modernas.
- Eficiente y flexible: Soporta tanto comunicación orientada a conexión (TCP) como no orientada a conexión (UDP).
- Escalabilidad: Permite la conexión entre redes heterogéneas.

#### Limitaciones del Modelo TCP/IP:
- Menos modular: No separa claramente conceptos como servicio, interfaz y protocolo, lo que puede ser problemático desde el punto de vista de ingeniería del software.
- Menor claridad en la división de funciones: Agrupa varias funciones en capas menos definidas en comparación con OSI.
