# ****TRES EN RAYA****

## Descripcion


## Funciones principales del código
| **Función** | **Descripción** |
|--|--|
|***void showBoard(char board[][SIDE])***| Esta funcion muestra el status actual del tablero y cuenta con printf con la respectiva posicion. |
|***void showInstructions()***| Esta funcion muestra las instrucciones, cuenta con printf y muestra el numero de cada casilla.|
|***void initialise(char board[][SIDE])***| Esta funcion es utilizada para iniciar el juego tres en raya, esta formada por dos for que recorreran toda la tabla y la vacian. |
|***void declareWinner(int whoseTurn)***| Esta funcion permite conocer el ganador del juego y cuenta con una condicion para que se pueda mostrar el ganador, en este caso la computadora o el humano.|
|***bool rowCrossed(char board[][SIDE])***| Esta funcion muestra cuando el mismo participante tiene 3 jugadas en la misma fila, cuenta con un for, que recorre la lista en fila, con una condicion que permite comparar el movimiento con el resto de casillas marcadas.|
|***bool columnCrossed(char board[][SIDE])***| Esta funcion muestra cuando el mismo participante tiene 3 jugadas en la misma columna, cuenta con un for, que recorre la lista en columna, con una condicion que permite comparar el movimiento con el resto de casillas marcadas. |
|***bool diagonalCrossed(char board[][SIDE])***| Esta funcion muestra cuando el mismo participante tiene 3 jugadas en la misma diagonal, cuenta con 2 if donde comparamos 2 posibles casos diagonales de la primera, quinta y novena casilla, y para el otro caso la tercera, quinta y septima casilla.|
|***bool gameOver(char board[][SIDE])***| Esta funcion muestra si termina o no el juego y cuenta con un retorno de verdadero o falso, verdadero para terminar y falso para continuar.|
|***int minimax(char board[][SIDE], int depth, bool isAI)***| Esta funcion ayuda a evaluar el mejor score, si de la computadora o del humano, cuenta con condiciones y for para recorrer la lista y poder mejorar el calculo del puntaje. |
|***int bestMove(char board[][SIDE], int moveIndex)***| Esta funcion es para la computadora nada mas y se evalua las posiciones libres para realizar la jugada, cuenta con 2 for donde recorren la lista, 2 if, el primer if es para verificar que este disponible el espacio de la casilla y el segundo para realizar el mejor movimiento.|
|***void playTresEnRaya(int whoseTurn)***| Esta funcion ayuda a que sigan jugando hasta que el juego termine o haya un empate, mostrara los puestos libres y tambien las celdas ocupadas, quien gano y cuanta con la mayoria de las funciones mencionadas previamente. |
|***int main()***| Esta es nuestra funcion principal para poder ejecutar nuestro codigo, cuenta con un switch con las opciones de si desea o no que comience la computadora, tambien para poder finalizar el juego y por si existe algun error al momento de ingresar el numero. | 

## Tiempo de los mejores y peores casos 
Podemos decir que este codigo ayudaria a minimizar las perdidas de la computadora dando asi un mejor rendimiento y una gran dificultad al jugador para que de esa manera dar un excelente resultado.
- Jugador 1 Computadora (O)
- Jugador 2 Humano (X)
Nuestro primero caso

| **Imagen** | **Proceso Computadora** | **Proceso Humano**| **Tiempo**|
|--|--|--|--|
|![image](https://upload.wikimedia.org/wikipedia/commons/3/32/Tic_tac_toe.svg)|1. Casilla 9 O, 3. Casilla 6 O, 5. Casilla 8 O, 7. Casilla 1 O, 9. Casilla 5 O|2. Casilla 7 X, 4. Casilla 3 X, 6. Casilla 2 X, 8. Casilla 4 X| 1:20|

*Explicacion:* Como podemos notar aqui existió un fallo de parte del humano como comun mente suele suceder, encontramos que la computadora tiene 5 movimientos y el humano tiene 4 por lo que el marcador esta Computadora 1 - Humano 0, con un tiempo aproximado de un minuto con 20 segundos.

| **Imagen** | **Proceso Computadora** | **Proceso Humano**| **Tiempo**|
|--|--|--|--|
|![image](https://user-images.githubusercontent.com/121835070/210359071-db631cea-00b3-4717-a007-504d75cec646.png)|2. Casilla 1 O, 4. Casilla 2 O, 6. Casilla 6 O|1. Casilla 5 X, 2. Casilla 9 X, 5. Casilla 3 X, 7. Casilla 7 X| 1:00|


## Estudio combinatorio del juego
Los árboles de decisión son herramientas para ayudar a tomar la decisión correcta entre muchas opciones. Su estructura te permite elegir diferentes opciones una y otra vez para explorar diferentes escenarios de decisión posibles. Los árboles de decisión son guías multidireccionales jerárquicas en las que los valores propios son criterios de diagnóstico para evaluar y determinar el uso más adecuado. La jerarquía es cuando una decisión o camino conduce a otro hasta que se consideran todos los factores o características involucradas. Es multidireccional porque puede haber más de dos opciones y es indicativo porque responder una pregunta lleva a una decisión.

Debemos añadir que el numero de posibilidades va cada vez menos ya que
![image](https://user-images.githubusercontent.com/121835070/210329562-af6a9870-9403-4462-ba82-e72020aee4d4.png)


## Código en Windows y Linux


## Integrantes
- Fabiana Vásconez
- Juan David Ramirez
- Said Cabrera
- Daniel Vizcarra
