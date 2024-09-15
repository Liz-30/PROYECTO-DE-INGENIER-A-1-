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


![4057a6ed-824e-474e-ac80-8445f42d3ed0](https://github.com/user-attachments/assets/f2914f3e-8a66-4173-8cac-f305f7bedcf1)



### - Google colab

Hemos utilizado esta herramienta para procesar y reformar los datos JSON obtenidos de TinyML, adaptándolos al formato requerido por Edge Impulse.

![image](https://github.com/user-attachments/assets/e86649d4-f1d4-4115-a078-e9b9057dd915)


### 3.- RESULTADOS:

En base a la recopilación de datos, el modelo debe ser capaz de identificar las señales utilizando el modelo entrenado y proporcionar los resultados correspondientes.

- LED rojo: Activado cuando se detecta un círculo.

- LED azul: Activado cuando se detecta el número 3.

- LED verde: Activado cuando se detecta el número 1.


Sin embargo, debido a nuetsras dificultades con el manejo de estas herramientas, no hemos logrado alcanzar los resultados esperados. Aunque logramos entrenar nuestro modelo, al momento de ejecutarlo en el Arduino, este no reconoce todas las muestras de manera adecuada.


![5be7c90e-1d41-45d8-99c3-b85972a20d59](https://github.com/user-attachments/assets/f781a746-e3ef-4712-8303-8ee3183195ba)







### 4.- DISCUSIONES:

Este proyecto nos permitió apreciar el enorme potencial de TinyML en dispositivos pequeños como el Arduino Nano 33 BLE Sense. La capacidad de ejecutar modelos de aprendizaje automático en un dispositivo compacto y de bajo consumo abre la puerta a una nueva era de aplicaciones inteligentes en campos como el IoT, la agricultura, la salud, y muchas otras áreas donde la eficiencia energética es crucial.

El hecho de que el modelo es bueno y responde a formas y números como círculos y dígitos muestra cómo TinyML puede facilitar la interacción entre las personas y las máquinas en entornos cotidianos. No obstante, también enfrentamos algunos desafíos, como la limitación en la precisión cuando las imágenes de entrada eran más complejas o de menor calidad. Esto nos hizo reflexionar sobre la necesidad de continuar optimizando el procesamiento de imágenes y mejorar la robustez del modelo ante ruidos en los datos.

Otro aspecto que se destacó fue el tiempo de respuesta del dispositivo. Aunque en general fue satisfactorio, se observó que el modelo podría beneficiarse de una mayor optimización en términos de velocidad, especialmente cuando se trabaja con grandes cantidades de datos o en aplicaciones que requieren respuestas en tiempo real.

De este trabajo podemos conluir que el modelo que empleamos es adecuado para tareas de optimización y aprendizaje, ya que tiene un bajo consumo de energía, lo que lo hace eficiente. Sin embargo, debido a nuestra falta de experiencia tanto en el tema como en el manejo adecuado de la página web, no hemos logrado alcanzar los objetivos planteados.




### REFERENCIAS BIBLIOGRAFICAS

1. DataScientest. (2024). TinyML: La revolución de la IA en dispositivos de baja potencia. DataScientest. https://datascientest.com/es/tinyml-todo-sobre

2. Tardif, A. (2023). TinyML: el futuro del aprendizaje automático en una escala minúscula. https://www.unite.ai/es/tinyml-the-future-of-machine-learning-on-a-minuscule-scale/



