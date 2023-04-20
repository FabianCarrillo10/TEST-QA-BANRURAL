La estrategia puede ser resumida de esta forma:
 1. Ejecutar script y observar errores
 2. Refrescar ideas en Javascript
 3. Analizar el código 
 4. Buscar funciones que sean de utilidad

Como primer punto se ejecutó el código en el navegador, haciendo uso de la consola fue fácil detectar el primer error, "addeventListener", una simple letra causó que el programa no funcione correctamente, arreglado esto apareció otro error "lowOrHi" ya que no estaba definido correctamente dentro del script por un . (punto). 

Una vez realizado esto era turno de refrescar un poco sobre el lenguaje y analizar el código. Mientras buscaba en el archivo, encontré errores de sintaxis y lógicos, por ejemplo, el número aleatorio no generaba datos de 1 a 100, los intentos estaban reducidos a 5, el color del texto estaba revuelto y algunos if tenían el código incorrecto, todo esto se detalla en los comentarios agregados en index.html.

La generación del número aleatorio fue colocada dentro de una nueva función con el objetivo de ser llamada desde otras funciones. ¿Por qué realizar esto? Bueno, luego de algunas pruebas pude notar que el juego se reiniciaba pero el número era el mismo, ya que se generaba al principio solamente y nunca se volvía a generar, usando esta función es posible generar un nuevo número cada que el usuario adivine/falle mediante una llamada en la función resetGame(). 

Finalmente llegó el turno de agregar código, debido a que se solicita la validación de valores enteros, esto fue resuelto utilizando la función Math.floor() en la que se realiza una comparación, si el valor de Math.floor(userGuess) restado a userGuess es igual a 0, significa que userGuess no tiene decimales, por lo tanto es un dato entero y aplica para los if que ya estaban definidos. Por último, se agregó un else que le da un mensaje al usuario de advertencia, solicitando que ingrese solamente valores enteros. Como detalle extra, con la validación realizada si un usuario ingresa una letra, tendrá el mismo mensaje de advertencia y su intento no contará.

Esto sería mi planteamiento y cómo abordé el problema para obtener una solución.