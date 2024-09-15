# *MODELO DE TINYML*

## 1.- INTRODUCCIÓN:
Machine learning (Aprendizaje automático integrado) en la actualidad representa un avance significativo en la capacidad qué tienen los dispositivos para realizar un procesamiento inteligente de datos, este se enfoca en la implementación de algoritmos de aprendizaje en sistemas embebidos (funciones específicas), lo que esto permite la ejecución de tareas complejas directamente en el dispositivo sin depender de recursos computacionales externos [1].

El TinyML (Machine Learning en Dispositivos Pequeños), que se centra en la adaptación y optimización de modelos de aprendizaje automático para su ejecución en hardware con  algunas limitaciones en términos de procesamiento, memoria y consumo energético. TinyML facilita la integración de capacidades inteligentes en dispositivos compactos y de bajo consumo, ampliando las posibilidades para aplicaciones en el Internet de las Cosas (IoT), dispositivos portátiles y sistemas de monitoreo ambiental [2].

El presente informe tiene como objetivo desarrollar un modelo de TinyML para su implementación en un Arduino Nano 33 BLE Sense. El modelo será diseñado para inferir y realizar las siguientes acciones en función de las formas y números dibujados:

- Encender un LED rojo cuando el Arduino detecte un dibujo de un círculo.

- Encender un LED azul cuando el Arduino detecte el número 3.

- Encender un LED verde cuando el Arduino detecte el número 1.

Estos resultados nos van a permitir validar la capacidad  que tiene el modelo TinyML para identificar y diferenciar entre formas geométricas y dígitos, facilitando la interacción con el entorno a través de señales visuales.


## 2.- METODOLOÍA:

El proceso para implementar el modelo TinyML en el Arduino Nano 33 BLE Sense se dividió en varias fases:

### Preparación del entorno y selección de herramientas 

### - Sensor BLE Arduiono Nano 33:

El Arduino Nano 33 BLE es una placa de desarrollo de bajo costo, que incluye conectividad Bluetooth Low Energy (BLE) para la comunicación con dispositivos externos. Integra varios sensores, como un acelerómetro, giroscopio y magnetómetro, además de un sensor de temperatura. Su principal funcion en este reto es que actúa como el cerebro, recolectando, procesando datos de los sensores, y controlando salidas, como el encendido de un LED si esque es (cero, uno o tres). Esto lo hace ideal para aplicaciones de IoT, monitoreo remoto y dispositivos portátiles.


![arduino_nano_33_ble](https://github.com/user-attachments/assets/4b6f48b8-c8b0-475f-88ee-c7fe886641ff)


### - TinyML
 
Mediante esta plataforma (https://tinyml.seas.harvard.edu/magic_wand/) hemos recolectado patrones de dibujo como formas geometricas (circulos) y datos numericos (1y2).

https://github.com/user-attachments/assets/40f89249-e745-4640-9d5b-4a2387af70e8

### - Edge Impluce:

Es una plataforma en línea que se usa para el desarrollo de modelos de aprendizaje automático en dispositivos IoT, esta herramienta nos ayudo a entrenar un modelo de clasificación que fue diseñado para identificar señales de dibujo (circulo, uno y tres) partir de los datos recolectados por el Arduino Nano 33 BLE Sense. Esta herramienta permitió automatizar el procesamiento de datos sensoriales y mejorar la precisión en la detección de movimientos.

![edge impulse](https://github.com/user-attachments/assets/faa5d81d-bd34-47e4-ad68-953ce77ebf5b)

### - Google colab

Hemos utilizado esta herramienta para procesar y reformar los datos JSON obtenidos de TinyML, adaptándolos al formato requerido por Edge Impulse.

![image](https://github.com/user-attachments/assets/e86649d4-f1d4-4115-a078-e9b9057dd915)


### Implementación en el Arduino Nano 33 BLE Sense

Una vez entrenado el modelo, se convirtió a un formato compatible con el microcontrolador y se cargó en el Arduino. Se programaron tres salidas específicas en función de la predicción del modelo:

- LED rojo: Activado cuando se detecta un círculo.

- LED azul: Activado cuando se detecta el número 3.

- LED verde: Activado cuando se detecta el número 1.


### 3.- RESULTADOS:





### 4.- DISCUSIONES:







### REFERENCIAS BIBLIOGRAFICAS

1. DataScientest. (2024). TinyML: La revolución de la IA en dispositivos de baja potencia. DataScientest. https://datascientest.com/es/tinyml-todo-sobre

2. Tardif, A. (2023). TinyML: el futuro del aprendizaje automático en una escala minúscula. https://www.unite.ai/es/tinyml-the-future-of-machine-learning-on-a-minuscule-scale/



