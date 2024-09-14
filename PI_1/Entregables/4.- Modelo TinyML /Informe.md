# *MODELO DE TINYML*

### INTRODUCCIÓN:
Machine learning (Aprendizaje automático integrado) en la actualidad representa un avance significativo en la capacidad qué tienen los dispositivos para realizar un procesamiento inteligente de datos, este se enfoca en la implementación de algoritmos de aprendizaje en sistemas embebidos (funciones específicas), lo que esto permite la ejecución de tareas complejas directamente en el dispositivo sin depender de recursos computacionales externos [1].

El TinyML (Machine Learning en Dispositivos Pequeños), que se centra en la adaptación y optimización de modelos de aprendizaje automático para su ejecución en hardware con  algunas limitaciones en términos de procesamiento, memoria y consumo energético. TinyML facilita la integración de capacidades inteligentes en dispositivos compactos y de bajo consumo, ampliando las posibilidades para aplicaciones en el Internet de las Cosas (IoT), dispositivos portátiles y sistemas de monitoreo ambiental [2].

El presente informe tiene como objetivo desarrollar un modelo de TinyML para su implementación en un Arduino Nano 33 BLE Sense. El modelo será diseñado para inferir y realizar las siguientes acciones en función de las formas y números dibujados:

- Encender un LED rojo cuando el Arduino detecte un dibujo de un círculo.

- Encender un LED azul cuando el Arduino detecte el número 3.

- Encender un LED verde cuando el Arduino detecte el número 1.

Estos resultados nos van a permitir validar la capacidad  que tiene el modelo TinyML para identificar y diferenciar entre formas geométricas y dígitos, facilitando la interacción con el entorno a través de señales visuales.


### METODOLOÍA:

El proceso para implementar el modelo TinyML en el Arduino Nano 33 BLE Sense se dividió en varias fases:

2.1 Preparación del Entorno

Se configuró el entorno de desarrollo para trabajar con el Arduino Nano 33 BLE Sense utilizando TensorFlow Lite for Microcontrollers. Esta versión de TensorFlow permite implementar modelos de aprendizaje automático optimizados para dispositivos de baja potencia. También se instalaron las librerías necesarias para la manipulación de datos y procesamiento de señales.

2.2 Diseño del Modelo TinyML

El modelo de ML se entrenó previamente en una plataforma de alto rendimiento y luego se adaptó para el Arduino utilizando TensorFlow Lite. El modelo se entrenó para identificar dos tipos de patrones: formas geométricas y números. Para el entrenamiento, se utilizaron datos de imágenes de formas simples (círculos) y dígitos numéricos (1 y 3). El conjunto de datos se preprocesó mediante técnicas de normalización y reducción de dimensionalidad para ajustarse a las limitaciones del hardware.









2.3 Implementación en el Arduino Nano 33 BLE Sense
Una vez entrenado el modelo, se convirtió a un formato compatible con el microcontrolador y se cargó en el Arduino. Se programaron tres salidas específicas en función de la predicción del modelo:

- LED rojo: Activado cuando se detecta un círculo.

- LED azul: Activado cuando se detecta el número 3.

- LED verde: Activado cuando se detecta el número 1.





### RESULTADOS:





### DISCUSIONES:

### REFERENCIAS BIBLIOGRAFICAS

1. DataScientest. (2024). TinyML: La revolución de la IA en dispositivos de baja potencia. DataScientest. https://datascientest.com/es/tinyml-todo-sobre

2. Tardif, A. (2023). TinyML: el futuro del aprendizaje automático en una escala minúscula. https://www.unite.ai/es/tinyml-the-future-of-machine-learning-on-a-minuscule-scale/



