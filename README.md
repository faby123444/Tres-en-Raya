# ****TRES EN RAYA****

## Descripcion
La historia del tres en raya tal y como lo conocemos se remonta a casi mil años a la lejana Persia, desde donde los comerciantes italianos lo exportaban y difundían a sus países. En poco tiempo se convirtió en uno de los juegos más populares de las clases bajas en la Edad Media. En España hay sobradas pruebas de lo extendido que estaba este juego. 
1.	Tenemos que pintar un tablero con nueve celdas. Se dibujan dos líneas horizontales y dos verticales, formando una cuadrícula de nueve espacios. 
2.	 Un jugador puede usar, cruces y otro, círculos para marcar las casillas. Gana el que consiga hacer línea ya sea vertical, horizontal o diagonal.
3.	Las casillas se van marcando de una en una, por jugada, de tal forma que cuenta con ventaja el que primero tira, eso no quiere decir que sea el que finalmente gane.
4.	 Gana el que consiga hacer línea (horizontal, vertical o diagonal).

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

| **Imagen** |**Proceso**| **Tiempo**|
|--|--|--|
|![image](https://upload.wikimedia.org/wikipedia/commons/3/32/Tic_tac_toe.svg)|1. Casilla 9 O-Computadora, 2. Casilla 7 X-Humano, 3. Casilla 6 O-Computadora, 4. Casilla 3 X-Humano, 5. Casilla 8 O-Computadora, 6. Casilla 2 X-Humano, 7. Casilla 1 O-Computadora, 8. Casilla 4 X-Humano, 9. Casilla 5 O-Computadora | 1:20|

*Explicacion:* Como podemos notar aqui existió un fallo de parte del humano como comun mente suele suceder, encontramos que la computadora tiene 5 movimientos y el humano tiene 4 por lo que el marcador esta Computadora 1 - Humano 0, con un tiempo aproximado de un minuto con 20 segundos.

| **Imagen** |**Proceso**| **Tiempo**|
|--|--|--|
|![image](https://user-images.githubusercontent.com/121835070/210359071-db631cea-00b3-4717-a007-504d75cec646.png)|1. Casilla 5 X-Humano,2. Casilla 1 O-Computadora, 3. Casilla 9 X-Humano,4. Casilla 2 O-Computadora, 5. Casilla 3 X-Humano,6. Casilla 6 O-Computadora, 7. Casilla 7 X-Humano| 1:00|

*Explicacion:* En este caso la computadora falló, dando asi al humano 4 movimientos y la computadora 3 movimientos en un lapso de 1 minutos nada mas, cambiando asi el marcador a Computadora 1 - Humano 1.

| **Imagen** |**Proceso**| **Tiempo**|
|--|--|--|
|![image](https://user-images.githubusercontent.com/121835070/210361578-4a5da31d-15a5-4e75-9808-140073c9e9f3.png)|1. Casilla 1 X-Humano,2. Casilla 4 O-Computadora, 3. Casilla 5 X-Humano,4. Casilla 9 O-Computadora, 5. Casilla 6 X-Humano,6. Casilla 2 O-Computadora, 7. Casilla 7 X-Humano,8. Casilla 3 O-Computadora, 9. Casilla 8 X-Humano| 1:33|

*Explicacion:* En este ejemplo hay un empete con 5 movimientos el humano y 4 la computadora, el tiempo marco 1 minuto con 33 segundos ya que el humano demoro un poco mas en responder que la anterior vez, el marcador se mantiene con Computadora 1 - Humano 1.

##### Explicacion general
*Hubo un promedio de respuesta de la computadora de 30 milisegundo y aproximadame de 24 segundos del humano, consideramenos que el mejor caso es la derrota de la computadora con 4 movimientos y el peor caso es el empate o perdida del humano.*

## Estudio combinatorio del juego
Los árboles de decisión son herramientas para ayudar a tomar la decisión correcta entre muchas opciones. Su estructura te permite elegir diferentes opciones una y otra vez para explorar diferentes escenarios de decisión posibles. Los árboles de decisión son guías multidireccionales jerárquicas en las que los valores propios son criterios de diagnóstico para evaluar y determinar el uso más adecuado. La jerarquía es cuando una decisión o camino conduce a otro hasta que se consideran todos los factores o características involucradas. Es multidireccional porque puede haber más de dos opciones y es indicativo porque responder una pregunta lleva a una decisión.

Como podemos notar al tomar un decision tanto como el humano y computadora si inician de nuevo tienen la opcion de escoger cualquiera de las 9 casillas para la segunda toma de decision ya solo tendra disponible 8 de las nueve casillas y de esa manera ira disminuyendo cada una de las posibilidades hasta que hayan ganado o se dará un empate, en nuestro ejemplo se puede notar evidentemente un empate siendo 1 el humano y 2 la computadora.

![image](https://user-images.githubusercontent.com/121835070/210329562-af6a9870-9403-4462-ba82-e72020aee4d4.png)


## Código en Windows y Linux
Debemos tomar en cuenta que para poder ejectura el código en Linux y Windows se debe tener un compilador compatible y Visual Studio Code, es decir se va a genera un problema al momento de querer iniciar el juego, para que esto no suceda se puede ayudar con el siguiente video.
Video:https://www.youtube.com/watch?v=v3ENcQpoA5A&ab_channel=FaztCode
Pagina: https://www.msys2.org
De esta manera ya no existirá ningun otro inconveniente.
*No olvides poner la direccion al path*

## Integrantes
- Fabiana Vásconez
- Juan David Ramirez
- Said Cabrera
- Daniel Vizcarra
