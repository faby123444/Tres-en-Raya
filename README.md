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


## Estudio combinatorio del juego


## Código en Windows y Linux


## Integrantes
- Fabiana Vásconez
- Juan David Ramirez
- Said Cabrera
- Daniel Vizcarra
