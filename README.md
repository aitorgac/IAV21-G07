# IAV21-G07
## Introducción
Este repositorio funcionará como punto de enlace entre todas las prácticas del grupo 07 de la asignatura de Inteligencia Artifical para Videojuegos. Cada apartado se actualizará con información de las diferentes prácticas que realizaremos durante el curso. Los integrantes del grupo somos:
* Jorge Bello Martín
* Aitor García Casamayor
* David Godoy Ruiz
* Eva Lucas Leiro
* Tomás López Antón

### Práctica 1: El flautista de Hamelín

Para realizar esta práctica hemos colocado varias esferas en un espacio cuadrado, con colores diferentes según su comportamiento:
* La esfera amarilla es el jugador, y se mueve utilizando las teclas WASD o las flechas del teclado y puede tocar la flauta manteniendo la barra espaciadora, lo que cambia el suelo de color y los comportamientos del resto de esferas.
* La esfera azul es el perro, que sigue al jugador hasta que toca la flauta lo que le hace huir.
* Las esferas rojas son las ratas, que deambulan por el escenario evitándose entre sí hasta que el jugador toca la flauta, lo que provoca que vayan hacia él, evitando acabar en la misma posición que otras ratas.

Para ello hemos integrado los componentes de llegada (Llegada.cs), usados tanto en el perro como en las ratas de forma alternativa y merodeo, (Merodeo.cs) usado por las ratas cuando no suena la flauta y que tiene como padres y abuelo
los componentes encarar y alinear (Encarar.cs y Alinear.cs). Para evitar que las ratas acaben todas en la misma posición y para dar más sensación de horda hemos implementado un comportamiento de evasión (EvitarAgente.cs) que provoca
que se mantengan separadas entre sí.

Para gestionar el uso de la flauta hemos hecho un gestor para la escena (Manager.cs) que, gracias a la estructura singleton, es llamado por el jugador (desde ControlJugador.cs) para alterar el resto de objetos.

### Práctica 2: El hilo de Ariadna

Para realizar esta práctica hemos utilizado el proyecto base de Navegación. En él, a raíz de un archivo de texto codificado para formar un mapa, una vez pulsamos el botón de Play se creará dicho mapa, teniendo a Teseo en un punto del mapa y al Minotauro en el centro del mismo. Además, hemos reutilizado los scripts de movimiento de la anterior práctica.
* La esfera __ es el jugador, y se mueve utilizando las teclas WASD o las flechas del teclado y puede tocar mostrar el hilo de Ariadna manteniendo la barra espaciadora, lo que marca el camino más corto en el suelo y comienza a seguirlo, hasta que deje de pulsar el espacio.
* Si mientras se ve el hilo de Ariadna se pulsa el botón S, cambiará el camino mostrado al modo suavizado.
* La esfera ___ es el minotauro, que merodeará de manera lenta a no ser de que en su ángulo de visión vea a Teseo.

Para ello hemos integrado los componentes de ___


#### Bibliografía
* Millington, I.: Artificial Intelligence for Games. CRC Press, 3rd Edition(2019)
* Palacios, J.: Unity 2018 Artificial Intelligence Cookbook. Packt Publishing, 2nd Revised edition (2018)
* Creador de mapas: https://www.dcode.fr/maze-generator
