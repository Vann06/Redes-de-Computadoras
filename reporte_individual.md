# Reporte Individual – Laboratorio 1  
## Introducción a Wireshark

---

### Información general

| Campo | Información |
|---|---|
| Nombre completo | [Nombre del integrante 1] |
| Carnet | [Carnet integrante 1] |
| Curso | [Nombre del curso] |
| Laboratorio | Laboratorio 1 |
| Docente | [Nombre del docente] |
| Fecha de realización | [DD/MM/AAAA] |
| Fecha de entrega | [DD/MM/AAAA] |
| Repositorio de GitHub | [Pegar enlace] |

---

## 1. Introducción

[Explique brevemente en qué consistió el laboratorio. Mencione la personalización del entorno de Wireshark, la configuración de una captura mediante ring buffer y el análisis de tráfico HTTP.]

---

## 2. Objetivos

- Familiarizarse con el entorno de Wireshark.
- Personalizar un perfil de trabajo.
- Configurar columnas, paneles, filtros y reglas de color.
- Identificar las interfaces de red del equipo.
- Realizar capturas mediante un ring buffer.
- Analizar paquetes HTTP reales.
- Relacionar la teoría de redes con información capturada.

---

## 3. Datos del equipo utilizado

| Elemento | Información |
|---|---|
| Sistema operativo | [Windows / Linux / macOS] |
| Versión del sistema | [Versión] |
| Versión de Wireshark | [Versión] |
| Tipo de conexión | [WiFi / Ethernet] |
| Navegador utilizado | [Nombre y versión] |
| Interfaz de captura | [Nombre de la interfaz] |

---

## 4. Personalización del entorno de Wireshark

### 4.1 Creación del perfil

**Nombre del perfil:** `[Primer nombre y primer apellido]`

**Procedimiento realizado:**  
[Explique cómo creó el perfil desde `Edit > Configuration Profiles`.]

![Perfil creado](evidencias/individual_1/01_perfil.png)

**Descripción de la evidencia:**  
[Indique dónde se observa el nombre del perfil.]

---

### 4.2 Apertura del archivo de captura

**Archivo utilizado:** `intro-wireshark-trace1.pcap`

[Explique cómo abrió el archivo y qué información general observó.]

![Archivo PCAP abierto](evidencias/individual_1/02_archivo_pcap.png)

**Descripción:** [Detalle lo que muestra la captura.]

---

### 4.3 Formato de tiempo

**Formato seleccionado:** `Time of Day`

**Ruta utilizada:** `View > Time Display Format > Time of Day`

![Formato de tiempo](evidencias/individual_1/03_formato_tiempo.png)

**Descripción:** [Indique cómo se evidencia el cambio.]

---

### 4.4 Columna de longitud del protocolo

**Nombre asignado a la columna:** [Nombre]

**Tipo de columna seleccionado:** [Tipo]

[Explique cómo agregó la columna y cómo ocultó la columna original de longitud.]

![Nueva columna](evidencias/individual_1/04_columna_protocolo.png)

**Descripción:** [Explique qué columna se agregó y cuál se ocultó.]

---

### 4.5 Diseño de paneles

**Diseño seleccionado:** [Describa el diseño]

**Justificación:**  
[Explique por qué eligió este diseño y cómo facilita el análisis.]

![Diseño de paneles](evidencias/individual_1/05_layout.png)

---

### 4.6 Regla de color para paquetes TCP SYN

**Filtro utilizado:**

```wireshark
tcp.flags.syn == 1
```

**Color seleccionado:** [Color]

[Explique cómo creó la regla desde `View > Coloring Rules`.]

![Regla de color](evidencias/individual_1/06_regla_color.png)

**Descripción:** [Señale los paquetes resaltados.]

---

### 4.7 Botón de filtro TCP SYN

**Nombre del botón:** [Nombre]

**Expresión utilizada:**

```wireshark
tcp.flags.syn == 1
```

![Botón de filtro](evidencias/individual_1/07_boton_filtro.png)

**Descripción:** [Explique cómo se valida que el botón funciona.]

---

### 4.8 Interfaces de captura

[Indique cuáles interfaces virtuales ocultó y cuál interfaz dejó habilitada.]

| Interfaz | Tipo | Estado | Razón |
|---|---|---|---|
| [Interfaz] | [Física/Virtual] | [Visible/Oculta] | [Explicación] |
| [Interfaz] | [Física/Virtual] | [Visible/Oculta] | [Explicación] |
| [Interfaz] | [Física/Virtual] | [Visible/Oculta] | [Explicación] |

![Lista de interfaces](evidencias/individual_1/08_interfaces.png)

---

## 5. Configuración de la captura de paquetes

### 5.1 Resultado de `ipconfig` o `ifconfig`

**Comando utilizado:**

```bash
[ipconfig / ifconfig / ip addr]
```

**Resultado relevante:**

```text
[Pegue únicamente las líneas necesarias. Puede ocultar información sensible.]
```

### Explicación de lo observado

| Dato | Valor observado | Explicación |
|---|---|---|
| Dirección IPv4 | [Valor] | [Explicación] |
| Máscara de subred | [Valor] | [Explicación] |
| Puerta de enlace | [Valor] | [Explicación] |
| Dirección MAC | [Valor] | [Explicación] |
| Interfaz activa | [Valor] | [Explicación] |
| Dirección IPv6 | [Valor, si aplica] | [Explicación] |

![Comando de red](evidencias/individual_1/09_comando_red.png)

**Nota de privacidad:**  
[Indique si ocultó parcialmente alguna dirección o dato antes de publicar la captura.]

---

### 5.2 Configuración del ring buffer

| Parámetro | Configuración |
|---|---|
| Interfaz | [WiFi/Ethernet] |
| Tamaño máximo por archivo | 5 MB |
| Número máximo de archivos | 10 |
| Nombre base | `lab1_[Carnet integrante 1].pcap` |
| Método utilizado | [Interfaz gráfica / línea de comandos] |

#### Configuración mediante interfaz gráfica

[Explique los pasos seguidos en Wireshark.]

#### Configuración mediante comando, si aplica

```bash
[Pegue aquí el comando utilizado]
```

![Configuración del ring buffer](evidencias/individual_1/10_ring_buffer_config.png)

**Descripción:** [Explique dónde se observan los valores de 5 MB y 10 archivos.]

---

### 5.3 Archivos generados

| No. | Nombre del archivo | Tamaño | Observaciones |
|---:|---|---:|---|
| 1 | [Nombre] | [Tamaño] | [Comentario] |
| 2 | [Nombre] | [Tamaño] | [Comentario] |
| 3 | [Nombre] | [Tamaño] | [Comentario] |
| 4 | [Nombre] | [Tamaño] | [Comentario] |
| 5 | [Nombre] | [Tamaño] | [Comentario] |

![Archivos generados](evidencias/individual_1/11_archivos_ring_buffer.png)

**Descripción:** [Indique cómo se evidencia la rotación de archivos.]

---

## 6. Análisis de paquetes HTTP

### 6.1 Procedimiento

1. Se inició una captura sin filtros.
2. Se abrió el navegador.
3. Se accedió a la dirección indicada en la guía.
4. Se detuvo la captura.
5. Se aplicó el filtro HTTP.
6. Se identificaron las solicitudes y respuestas relevantes.

**Filtro utilizado:**

```wireshark
http
```

![Tráfico HTTP identificado](evidencias/individual_1/12_http_general.png)

---

### 6.2 Solicitud HTTP del navegador

**Paquete número:** [Número]

![Solicitud HTTP](evidencias/individual_1/13_http_request.png)

#### a. ¿Qué versión de HTTP está ejecutando el navegador?

**Respuesta:** [HTTP/1.0, HTTP/1.1, HTTP/2 u otra]

**Evidencia y explicación:**  
[Indique el campo o línea del paquete donde encontró la versión.]

---

#### c. ¿Qué lenguajes indica el navegador que acepta?

**Respuesta:** [Ejemplo: es-ES, es, en-US, en]

**Campo analizado:** `Accept-Language`

![Accept-Language](evidencias/individual_1/14_accept_language.png)

**Explicación:**  
[Explique qué significan los valores observados.]

---

### 6.3 Respuesta HTTP del servidor

**Paquete número:** [Número]

![Respuesta HTTP](evidencias/individual_1/15_http_response.png)

#### b. ¿Qué versión de HTTP está ejecutando el servidor?

**Respuesta:** [Versión]

**Evidencia y explicación:**  
[Indique la línea de estado observada.]

---

#### d. ¿Cuántos bytes de contenido fueron devueltos por el servidor?

**Respuesta:** [Cantidad] bytes

**Campo analizado:** `Content-Length`

![Content-Length](evidencias/individual_1/16_content_length.png)

**Explicación:**  
[Explique la diferencia, si aplica, entre el tamaño total del paquete y el contenido HTTP.]

---

### 6.4 Análisis de un problema de rendimiento

#### e. Si existiera un problema de rendimiento durante la descarga, ¿en qué elementos de la red convendría escuchar los paquetes?

[Analice, como mínimo, los siguientes puntos:]

- Equipo cliente.
- Puerta de enlace o router local.
- Enlace entre redes.
- Firewall o proxy.
- Balanceador de carga, si existe.
- Servidor de destino.
- Puntos antes y después del elemento sospechoso.

#### ¿Es conveniente instalar Wireshark directamente en el servidor?

**Respuesta:** [Sí / No / Depende]

**Justificación:**  
[Explique los beneficios y riesgos. Puede mencionar consumo de recursos, permisos, seguridad, volumen de tráfico y alternativas como capturas remotas, port mirroring o TAP de red.]

---

## 7. Resumen de respuestas

| Pregunta | Respuesta |
|---|---|
| Versión HTTP del navegador | [Respuesta] |
| Versión HTTP del servidor | [Respuesta] |
| Lenguajes aceptados | [Respuesta] |
| Bytes devueltos | [Respuesta] |
| Mejor punto de captura | [Respuesta resumida] |
| ¿Instalar Wireshark en el servidor? | [Respuesta resumida] |

---

## 8. Discusión de la actividad

### 8.1 Experiencia en la primera parte

[Comente su experiencia con los códigos Morse y Baudot, la transmisión empaquetada y la conmutación de mensajes.]

### 8.2 Experiencia con Wireshark

[Describa qué partes fueron fáciles, cuáles fueron difíciles y qué funciones de Wireshark le parecieron más útiles.]

### 8.3 Hallazgos principales

- [Hallazgo 1]
- [Hallazgo 2]
- [Hallazgo 3]
- [Hallazgo 4]

### 8.4 Problemas encontrados y solución aplicada

| Problema | Posible causa | Solución aplicada | Resultado |
|---|---|---|---|
| [Problema] | [Causa] | [Solución] | [Resultado] |
| [Problema] | [Causa] | [Solución] | [Resultado] |

### 8.5 Aprendizaje obtenido

[Explique qué aprendió sobre paquetes, protocolos, interfaces, filtros, capturas y análisis de tráfico.]

---

## 9. Conclusiones

1. [Conclusión sobre la personalización y uso de Wireshark.]
2. [Conclusión sobre las interfaces y la configuración de captura.]
3. [Conclusión sobre el ring buffer.]
4. [Conclusión sobre el protocolo HTTP.]
5. [Conclusión general del laboratorio.]

---

## 10. Referencias


---