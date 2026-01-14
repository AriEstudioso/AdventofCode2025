# AdventofCode2025

Ejercicio 1:
-Creamos una public class con un nombre adecuado.
-Creamos una variable para almacenar los datos de entrada. Mientras no se acabe la linea vamos añadiendo los datos a rotation.
-LLamamos al metodo CountZeros() el cual creamos posteriormente. Este recibe la lista de instrucciones.
-Creamos las variables dir(direccion) y steps(numero de pasos)
-Si pide girar a la derecha nos movemos la cantidad de steps que nos pide y sei es a la izquierda lo mismo.
-Comprobamos si la posicion esta en 0. Si es asi contamos +1 cero.
-Devolvemos el numero de ceros que habia

Ejercicio 1.2:
-Esta vez cuenta cuantas veces ha pasado por cero sin tener que pararse en el para que cuente.
-Ahora simplemente en la direccion que nos piden utilizamos un for para dar el numero de pasos que nos piden y si en algun momento 
pasamos por 0 entonces se suma +1 al contador de ceros.

Ejercicio 2:
-Creamos la public class con un nombre adecuado.
-Creamos una variable buffer para poder leer los caracteres de la string. En este caso seran rangos de numeros separados por - y ,.
-Dividimos los rangos por ",".
-En cada rango usamos split para separar los valores de "-" y cogerlos individualmente.
-Recorro todo lo que se encuentra dentro del rango incluyendo estos. Utilizo fuerza bruta.
-Si se cumple la condicion se suma al total.
-Creamos el metodo que definira que significa que sea invalido.
-Si el numero tiene una cantidad impar de digitos no puede dividirse por lo tanto devolvemos falso.
-Luego si era par comprobamos que ambas mitades sean iguales con el metodo first.equals().

Ejercicio 2.2:
-Se pide que ahora tiene que estar repetido al menos dos veces.
-Probamos todas las longitudes del patron pero nunca mas de la mitad del numero porque no nos interesan evaluar esos casos
-El patron debe encajar. No pueden ser 2 numeros y luego 3 por ejemplo la comparacion. Tiene que ser exactos 2 y 2 o 3 y 3...
-Reconstruimos el numero y hacemos un equals para ver si es igual.

Ejercicio 3:
-Creamos variables para leer input y almacenar lineas.
-Recorremos cada linea y comprobamos cual es el mayor numero de dos digitos posible que se puede formar en dicha linea.
-Se le suma al total.
En el metodo maxTwoDigit cogemos el mayor numero de 1 digito y luego recorremos la linea intentando emparejarlo con otro para formar 
el numero de 2 digitos mas grande.

Ejercicio 3.2:
-Ahora utilizamos greedy(voraz) para elegir en cada paso el mejor digito posible sin comprometer al resultado final
-Ahora se busca el mayor numero posible de 12 digitos en vez de 2 digitos
-Se eligen k digitos(12) y en cada iteracion se añade uno a la solucion final.
-Igual que antes buscamos el mejor digito posible en el rango.
-Lo devolvemos como String

Ejercicio 4:
-Creamos variables para leer input y almacenar lineas. Cada linea representa una cuadricula.
-Creamos una matriz 2D. Definimos sus columnas y filas en la que cada fila es un array de caracteres.
-En el metodo creamos las direcciones de los 8 vecinos. 
-Recorremos cada posicion comprobando que la célula sea válida. Solo se considera válida los @.
-Contamos los vecinos que estan dentro de los limites. Una posicion se considera accesible si hay menos de 4 vecinos @.
-Result devuelve la cantidad de posiciones accesbles.

Ejercicio 4.2:
-Inicializamos el grid dinamico
-Cada linea se convierte en un array de carcteres que se añade al grid dinamico.
-Llamamos al TotalRemove
-Mientras no se elimine nada cada ronda tiene su matriz remove temporal en la que se marcaran los lugares que deben eliminarse.
-Recorre sus 8 vecinos y si hay alguno accesible(con < 4) se elimina.
-Si ninguna posicion se marca para eliminar pues termina su trabajo
-Remplazamos el @ por un . despues de procesr la ronda para no afectar al resto.
-Devolvemos el total de elementos removidos

Ejercicio 5:
-Creamos una clase interna dentro de public Day5 para representar el rango de numeros para poder reutilizar la logica.
-Creamos un objeto rango en el que almacenar su rango en su lista ranges.
-Creamos el contador de IDs
-Comprobamos que la ID se encuentra dentro de los rangos.
-Se imprime cuantos IDs estan dentro de algun rango.

Ejercicio 5.2:
-Fusiona rangos solapados.
-Utlizo un Comparator para ordenar desde el inicio. Ordenamos los rangos de menor a mayor.
-Inicializamos los rangos de fusion.
-Empezamos a fusionarlos para que si tenemos un rango de 1-5 y otro de 3-7 convertirlo ne un unico rango de 1-7.
-Comprobamos que la ID se encuentra dentro de los rangos.
-Se imprime cuantos IDs estan dentro de algun rango.



