# Proyecto 5: Sistemas inteligentes y sus aplicaciones en la actualidad

Este proyecto analiza tres aplicaciones actuales de la Inteligencia Artificial pertenecientes a sectores muy distintos (Videojuegos, Agricultura y Salud). El objetivo es identificar cómo se integran los principios teóricos de los sistemas inteligentes en casos de uso del mundo real, evaluando qué características cumplen y cuáles no.

---

## 1. Campo: Entretenimiento y Videojuegos
**Aplicación:** AI Director (Saga *Left 4 Dead*)

El "AI Director" es un sistema de ajuste dinámico de dificultad que gestiona el ritmo de una partida cooperativa en tiempo real, adaptando la experiencia al estado y habilidad de los jugadores.

### Análisis de las 8 características:

1. **Inteligencia (Cumple parcialmente):** El sistema demuestra inteligencia al lograr su objetivo principal (mantener el ritmo de juego adecuado), aunque es limitada, ya que funciona mediante reglas predefinidas en lugar de razonamiento flexible.

2. **Sistematización (Cumple):** El AI Director es un sistema claramente delimitado. Interactúa con el motor del videojuego (sus componentes internos), pero sus límites están bien definidos: no interfiere en otras partes del juego fuera de su ámbito de control (gráficos, audio, física).

3. **Objetivo (Cumple):** Su meta está claramente definida y bien documentada: mantener la tensión del juego ("pacing") evitando tanto el aburrimiento como la frustración extrema. Esto es medible a través del nivel de "estrés" del equipo.

4. **Capacidad sensorial (Cumple):** Sus sensores son virtuales. Extrae telemetría constante del motor del juego: nivel de salud de los avatares, munición disponible, posición en el mapa, y un valor calculado de "estrés" basado en el daño recibido en los últimos minutos.

5. **Conceptualización (Cumple):** Conceptualiza el entorno del juego dividiéndolo en zonas de "intensidad" (baja, media, alta) y abstrae el estado grupal en un único valor: el nivel de estrés colectivo. Esto permite generalizaciones más allá de casos específicos.

6. **Reglas de actuación (Cumple):** Utiliza árboles de decisión complejos y máquinas de estado para actuar sobre el entorno digital. Ejemplo: *"Si estrés grupal > 80%, ejecutar regla de pausa de spawning y generar botiquines en la siguiente sala"*.

7. **Memoria (Cumple):** Almacena el estado a corto plazo del equipo durante la partida. Recuerda si los jugadores acaban de sobrevivir a un ataque masivo o si llevan mucho tiempo sin presión, evitando generar patrones repetitivos.

8. **Aprendizaje (No cumple):** El sistema clásico **no utiliza Machine Learning**. Funciona mediante algoritmos heurísticos y lógica de programación avanzada (máquinas de estados) escritos manualmente. Una vez el juego se lanza, su comportamiento no evoluciona ni mejora automáticamente a partir de las nuevas partidas.

---

## 2. Campo: Agricultura de Precisión (AgriTech)
**Aplicación:** Tractores *See & Spray* (Blue River Technology / John Deere)

Se trata de vehículos agrícolas equipados con visión artificial y Deep Learning que aplican micro-chorros de herbicida de forma selectiva únicamente sobre las malas hierbas, perdonando al cultivo principal.

### Análisis de las 8 características:

1. **Inteligencia (Cumple):** El sistema demuestra un alto nivel de inteligencia al lograr su objetivo complejo: identificar plantas individuales a 20 km/h y aplicar herbicida solo donde es necesario. Su tasa de precisión supera el 95% en condiciones reales.

2. **Sistematización (Cumple):** Es un sistema bien delimitado compuesto por subsistemas especializados: cámaras (sensores), procesador GPU (cómputo), actuadores eléctricos (boquillas pulverizadoras). Estos componentes interactúan fuertemente entre sí pero están aislados de otras funciones del tractor.

3. **Objetivo (Cumple):** Su objetivo es doble pero coherente: (a) maximizar la eliminación de malas hierbas y (b) minimizar el uso de herbicida (reducción del 80%). Ambos son medibles y están bien documentados en especificaciones técnicas.

4. **Capacidad sensorial (Cumple):** Utiliza sensores puramente físicos: cámaras de resolución de 2048 x 1536 píxeles montadas en los brazos del tractor que escanean el suelo a alta velocidad mientras el vehículo avanza. Captura imágenes en rango visible e infrarrojo.

5. **Conceptualización (Cumple):** Mediante Redes Neuronales Convolucionales (CNN), el sistema abstrae imágenes de píxeles en conceptos de alto nivel: *"algodón sano"*, *"mala hierba tipo A"*, *"tierra desnuda"*, *"residuo de cosecha anterior"*. Esto permite generalizar a nuevas imágenes nunca vistas.

6. **Reglas de actuación (Cumple):** Sus reglas son físicas y determinísticas. La regla principal es binaria: *"Si clasificación = mala hierba con confianza > 90%, enviar impulso eléctrico a boquilla XYZ durante 50 ms"*. La acción es inmediata y medible en el mundo real.

7. **Memoria (Cumple):** El sistema tiene memoria a dos niveles: (a) memoria local en tiempo real (recuerda la posición GPS del tractor para no pulverizar dos veces el mismo punto) y (b) memoria histórica global (el modelo CNN entrenado "recuerda" los millones de ejemplos de entrenamiento que le enseñaron a distinguir cultivos de malezas).

8. **Aprendizaje (Cumple):** Es probablemente donde el sistema más brilla. Utiliza aprendizaje supervisado: se reentrena regularmente con nuevas imágenes capturadas por los tractores en el campo, validadas por agrónomos reales. Esto permite que el modelo mejore su precisión continuamente frente a nuevas especies de malezas o condiciones de suelo.

---

## 3. Campo: Salud y Telemedicina
**Aplicación:** Diagnóstico de Melanoma por Visión Artificial (ej. *SkinVision*)

Aplicaciones móviles orientadas al usuario final que analizan fotografías de lesiones cutáneas y lunares para predecir el riesgo de desarrollar cáncer de piel (melanoma).

### Análisis de las 8 características:

1. **Inteligencia (Cumple):** El sistema demuestra inteligencia médica significativa. Estudios clínicos muestran que su tasa de detección de melanomas es comparable o superior a la de dermatólogos humanos (sensibilidad > 90%). Esto prueba que logra su objetivo de forma inteligente.

2. **Sistematización (Cumple):** Es un sistema bien estructurado con límites claros. Incluye subsistemas: interfaz móvil (captura de imagen), preprocesamiento (normalización de imagen), modelo CNN (clasificación), base de datos (histórico del paciente), y módulo de alerta. Cada uno tiene una función específica.

3. **Objetivo (Cumple):** Múltiples objetivos jerarquizados: objetivo principal es detectar melanomas en estadios tempranos (cuando aún son tratables); objetivo secundario es reducir falsos positivos para no alarmar innecesariamente; objetivo terciario es democratizar el acceso a screening dermatológico sin cita previa.

4. **Capacidad sensorial (Cumple):** Utiliza un único sensor físico pero fundamental: la lente de la cámara del smartphone del usuario. A pesar de su simplicidad, captura información visual suficiente (color, textura, bordes, diámetro) para el análisis.

5. **Conceptualización (Cumple):** Conceptualiza lesiones cutáneas mediante la extracción automática de características visuales de alto nivel: *"asimetría"*, *"irregularidad de bordes"*, *"variación de color"*, *"diámetro > 6mm"* (criterios ABCD de dermatología). Estos conceptos abstraen la información de píxeles a categorías médicas significativas.

6. **Reglas de actuación (Cumple):** Sus reglas son determinísticas y médicamente válidas. Ejemplo: *"Si puntuación ABCD > umbral clínico, generar alerta roja y sugerir derivación a dermatólogo en las próximas 48 horas"*. La acción es digital (interfaz UI) pero está diseñada para motivar acciones físicas del usuario.

7. **Memoria (Cumple):** El sistema posee memoria tanto local como histórica. Memoria local: durante una sesión, compara la foto actual del lunar con fotos previas del mismo lunar capturadas hace semanas/meses para detectar cambios. Memoria histórica: la base de datos del paciente (almacenada en cloud) conserva todo el historial longitudinal de lesiones y diagnósticos.

8. **Aprendizaje (Cumple):** Implementa un esquema sofisticado de *Human in the Loop*. El sistema aprende mediante retroalimentación validada: cuando un dermatólogo humano confirma o corrige el diagnóstico de la IA, ese caso (con la corrección) se reintroduce en la base de datos de entrenamiento para reentrenar el modelo. Esto permite que la IA mejore iterativamente sin caer en sesgo algorítmico.

---

## Tabla Resumen de Características

| Característica | AI Director (Videojuegos) | See & Spray (Agricultura) | SkinVision (Salud) |
| :--- | :--- | :--- | :--- |
| **1. Inteligencia** | Parcial (heurística) | Sí (>95% precisión) | Sí (comparable a humanos) |
| **2. Sistematización** | Sí (motor + subsistemas) | Sí (hardware + software) | Sí (móvil + cloud) |
| **3. Objetivo** | Sí (mantener ritmo) | Sí (eliminar malezas, ahorrar herbicida) | Sí (detectar melanoma temprano) |
| **4. Capacidad sensorial** | Virtual (telemetría) | Física (cámaras RGB+IR) | Física (cámara móvil) |
| **5. Conceptualización** | Sí (zonas de estrés) | Sí (tipos de plantas via CNN) | Sí (criterios ABCD de dermatología) |
| **6. Reglas de actuación** | Sí (árboles decisión) | Sí (control de boquillas) | Sí (alertas médicas) |
| **7. Memoria** | Corto plazo (partida) | Dual (local + histórica global) | Dual (sesión + histórico paciente) |
| **8. Aprendizaje** | No (algoritmo estático) | Sí (supervisado continuo) | Sí (*Human in the Loop*) |
