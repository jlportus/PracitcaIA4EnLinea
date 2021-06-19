# INTELIGENCIA ARTIFICIAL
### Diploma en Informática Militar
### Curso 2020/21
### PRÁCTICA: Juegos bipersonales. Cuatro en Raya
### Realizada por: Capitán José Luis Puerto Pérez

## 1. INTRODUCCIÓN

Como evaluación de la asignatura de Inteligencia Artificial (IA), en la parte de búsqueda, se solicita la realización de una práctica consistente en una aplicación que permita el juego conecta 4, o 4 en línea, contra una IA que sea capaz de determinar la mejor jugada.

## 2. El Juego Conecta 4
       
#### Características del Juego:

> *“Conecta 4 (también conocido como 4 en Linea en algunas versiones) es un juego de mesa para dos jugadores distribuido por Hasbro, en el que se introducen fichas en un tablero vertical con el objetivo de alinear cuatro consecutivas de un mismo color. Fue creado en 1974 por Ned Strongin y Howard Wexler para Milton Bradley Company.1​ “* 

#### Reglas del juego: 

> *“ El objetivo de Conecta 4 es alinear cuatro fichas sobre un tablero formado por seis filas y siete columnas. Cada jugador dispone de 21 fichas de un color (por lo general, rojas o amarillas).2​ Por turnos, los jugadores deben introducir una ficha en la columna que prefieran (siempre que no esté completa) y ésta caerá a la posición más baja. Gana la partida el primero que consiga alinear cuatro fichas consecutivas de un mismo color en horizontal, vertical o diagonal.2​ Si todas las columnas están llenas pero nadie ha hecho una fila válida, hay empate.2​ 
Conecta 4 es un juego de estrategia abstracta donde los contrincantes disponen de información perfecta. Por norma general, el primer jugador tiene más posibilidades de ganar si introduce la primera ficha en la columna central. Si lo hace en las contiguas se puede forzar un empate, mientras que si la mete en las más alejadas del centro su rival puede vencerle con mayor facilidad.”*

#### Condiciones de Victoria:
> *“Gana el primer jugador que logre alinear 4 fichas de manera horizontal, vertical o diagonal. “*

> **Fuente: https://es.wikipedia.org/wiki/Conecta_4**


## 3. Condiciones del desarrollo de la practica

#### Hipótesis para el desarrollo:
- Se considera un tablero de seis filas y siete columnas.
- Las fichas siempre se colocan en una sola de las columnas, que no este llena, en la posición libre mas baja de la misma.
- Cada jugador dispone de fichas de su color.
- En cada intersección fila-columna solo puede haber una ficha de un color.
- El juego se desarrolla por turnos, humano-maquina-humano-maquina[…], introduciendo cada uno una ficha de su color en una columna.
- Se repite el intercambio de turnos hasta que uno de los dos jugadores alcance la condición de victoria.
- Se considera victoria en caso que se encuentren alineadas en vertical, horizontal o diagonal 4 fichas del mismo color (del mismo jugador).
- Se considera para la aplicación que siempre inicia el jugador humano.

#### Características del desarrollo:
- La aplicación se desarrolla en lenguaje de programación JavaScript, empleando una capa de presentación con HTML y CSS para la aplicación de estilos.
- La interacción por parte del jugador humano se realiza mediante un navegador web y el empleo de punteros o ratón, seleccionando la columna donde se introduciría la ficha.

## 4. Desarrollo

Se especifican los métodos principales que intervienen en el desarrollo del juego y que son relevantes desde el punto de vista de la IA.

#### Presentación.

Se emplea un método `iniciarPartida()`, el cual dibuja el tablero, y activa los Listener para que se desencadenen las jugadas a partir de la interacción por parte del jugador.

#### Juego.

Se emplean como métodos generales para el desarrollo del juego: 
- Método para `comprobarganador()`, el cual determina si se da la condición de victoria.
- Método para `empate()`, el cual determina si se da la condición de empate.

#### Algoritmo MINIMAX

Se emplea el método ```valorarJugada()``` el cual determina a partir de la situación las posibles ramificaciones, determinando las condiciones mínima y máxima, para la máquina y el jugador, determinando así la mejor jugada.

En este método se introduce el factor de profundidad, el cual determina el numero de ramificaciones que se desciende en la valoración.

## 5. Conclusiones

Como condicionante clave para el desarrollo de la búsqueda de la mejor jugada por parte de la máquina, se ha demostrado que variando la profundidad de exploración de las ramas, se pueden obtener mejores jugadas por parte de ésta (más inteligentes).

En contrapartida, los tiempo requeridos para realizar la búsqueda se dilatan, pudiendo llegara a hacer el juego poco atractivo para el jugador humano por los tiempos de espera para la decisión de la máquina.