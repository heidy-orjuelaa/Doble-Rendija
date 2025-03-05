# Experimento de la Doble Rendija

El experimento de la doble rendija es una de las demostraciones más caracteristicas de la mecánica cuántica. Muestra el comportamiento ondulatorio de las partículas y plantea preguntas importantes y basicas sobre la naturaleza de la realidad y la observación en la física.

## Comenzando

Estas instrucciones nos permitieron replicar el experimento de la doble rendija en un montaje experimental. 

### Requisitos Previos

Materiales y herramientas necesarias para llevar a cabo el experimento:

```
* Fuente de electrones, fotones o cualquier tipo de partícula (laser).
* Placa con dos rendijas paralelas (cuadro de aluminio).
* Pantalla de detección (caja negra).
```

### Instalación

Pasos para preparar el experimento:

1. Cortar un cuadro de aluminio y hacer las dos rendijas ahi, teniendo menos de un mm de separación.
2. Hacer una caja de carton (negra) y cortar un agujero para colocar el cuadro de aluminio del punto anterior.
3. Configurar la fuente de partículas (laser) y alinearla con la doble rendija.
4. Colocar la pantalla de detección a una distancia adecuada.
5. Realizar las pruebas sin observación directa para observar el patrón de interferencia.

```
* Encender el emisor de electrones (laser) y calibrar su dirección.
* Asegurar que la pantalla esté en una posición fija para registrar los impactos correctamente.
```

## Ejecución de Pruebas

### Pruebas de extremo a extremo

El experimento evalúa el patrón de interferencia generado en la pantalla:

```
Medir la distribución y observar si sale una rendija o dos rendijas.
```

### Pruebas de consistencia teórica

Comparación de los resultados con las predicciones teóricas:

```
Verificar si el patrón de interferencia coincide con la teoria, o el planteado inicialmente.
```

## Simulacion en codigo de python

```
import numpy as np
import matplotlib.pyplot as plt

def interferencia_doble_rendija(ancho_rendija=0.1, separacion=0.5, longitud_onda=0.5, distancia_pantalla=5, puntos=1000):
    x = np.linspace(-5, 5, puntos)
    k = 2 * np.pi / longitud_onda
    
    # Cálculo de la amplitud de onda desde ambas rendijas
    r1 = np.sqrt((x - separacion / 2)**2 + distancia_pantalla**2)
    r2 = np.sqrt((x + separacion / 2)**2 + distancia_pantalla**2)
    
    # Intensidad de interferencia
    intensidad = (np.cos(k * (r1 - r2) / 2))**2
    
    # Gráfica del patrón de interferencia
    plt.figure(figsize=(10, 5))
    plt.plot(x, intensidad, color='blue')
    plt.fill_between(x, intensidad, alpha=0.3, color='blue')
    plt.title("Patrón de Interferencia en la Doble Rendija")
    plt.xlabel("Posición en la pantalla")
    plt.ylabel("Intensidad relativa")
    plt.grid()
    plt.show()

interferencia_doble_rendija()
```


## Conclusión

El experimento de la doble rendija demuestra de manera clara la dualidad onda-partícula, un principio fundamental de la mecánica cuántica. Al observar el patrón de interferencia sin un detector, se confirma que las partículas pueden comportarse como ondas, interfiriendo consigo mismas. Sin embargo, cuando se coloca un detector en una de las rendijas, el patrón de interferencia desaparece y las partículas se comportan como corpúsculos. Esto sugiere que el acto de observación influye en el comportamiento de las partículas, planteando profundas cuestiones sobre la naturaleza de la realidad y el papel del observador en la física cuántica.

## Despliegue

Para un despliegue en un sistema en vivo:

* Configurar un ambiente controlado para evitar interferencias externas (Un lugar totalmente oscuro).
  
## Construido con

* Simulaciones Cuánticas - Herramientas para modelar el experimento.
* nterferencia de doble rendija: https://www.youtube.com/watch?v=PVyJFzx7zig
* Interferencia de una sola rendija e interferencia circular: https://www.youtube.com/watch?v=uohd0TtqOaw
* Interferencia de partículas: https://www.youtube.com/watch?v=1LVkQfCptEs

## Autores

* **Heidy Orjuela**
* **Paula Diaz**

## Licencia

Este proyecto está bajo la licencia MIT - consulta LICENSE.md.

## Agradecimientos

* A la comunidad científica por sus contribuciones
* A los desarrolladores de software de simulación
* A las instituciones de investigación en mecánica cuántica
