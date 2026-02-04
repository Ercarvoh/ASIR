

### 1. Ejercicio 
Si emites un streaming de audio a un bitrate constante (**CBR**) de **128 kbps** y tienes **25 oyentes** simultáneos en una red **Unicast**, ¿cuál es el ancho de banda total consumido?

---

### 🔍 Explicación Paso a Paso

1.  **Identificar el tipo de red (Unicast):**
    En el modelo **Unicast**, el servidor establece una conexión única para cada cliente. Esto significa que el ancho de banda se multiplica por el número de usuarios.
    > **Fórmula:** $Ancho \text{ de banda total} = Bitrate \times Usuarios$

2.  **Realizar el cálculo en kbps:**
    Multiplicamos el bitrate individual por la cantidad de oyentes:
    $$128 \text{ kbps} \times 25 \text{ oyentes} = 3.200 \text{ kbps}$$

3.  **Conversión de unidades (kbps a Mbps):**
    Para obtener un resultado más legible (y que coincida con las opciones del examen), dividimos entre **1.000**:
    $$3.200 / 1.000 = \mathbf{3,2 \text{ Mbps}}$$

---

### ✅ Respuesta Correcta

La respuesta correcta es la **c. 3.2 Mbps**.

#### 💡 Análisis de las opciones:
* **a. 25 Mbps:** Incorrecto. No se multiplica el número de usuarios por 1 Mbps.
* **b. 3200 Mbps:** Incorrecto. El número es correcto, pero la unidad (Mega) es demasiado grande. Serían 3200 **kbps**.
* **c. 3.2 Mbps:** **CORRECTO**.
* **d. 128 kbps:** Incorrecto. Este sería el ancho de banda si solo hubiera **1 oyente** o si la red fuera **Multicast**.



### 2. Ejercicio 
Tienes un disco de **500 GB**. ¿Cuántas horas de vídeo **HD a 2 Mbps** podrías alojar aproximadamente?

---

### 🔍 Resolución Paso a Paso

Para resolver esto, primero debemos saber cuánto "pesa" una hora de ese vídeo y luego ver cuántas veces cabe en el disco.

#### 1. Calcular cuánto ocupa 1 hora de vídeo (en Gigabytes)
* **Paso A (Tiempo a segundos):** $1 \text{ hora} = 3.600 \text{ segundos}$.
* **Paso B (Peso en Megabits):** $2 \text{ Mbps} \times 3.600 \text{ seg} = 7.200 \text{ Megabits (Mb)}$.
* **Paso C (Cruzar el puente de bits a Bytes):** $7.200 \text{ Mb} / 8 = 900 \text{ Megabytes (MB)}$.
* **Paso D (Pasar a Gigabytes):** $900 \text{ MB} / 1.000 = \mathbf{0,9 \text{ GB}}$.
  *(Por lo tanto, cada hora de vídeo ocupa 0,9 GB).*

#### 2. Calcular cuántas horas caben en el disco
Dividimos la capacidad total del disco entre lo que ocupa una hora:
$$\text{Total horas} = \frac{500 \text{ GB}}{0,9 \text{ GB/hora}} = \mathbf{555,55 \text{ horas}}$$

---

### ✅ Respuesta Correcta

La respuesta más aproximada es la **a. 555 horas**.

#### 💡 Por qué fallan las otras:
* **b. 1000 horas:** Es el error de no dividir entre 8 (500 / 0.5 Mbps si no se hiciera el cambio de bits a Bytes).
* **c. 250 horas:** No corresponde a la división correcta.
* **d. 277 horas:** Es un error común de cálculo si se divide mal el bitrate inicial.

### 3. Ejercicio: Cálculo de Bitrate de Audio (LPCM)

**Enunciado:** ¿Cuál es el bitrate de un flujo de audio que utiliza una frecuencia de muestreo de **48 kHz**, una profundidad de **24 bits** y un solo canal (**mono**)?

**Paso a paso:**

1. **Identificar la fórmula del Bitrate de audio:**
   $Bitrate = Frecuencia \text{ de muestreo} \times Profundidad \text{ de bit} \times \text{Nº de canales}$.

2. **Sustituir con los datos del enunciado:**
   $48.000 \text{ Hz} \times 24 \text{ bits} \times 1 \text{ canal} = 1.152.000 \text{ bits por segundo (bps)}$.

3. **Convertir a kilobits por segundo (kbps):**
   Dividimos entre 1.000:
   $1.152.000 / 1.000 = \mathbf{1.152 \text{ kbps}}$.

4. **Convertir a Megabits por segundo (Mbps):**
   Dividimos entre 1.000 otra vez:
   $1.152 / 1.000 = \mathbf{1,152 \text{ Mbps}}$.

**Respuesta correcta:**
**b. 1.152 Mbps**

### 4. Ejercicio: Cálculo de almacenamiento para vídeo de alto bitrate

**Enunciado:** Con un bitrate de **14,93 Gbps**, ¿cuánto espacio de disco ocupará una toma de **10 segundos**?

**Paso a paso:**

1. **Calcular el peso total en Gigabits (Gb):**
   Multiplicamos el bitrate por el tiempo de la toma:
   $14,93 \text{ Gbps} \times 10 \text{ segundos} = 149,3 \text{ Gigabits (Gb)}$.

2. **Cruzar el puente de bits a Bytes (Dividir entre 8):**
   Para saber cuánto ocupa en el disco (Gigabytes), debemos dividir el total de bits entre 8:
   $149,3 / 8 = \mathbf{18,6625 \text{ Gigabytes (GB)}}$.

3. **Verificar la unidad resultante:**
   El resultado directo de la operación anterior ya está en GB, que es una de las opciones de la lista.

**Respuesta correcta:**
**b. 18.66 GB**

### 5. Ejercicio: Cálculo de peso de audio WAV (Calidad CD)

**Enunciado:** Calcula el peso aproximado de un archivo de audio WAV de **5 minutos**, con **44.1 kHz**, **16 bits** y **estéreo**.

**Paso a paso:**

1. **Convertir el tiempo a segundos:**
   $5 \text{ minutos} \times 60 \text{ segundos} = 300 \text{ segundos}$.

2. **Calcular el Bitrate (bps):**
   Multiplicamos frecuencia $\times$ profundidad $\times$ canales (estéreo = 2):
   $44.100 \text{ Hz} \times 16 \text{ bits} \times 2 \text{ canales} = 1.411.200 \text{ bits por segundo (bps)}$.

3. **Calcular el peso total en bits:**
   $1.411.200 \text{ bps} \times 300 \text{ segundos} = 423.360.000 \text{ bits}$.

4. **Pasar de bits a Bytes (Dividir entre 8):**
   $423.360.000 / 8 = 52.920.000 \text{ Bytes (B)}$.

5. **Convertir a Megabytes (MB):**
   Dividimos entre 1.000.000 (o dos veces entre 1.000):
   $52.920.000 / 1.000.000 = \mathbf{52,92 \text{ MB}}$.

**Respuesta correcta:**
**a. 50.47 MB** *(Nota: Es la opción más cercana; la diferencia decimal suele deberse a si el profesor usa 1024 o 1000 en el último paso).*


### 6. Ejercicio: Cálculo de Bitrate Vídeo 4K RAW

**Enunciado:** Un estudio graba en **RAW** a **3840x2160**, a **60 fps** y **30 bits** de color. ¿Cuál es el bitrate resultante en **Gbps**?

**Paso a paso:**

1. **Calcular el total de píxeles por cuadro:**
   $3840 \times 2160 = 8.294.400 \text{ píxeles}$.

2. **Calcular los bits por segundo (bps):**
   Multiplicamos: Píxeles $\times$ Profundidad de color $\times$ FPS.
   $8.294.400 \times 30 \text{ bits} \times 60 \text{ fps} = 14.929.920.000 \text{ bps}$.

3. **Convertir a Gigabits por segundo (Gbps):**
   Dividimos entre 1.000.000.000 (o tres veces entre 1.000):
   $14.929.920.000 / 1.000.000.000 = \mathbf{14,93 \text{ Gbps}}$.

**Respuesta correcta:**
**b. 14.93 Gbps**

### 7. Ejercicio: Capacidad de usuarios en red (Unicast)

**Enunciado:** En una línea de **100 Mbps simétricos**, ¿cuántos usuarios podrían ver un streaming de vídeo de **2 Mbps**?

**Paso a paso:**

1. **Identificar el tipo de cálculo:**
   Estamos calculando la capacidad de una red para servir flujos individuales (Unicast). Debemos dividir el ancho de banda total disponible entre lo que consume cada flujo.

2. **Verificar que las unidades coinciden:**
   * Ancho de banda total: $100 \text{ Mbps}$
   * Bitrate del vídeo: $2 \text{ Mbps}$
   (Ambas están en Megabits por segundo, así que no hace falta convertir nada).

3. **Realizar la división:**
   $\text{Usuarios} = \frac{\text{Ancho de banda total}}{\text{Bitrate por usuario}}$
   $100 / 2 = \mathbf{50 \text{ usuarios}}$.

**Respuesta correcta:**
**a. 50 usuarios**

### 8. Ejercicio: Saturación de Ancho de Banda (Subida)

**Enunciado:** Si 4 alumnos emiten a **6 Mbps cada uno** en una línea de **20 Mbps de subida**, ¿qué ocurrirá?

**Paso a paso:**

1. **Calcular la demanda total de la red:**
   Cada alumno es un emisor independiente. Debemos sumar sus bitrates individuales:
   $4 \text{ alumnos} \times 6 \text{ Mbps/alumno} = \mathbf{24 \text{ Mbps}}$.

2. **Comparar con la capacidad disponible:**
   * Demanda: $24 \text{ Mbps}$
   * Capacidad de subida: $20 \text{ Mbps}$

3. **Analizar el resultado:**
   Como la demanda ($24$) es mayor que la capacidad ($20$), la línea no puede transportar todos los datos en tiempo real. Esto genera un cuello de botella.

4. **Identificar la consecuencia técnica:**
   Cuando los paquetes de datos no pueden salir a la velocidad necesaria, se produce **latencia** y **buffering** (parones), ya que el servidor no recibe la información completa a tiempo.

**Respuesta correcta:**
**a. La red se saturará (24 Mbps requeridos) provocando buffering.**

### 9. Ejercicio: Cálculo de porcentaje de uso de red

**Enunciado:** Si tienes una conexión de **20 Mbps de subida** y emites vídeo a **6 Mbps**, ¿qué porcentaje de tu línea estás utilizando?

**Paso a paso:**

1. **Identificar los valores:**
   * Capacidad total (100%): $20 \text{ Mbps}$.
   * Consumo actual: $6 \text{ Mbps}$.

2. **Aplicar la fórmula del porcentaje:**
   $\text{Porcentaje} = \left( \frac{\text{Uso actual}}{\text{Capacidad total}} \right) \times 100$

3. **Realizar el cálculo:**
   $\frac{6}{20} = 0,3$
   $0,3 \times 100 = \mathbf{30\%}$.

**Respuesta correcta:**
**b. 30%**

### 10. Ejercicio: Límite de oyentes por ancho de banda

**Enunciado:** Un servidor tiene un límite de subida de **10 Mbps**. ¿Cuántos oyentes simultáneos puede soportar si cada uno consume **192 kbps**?

**Paso a paso:**

1. **Igualar las unidades:**
   Para poder dividir, ambos datos deben estar en la misma unidad. Pasamos los Mbps del servidor a kbps:
   $10 \text{ Mbps} \times 1.000 = \mathbf{10.000 \text{ kbps}}$.

2. **Aplicar la fórmula de capacidad (Unicast):**
   $\text{Nº de oyentes} = \frac{\text{Ancho de banda total}}{\text{Bitrate por oyente}}$

3. **Realizar el cálculo:**
   $10.000 \text{ kbps} / 192 \text{ kbps} = \mathbf{52,083...}$

4. **Interpretar el resultado:**
   Como no puedes tener "un trozo" de oyente, redondeamos hacia abajo para no superar el límite de la línea. El servidor soporta un máximo de **52 oyentes**.

**Respuesta correcta:**
**d. 52 oyentes**

### 11. Ejercicio: Cálculo de peso de película comprimida

**Enunciado:** Calcula el peso de una película de **2 horas (120 min)** comprimida a un bitrate de **1 Mbps** (Calidad SD estándar).

**Paso a paso:**

1. **Convertir el tiempo a segundos:**
   $120 \text{ minutos} \times 60 \text{ segundos} = 7.200 \text{ segundos}$.

2. **Calcular el peso total en Megabits (Mb):**
   Multiplicamos el bitrate por el tiempo:
   $1 \text{ Mbps} \times 7.200 \text{ segundos} = 7.200 \text{ Megabits (Mb)}$.

3. **Cruzar el puente de bits a Bytes (Dividir entre 8):**
   Para saber cuánto ocupa en disco (Megabytes), dividimos entre 8:
   $7.200 \text{ Mb} / 8 = \mathbf{900 \text{ Megabytes (MB)}}$.

4. **Verificar unidades:**
   El resultado es 900 MB. Si lo pasáramos a GB (dividiendo entre 1.000) sería 0,9 GB.

**Respuesta correcta:**
**b. 900 MB**

### 12. Ejercicio: Bitrate de Audio Estéreo de Alta Calidad

**Enunciado:** Calcula el bitrate de un flujo de audio que utiliza una frecuencia de **48 kHz**, **24 bits** de profundidad y **2 canales** (estéreo).

**Paso a paso:**

1. **Identificar los datos:**
   * Frecuencia: $48.000 \text{ Hz}$
   * Profundidad: $24 \text{ bits}$
   * Canales: $2$ (al ser estéreo)

2. **Aplicar la fórmula de Bitrate:**
   $\text{Bitrate} = \text{Frecuencia} \times \text{Profundidad} \times \text{Canales}$
   $48.000 \times 24 \times 2 = 2.304.000 \text{ bits por segundo (bps)}$

3. **Convertir a Megabits por segundo (Mbps):**
   Dividimos entre 1.000 para pasar a kbps y otra vez entre 1.000 para Mbps (o directamente entre 1.000.000):
   $2.304.000 / 1.000.000 = \mathbf{2,304 \text{ Mbps}}$

**Respuesta correcta:**
**c. 2.304 Mbps**

### 13. Ejercicio: Almacenamiento de vídeo 4K comprimido

**Enunciado:** Si una película 4K tiene un bitrate de **45 Mbps**, ¿cuánto espacio en disco ocuparán **2 horas** de metraje?

**Paso a paso:**

1. **Convertir el tiempo a segundos:**
   $2 \text{ horas} = 120 \text{ minutos} = 7.200 \text{ segundos}$.

2. **Calcular el total de Megabits (Mb):**
   Multiplicamos el bitrate por la duración:
   $45 \text{ Mbps} \times 7.200 \text{ segundos} = 324.000 \text{ Megabits (Mb)}$.

3. **Cruzar el puente de bits a Bytes (Dividir entre 8):**
   Para saber el peso en disco (Megabytes), dividimos entre 8:
   $324.000 / 8 = 40.500 \text{ Megabytes (MB)}$.

4. **Convertir a Gigabytes (GB):**
   Dividimos entre 1.000:
   $40.500 / 1.000 = \mathbf{40,5 \text{ GB}}$.

**Respuesta correcta:**
**c. 40,5 GB**

### 14. Ejercicio: Porcentaje de uso en fibra óptica

**Enunciado:** Si emites un directo en 4K con un bitrate recomendado de **25 Mbps** en una línea de fibra de **300 Mbps de subida**, ¿qué porcentaje de la línea consumes?

**Paso a paso:**

1. **Identificar los valores de la red:**
   * Capacidad total (100%): $300 \text{ Mbps}$.
   * Consumo del streaming: $25 \text{ Mbps}$.

2. **Aplicar la fórmula de porcentaje:**
   $$\text{Porcentaje} = \left( \frac{\text{Consumo}}{\text{Capacidad}} \right) \times 100$$

3. **Realizar el cálculo:**
   * $\frac{25}{300} = 0,08333...$
   * $0,08333 \times 100 = \mathbf{8,33\%}$.

**Respuesta correcta:**
**a. 8,33%**

### 15. Ejercicio: Capacidad de almacenamiento de audio

**Enunciado:** Si tienes un disco de **10 GB** disponible, ¿cuántas horas de audio a **192 kbps** puedes almacenar aproximadamente?

**Paso a paso:**

1. **Calcular cuánto ocupa 1 hora de este audio:**
   * Tiempo: $3.600 \text{ segundos}$.
   * Peso en Megabits: $192 \text{ kbps} \times 3.600 \text{ s} = 691.200 \text{ kilobits}$.
   * Pasar a Megabits: $691.200 / 1.000 = 691,2 \text{ Mb}$.
   * Pasar a Megabytes (Dividir entre 8): $691,2 / 8 = 86,4 \text{ MB}$.
   * Pasar a Gigabytes: $86,4 / 1.000 = \mathbf{0,0864 \text{ GB}}$ por hora.

2. **Calcular el total de horas en el disco:**
   Dividimos la capacidad total entre lo que ocupa una hora:
   $$\text{Horas} = \frac{10 \text{ GB}}{0,0864 \text{ GB/h}} = 115,74 \text{ horas}$$

3. **Interpretar el resultado:**
   El valor más cercano en las opciones es 115 horas.

**Respuesta correcta:**
**a. 115 horas**

### 16. Ejercicio: Cálculo de Déficit de Ancho de Banda

**Enunciado:** Seis alumnos emiten simultáneamente vídeo a **4 Mbps cada uno**. Si la línea de subida es de **20 Mbps**, ¿cuál es el déficit de ancho de banda?

**Paso a paso:**

1. **Calcular el ancho de banda total necesario:**
   Multiplicamos el número de emisores por su consumo individual:
   $6 \text{ alumnos} \times 4 \text{ Mbps/alumno} = \mathbf{24 \text{ Mbps requeridos}}$.

2. **Identificar la capacidad disponible:**
   La línea de subida es de **20 Mbps**.

3. **Calcular la diferencia (déficit):**
   Restamos lo que tenemos de lo que necesitamos:
   $24 \text{ Mbps (necesarios)} - 20 \text{ Mbps (disponibles)} = \mathbf{4 \text{ Mbps}}$.

**Respuesta correcta:**
**c. 4 Mbps (requiere 24 Mbps)**

### 17. Ejercicio: Peso de 1 minuto de audio "Calidad CD"

**Enunciado:** ¿Cuál es el peso de **1 minuto** de audio en "calidad CD" (**44,1 kHz, 16 bits, estéreo**) sin compresión?

**Paso a paso:**

1. **Convertir el tiempo a segundos:**
   $1 \text{ minuto} = 60 \text{ segundos}$.

2. **Calcular el Bitrate (bps):**
   Multiplicamos frecuencia $\times$ profundidad $\times$ canales (estéreo = 2):
   $44.100 \text{ Hz} \times 16 \text{ bits} \times 2 \text{ canales} = 1.411.200 \text{ bits por segundo (bps)}$.

3. **Calcular el peso total en bits:**
   $1.411.200 \text{ bps} \times 60 \text{ segundos} = 84.672.000 \text{ bits}$.

4. **Convertir de bits a Bytes (Dividir entre 8):**
   $84.672.000 / 8 = 10.584.000 \text{ Bytes (B)}$.

5. **Convertir a Megabytes (MB):**
   Dividimos entre 1.000.000 (o dos veces entre 1.000):
   $10.584.000 / 1.000.000 = \mathbf{10,58 \text{ MB}}$.

**Respuesta correcta:**
**c. 10,58 MB**

### 18. Ejercicio: Tiempo de Descarga Directa

**Enunciado:** Un usuario quiere escuchar un archivo de **100 MB**. Si su conexión es de **10 Mbps**, ¿cuánto tiempo tardará en completarse la "Descarga Directa"?

**Paso a paso:**

1. **Igualar las unidades (El paso clave):**
   El archivo está en **Bytes** (MB) y la conexión en **bits** (Mbps). Debemos pasar el archivo a Megabits multiplicando por 8:
   $100 \text{ MB} \times 8 = \mathbf{800 \text{ Megabits (Mb)}}$.

2. **Aplicar la fórmula del tiempo:**
   $\text{Tiempo} = \frac{\text{Tamaño del archivo (en bits)}}{\text{Velocidad de conexión (en bps)}}$

3. **Realizar el cálculo:**
   $800 \text{ Mb} / 10 \text{ Mbps} = \mathbf{80 \text{ segundos}}$.

**Respuesta correcta:**
**a. 80 segundos**

### 19. Ejercicio: Consumo total de un servidor de Streaming (Unicast)

**Enunciado:** Si el servidor emite un stream de audio de alta calidad a **320 kbps** y hay **50 oyentes** conectados por **Unicast**, ¿qué ancho de banda total consume el servidor?

**Paso a paso:**

1. **Entender el concepto Unicast:**
   En Unicast, el servidor debe enviar un flujo de datos independiente por cada usuario conectado. Por tanto, el consumo es acumulativo.

2. **Calcular el consumo total en kbps:**
   Multiplicamos el bitrate por el número de oyentes:
   $320 \text{ kbps} \times 50 \text{ oyentes} = 16.000 \text{ kbps}$.

3. **Convertir a Megabits por segundo (Mbps):**
   Dividimos entre 1.000:
   $16.000 / 1.000 = \mathbf{16 \text{ Mbps}}$.

**Respuesta correcta:**
**a. 16 Mbps**

### 20. Ejercicio: Peso total de vídeo 720p

**Enunciado:** Un vídeo de **15 minutos** en resolución 720p tiene un bitrate de **4 Mbps**. ¿Cuál es su peso total en **GB**?

**Paso a paso:**

1. **Convertir el tiempo a segundos:**
   $15 \text{ minutos} \times 60 \text{ segundos} = 900 \text{ segundos}$.

2. **Calcular el total en Megabits (Mb):**
   Multiplicamos el bitrate por la duración:
   $4 \text{ Mbps} \times 900 \text{ segundos} = 3.600 \text{ Megabits (Mb)}$.

3. **Cruzar el puente de bits a Bytes (Dividir entre 8):**
   Para obtener el peso en Megabytes (MB):
   $3.600 / 8 = 450 \text{ Megabytes (MB)}$.

4. **Convertir a Gigabytes (GB):**
   Dividimos entre 1.000:
   $450 / 1.000 = \mathbf{0,45 \text{ GB}}$.

**Respuesta correcta:**
**d. 0,45 GB**

### 21. Ejercicio: Capacidad de red local para 4K

**Enunciado:** En una red de **1 Gbps (1000 Mbps)**, ¿cuántos usuarios pueden ver simultáneamente un streaming 4K configurado a **40 Mbps**?

**Paso a paso:**

1. **Identificar la capacidad total:**
   El enunciado ya nos facilita la conversión: $1 \text{ Gbps} = 1.000 \text{ Mbps}$.

2. **Identificar el consumo por flujo (Unicast):**
   Cada usuario que ve el streaming consume **40 Mbps**.

3. **Realizar la división:**
   $$\text{Usuarios} = \frac{\text{Ancho de banda total}}{\text{Bitrate por usuario}}$$
   $1.000 / 40 = \mathbf{25 \text{ usuarios}}$.

**Respuesta correcta:**
**c. 25 usuarios**

### 22. Ejercicio: Eficiencia en Redes Multicast

**Enunciado:** En una red **Multicast**, si enviamos un audio de **128 kbps** a **100 oyentes**, ¿cuál es el ancho de banda que sale del servidor?

**Paso a paso:**

1. **Entender el concepto Multicast:**
   A diferencia del *Unicast* (donde el servidor envía una copia del archivo por cada oyente), en **Multicast** el servidor envía **un único flujo de datos** a la red. Son los nodos de la red (routers/switches) los que se encargan de replicar la señal solo donde sea necesario.

2. **Calcular el consumo del servidor:**
   Dado que el servidor solo emite **una vez** la señal, el ancho de banda de salida es igual al bitrate de la fuente, independientemente de si hay 1, 100 o 1.000 oyentes.
   
   * Bitrate de la fuente: $128 \text{ kbps}$.
   * Consumo de salida: **128 kbps**.

**Respuesta correcta:**
**b. 128 kbps**

### 23. Ejercicio: Capacidad máxima de oyentes (Unicast)

**Enunciado:** En una red con **100 Mbps de subida**, ¿cuántos oyentes simultáneos pueden recibir un flujo de audio de **256 kbps** antes de saturar la línea?

**Paso a paso:**

1. **Igualar las unidades:**
   Convertimos la capacidad de la red (Mbps) a la unidad del flujo de audio (kbps):
   $100 \text{ Mbps} \times 1.000 = \mathbf{100.000 \text{ kbps}}$.

2. **Aplicar la fórmula de capacidad:**
   Dividimos el ancho de banda total entre el consumo por oyente:
   $$\text{Nº de oyentes} = \frac{100.000 \text{ kbps}}{256 \text{ kbps}}$$

3. **Realizar el cálculo:**
   $100.000 / 256 = \mathbf{390,625}$.

4. **Interpretar el resultado:**
   Como no podemos tener una fracción de oyente, redondeamos al número entero inferior para no sobrepasar la capacidad física de la línea. El máximo es **390 oyentes**.

**Respuesta correcta:**
**a. 390 oyentes**

### 24. Ejercicio: Cálculo de peso de vídeo RAW (1080p)

**Enunciado:** ¿Cuánto pesa una toma de **5 segundos** de vídeo **1080p (1920x1080)** a **30 fps** y **24 bits** de color sin comprimir?

**Paso a paso:**

1. **Calcular los píxeles por cuadro:**
   $1920 \times 1080 = 2.073.600 \text{ píxeles}$.

2. **Calcular el total de bits de la toma:**
   Multiplicamos: Píxeles $\times$ Profundidad $\times$ FPS $\times$ Tiempo.
   $2.073.600 \times 24 \text{ bits} \times 30 \text{ fps} \times 5 \text{ segundos} = 7.464.960.000 \text{ bits}$.

3. **Convertir de bits a Bytes (Dividir entre 8):**
   $7.464.960.000 / 8 = 933.120.000 \text{ Bytes (B)}$.

4. **Convertir a Megabytes (MB):**
   Dividimos entre 1.000.000 (o dos veces entre 1.000):
   $933.120.000 / 1.000.000 = \mathbf{933,12 \text{ MB}}$.

**Respuesta correcta:**
**b. 933,12 MB**

### 25. Ejercicio: Reducción de peso por compresión (MP3)

**Enunciado:** Una canción de **4 minutos** pesa 42,33 MB en formato WAV. Si se comprime a MP3 a **128 kbps**, ¿cuál será su nuevo peso aproximado?

**Paso a paso:**

1. **Ignorar el dato del WAV:**
   El peso original (42,33 MB) es irrelevante para el cálculo final, ya que el peso de un archivo comprimido depende exclusivamente de su **bitrate** y su **duración**.

2. **Convertir el tiempo a segundos:**
   $4 \text{ minutos} \times 60 \text{ segundos} = 240 \text{ segundos}$.

3. **Calcular el peso en kilobits (kb):**
   Multiplicamos el bitrate por el tiempo:
   $128 \text{ kbps} \times 240 \text{ segundos} = 30.720 \text{ kilobits (kb)}$.

4. **Convertir a Megabits (Mb):**
   $30.720 / 1.000 = 30,72 \text{ Megabits (Mb)}$.

5. **Convertir a Megabytes (MB) - (Dividir entre 8):**
   $30,72 / 8 = \mathbf{3,84 \text{ MB}}$.

**Respuesta correcta:**
**d. 3,84 MB**

### 26. Ejercicio: Peso de Audio Mono de Alta Calidad (WAV)

**Enunciado:** Calcula el peso de **10 minutos** de audio sin compresión (WAV) a **48 kHz**, **24 bits** y **un solo canal (mono)**.

**Paso a paso:**

1. **Convertir el tiempo a segundos:** $10 \text{ minutos} \times 60 \text{ segundos} = 600 \text{ segundos}$.

2. **Calcular el Bitrate (bps):** $\text{Frecuencia} \times \text{Profundidad} \times \text{Canales}$  
   $48.000 \text{ Hz} \times 24 \text{ bits} \times 1 \text{ canal} = 1.152.000 \text{ bps (1,152 Mbps)}$.

3. **Calcular el peso total en bits:** $1.152.000 \text{ bps} \times 600 \text{ segundos} = 691.200.000 \text{ bits}$.

4. **Cruzar el puente de bits a Bytes (Dividir entre 8):** $691.200.000 / 8 = 86.400.000 \text{ Bytes (B)}$.

5. **Convertir a Megabytes (MB):** Dividimos entre 1.000.000:  
   $86.400.000 / 1.000.000 = \mathbf{86,4 \text{ MB}}$.

**Respuesta correcta:** **a. 86,4 MB**

### 27. Ejercicio: Bitrate de Vídeo RAW (Baja Resolución)

**Enunciado:** ¿Cuál es el bitrate de un vídeo de seguridad antiguo de **360p (640x360)** a **15 fps** y **24 bits** de color sin comprimir?

**Paso a paso:**

1. **Calcular los píxeles por cuadro:**
   $640 \times 360 = 230.400 \text{ píxeles}$.

2. **Calcular el Bitrate en bits por segundo (bps):**
   Multiplicamos: Píxeles $\times$ Profundidad $\times$ FPS.
   $230.400 \times 24 \text{ bits} \times 15 \text{ fps} = 82.944.000 \text{ bps}$.

3. **Convertir a Megabits por segundo (Mbps):**
   Dividimos entre 1.000.000 para obtener la unidad en Megas:
   $82.944.000 / 1.000.000 = \mathbf{82,944 \text{ Mbps}}$.

**Respuesta correcta:**
**a. 82,94 Mbps**

### 28. Ejercicio: Capacidad de almacenamiento masivo (TB)

**Enunciado:** ¿Cuántas horas de vídeo de perfil "HD" (**2 Mbps**) se pueden guardar en un disco de **1 TB**?

**Paso a paso:**

1. **Calcular cuánto ocupa 1 hora de este vídeo:**
   * Tiempo: $3.600 \text{ segundos}$.
   * Consumo en Megabits: $2 \text{ Mbps} \times 3.600 \text{ s} = 7.200 \text{ Megabits (Mb)}$.
   * Convertir a Megabytes (Dividir entre 8): $7.200 / 8 = 900 \text{ MB}$.
   * Convertir a Gigabytes: $900 / 1.000 = \mathbf{0,9 \text{ GB por hora}}$.

2. **Identificar la capacidad del disco en la misma unidad (GB):**
   * $1 \text{ TB} = 1.000 \text{ GB}$.

3. **Realizar la división final:**
   $$\text{Horas} = \frac{\text{Capacidad total (GB)}}{\text{Peso por hora (GB/h)}}$$
   $1.000 / 0,9 = \mathbf{1.111,11 \text{ horas}}$.

**Respuesta correcta:**
**d. 1.111 horas**

### 29. Ejercicio: Tamaño de un Podcast (MP3 CBR)

**Enunciado:** ¿Cuánto espacio ocupará un podcast de **30 minutos** comprimido a un bitrate constante (CBR) de **128 kbps**?

**Paso a paso:**

1. **Convertir el tiempo a segundos:**
   $30 \text{ minutos} \times 60 \text{ segundos} = 1.800 \text{ segundos}$.

2. **Calcular el total en kilobits (kb):**
   Multiplicamos el bitrate por la duración:
   $128 \text{ kbps} \times 1.800 \text{ segundos} = 230.400 \text{ kilobits (kb)}$.

3. **Convertir de bits a Bytes (Dividir entre 8):**
   Para obtener el peso en Kilobytes (KB):
   $230.400 / 8 = 28.800 \text{ Kilobytes (KB)}$.

4. **Convertir a Megabytes (MB):**
   Dividimos entre 1.000:
   $28.800 / 1.000 = \mathbf{28,8 \text{ MB}}$.

**Respuesta correcta:**
**d. 28,8 MB**

### 30. Ejercicio: Bitrate de Vídeo 8K RAW (HDR)

**Enunciado:** Calcula el bitrate en **Gbps** para un vídeo **8K (7680x4320)** a **60 fps** con una profundidad de color de **30 bits (HDR)** sin compresión.

**Paso a paso:**

1. **Calcular los píxeles por cuadro:**
   $7.680 \times 4.320 = 33.177.600 \text{ píxeles}$.

2. **Calcular el Bitrate en bits por segundo (bps):**
   Multiplicamos: Píxeles $\times$ Profundidad $\times$ FPS.
   $33.177.600 \times 30 \text{ bits} \times 60 \text{ fps} = 59.719.680.000 \text{ bps}$.

3. **Convertir a Gigabits por segundo (Gbps):**
   Dividimos entre 1.000.000.000 (mil millones) para pasar de bits a Gigabits:
   $59.719.680.000 / 1.000.000.000 = \mathbf{59,71 \text{ Gbps}}$.

**Respuesta correcta:**
**b. 59,71 Gbps**
