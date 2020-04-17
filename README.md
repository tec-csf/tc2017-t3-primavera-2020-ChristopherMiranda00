# Tarea *3*. *Técnicas de diseño de algoritmos*

---

##### Integrantes:
1. *Christopher Luis Miranda Vanegas* - *A01022676* - *Campus Santa Fe*


---
## 1. Aspectos generales

Las orientaciones de la tarea se encuentran disponibles en la plataforma **Canvas**.

Este documento es una guía sobre qué información debe entregar como parte de la tarea, qué requerimientos técnicos debe cumplir y la estructura que debe seguir para organizar su entrega.


### 1.1 Requerimientos técnicos

A continuación se mencionan los requerimientos técnicos mínimos de la tarea, favor de tenerlos presente para que cumpla con todos.

* El código debe desarrollarse en C++, cumpliendo con el último estándar [C++17](https://isocpp.org/std/the-standard).
* Toda la programación debe realizarse utilizando Programación Genérica.
* Deben utilizarse las [C++ Core Guidelines](https://github.com/isocpp/CppCoreGuidelines/blob/master/CppCoreGuidelines.md).
* Todo el código debe estar correctamente documentado, siguiendo los lineamientos que aparecen en [Documenting C++ Code](https://developer.lsst.io/cpp/api-docs.html).
* Todo el código de la tarea debe alojarse en este repositorio de GitHub.
* Debe configurar su repositorio para que utilice el sistema de Integración Continua [Travis CI](https://travis-ci.org/).

### 1.2 Estructura del repositorio

El proyecto debe seguir la siguiente estructura de carpetas:
```
- / 			        # Raíz del repositorio
    - README.md			# Archivo con la información general de la actividad (este archivo)
    - sources  			# Códigos fuente con la solución
```

## 2. Solución
##### Problema del Sistema Monetario
El código del sistema monetario, monetario.cpp, tiene definido un arreglo del valor de las monedas, el cual en el método de 'darCambio' dependiendo de la cantidad ingresada comparará y agregará la solución a un vector. El resultado es la cantidad ingresada a evaluar, y abajo el cambio con el número de monedas utilizadas con el valor de la moneda. Cabe recalcar que dicho algoritmo solo funciona con enteros. Este algoritmo tiene una complejidad O(n).

##### Problema del Viajante
El código del problema del viajante, grafo.cpp, usa el algoritmo de Dijkstra. Dicho algoritmo utiliza un grafo dirigido ponderado de N nodos. El proceso es el siguiente: 
1. Se inicializan las distancias con un valor infinito ( en este caso -1), ya que estas son desconocidas al principio. 
2. Se toma a vo como el nodo actual
3. Se hace un recorrido de los nodos adyacentes de vo, de los nodos no marcados. 
4. Se calcula la distancia del nodo actual con la de sus vecinos, sumando la distancia del nodo vi más la distancia del vo hasta el nodo vi. Si dicha distancia es menor que la distancia almacenada en la estructura y se actualiza con esta distancia. 
5. El nodo vo se marca.
6. Y tomamos como próximo nodo actual el nodo con menor valor de distancia. Y se repite hasta que ya no hayan nodos no marcados. 

Esta solución cuenta con una matriz de adyaciencia, haciendo este algoritmo con un complejidad O(n^2). 



### 2.1 Pasos a seguir para utilizar la aplicación

##### Problema Sistema Monetario
1. Mediante la terminal, navegar a la carpeta [sources](../sources)
2. Correr el comando: `g++ -o monetario.cpp -std=c++17`
3. Correr el comando: `./monetario`
##### Problema del Viajero
1. Mediante la terminal, navegar a la carpeta [sources](../sources)
2. Correr el comando: `g++ -o grafo.cpp -std=c++17`
3. Correr el comando: `./grafo`

## 3. Referencias
> http://www.lcc.uma.es/~av/Libro/CAP4.pdf
> https://ocw.ehu.eus/pluginfile.php/9410/mod_resource/content/1/03_Algoritmos_Voraces/03_Algoritmos_Voraces.pdf
> https://www.includehelp.com/cpp-tutorial/dijkstras-algorithm.aspx
> https://es.wikipedia.org/wikiAnexo:Ejemplo_de_Algoritmo_de_Dijkstra
> https://www.geeksforgeeks.org/dijkstras-shortest-path-algorithm-greedy-algo-7/