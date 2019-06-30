__          __                        _____                      
\ \        / /                       / ____|                     
 \ \  /\  / /_ _ _ __  _ __   ___   | |  __  __ _ _ __ ___   ___ 
  \ \/  \/ / _` | '_ \| '_ \ / _ \  | | |_ |/ _` | '_ ` _ \ / _ \
   \  /\  / (_| | |_) | |_) | (_) | | |__| | (_| | | | | | |  __/
    \/  \/ \__,_| .__/| .__/ \___/   \_____|\__,_|_| |_| |_|\___|
                | |   | |                                        
                |_|   |_|  
 ___       _             __           
|_ _|_ __ | |_ ___ _ __ / _| __ _ ____
 | || '_ \| __/ _ \ '__| |_ / _` |_  /
 | || | | | ||  __/ |  |  _| (_| |/ / 
|___|_| |_|\__\___|_|  |_|  \__,_/___|

-----------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------

Lo primero de todo es abrir el Spyder o similar y abrir el archivo INTERFAZ.py.
Despu�s simplemente tendremos que ejectar el archivo y ya se ejecutar� el spript,
con el cual podremos realizar cualquier tipo de prueba, usando diferentes algoritmos
para resolver niveles con uno y dos monstruos, sean del juego o inventados por nosotros.

** ES MUY IMPORTANTE INTRODUCIR LOS N�MEROS QUE SE INDICAN, NORMALMENTE ENTRE PAR�NTESIS,
EN LA CONSOLA, adem�s de tener en cuenta aspectos como que la casilla superior izquierda
del mapa es la (0,0) y que hacia abajo la primera coordenada aumenta, al igual que la
segunda coordenada aumenta al ir hacia la derecha, al igual que si existe alguna fila o
columna vac�a o inexistente en el mapa sus celdas cuentan y tienen cada una sus propias
coordenadas **

 __  __                                                                      _           
|  \/  | __ _ _ __   __ _ ___   _ __  _ __ ___  ___ __ _ _ __ __ _  __ _  __| | ___  ___ 
| |\/| |/ _` | '_ \ / _` / __| | '_ \| '__/ _ \/ __/ _` | '__/ _` |/ _` |/ _` |/ _ \/ __|
| |  | | (_| | |_) | (_| \__ \ | |_) | | |  __/ (_| (_| | | | (_| | (_| | (_| | (_) \__ \
|_|  |_|\__,_| .__/ \__,_|___/ | .__/|_|  \___|\___\__,_|_|  \__, |\__,_|\__,_|\___/|___/
             |_|               |_|                           |___/                       

Una vez ejecutado el programa nos preguntar� si queremos cargar un nivel 
precargado, de los cuales disponemos desde el nivel 0 al nivel 14, adem�s
de 4 niveles de prueba dise�ados por nosotros mismos. Debe simplemente
marcar por consola culquier n�mero del 1 al 19 para seleccionar cualquiera.

Cuando seleccione cualquier mapa o cree uno propio, el programa le preguntar� si
es el mapa que desea  represent�ndolo gr�ficamente mediante un m�todo que hemos dise�ado:

.-----..-----..-----..-----..-----..-----.#######
|     ||     ||     ||     ||     ||     |#######
|     ||     ||     ||     ||     ||     |#######
#######.-----..-----..-----..-----..-----.#######
########-----..-----..-----..-----..-----.#######
|M   M##     ||     ||     ||     ||     |#######
|M   M##     ||     ||     ||     ||     |#######
.-----##-----..-----..-----..-----..-----.#######
.-----##-----..-----..-----..-----..-----..-----.
|     ##     ||     ||     ||     ||     ||O O O|
|     ##     ||     ||     ||     ||     ||O O O|
.-----##-----..-----..-----..-----..-----..-----.
.-----##-----..-----..-----..-----..-----.#######
|     ##     ||     ||     ||     ||     |#######
|     ##     ||     ||     ||     ||     |#######
.-----##-----..-----..-----..-----..-----.#######
.-----..-----..-----..-----..-----..-----.#######
|     ||     ||P   P||     ||     ||     |#######
|     ||     ||P   P||     ||     ||     |#######
.-----..-----..-----..-----..-----..-----.#######
.-----..-----..-----..-----..-----..-----.#######
|     ||     ||     ||     ||     ||     |#######
|     ||     ||     ||     ||     ||     |#######
.-----..-----..-----..-----..-----..-----.#######

Ejemplo del nivel 0.

Una vez seleccionado un mapa, le preguntar� con que algoritmo de b�squeda desea intentar resolver
el mapa:

�Con qu� algoritmo de b�squeda quieres intentar resolver el mapa?
- B�squeda en anchura (1)
- B�squeda en profundidad (2)
- B�squeda con A* (3)

Simplemente se debe indicar en la consola de comandos con qu� algoritmo se quiere resolver el mapa. Seleccionando
el tercer algoritmo, A*, nos preguntar� a continuaci�n coste y heur�stica, a no ser que el nivel cargado sea de dos monstruos.
En este caso solo preguntar� por el coste.

�Qu� funci�n de coste quieres usar?
- Coste 0 para cada nodo (1)
- Coste 1 para cada nodo (2)

�Qu� funci�n de heur�stica quieres usar?
- Distancia Manhattan (Personaje - Objetivo) (1)
- Heur�stica contemplando diferentes situaciones, con preferencia a la casilla ardiente m�s cercana al personaje (2)
- Heur�stica contemplando diferentes situaciones, con preferencia a la casilla ardiente m�s lejana al personaje (3)
- Heur�stica contemplando diferentes situaciones, con preferencia a una casilla ardiente aleatoria (4)
- Heur�stica contemplando diferentes situaciones, con preferencia a una casilla ardiente aleatoria y teniendo en cuenta situaciones en las que el monstruo queda encajado en dos paredes contiguas (5)

El script nos preguntar� si queremos que el algoritmo nos muestre todos los nodos a tiempo real. 
Esto se pregunta por si no queremos que nos muestre todos los nodos por los que va explorando y nos llene la consola
de informaci�n.

Por �ltimo nos preguntar� si queremos que la reoluci�n se escribe en un fichero "resoluci�n_wappo.txt" que se encontrar�
en la ra�z del proyecto, mostr�ndonos todos los nodos por los que hay que pasar hasta llegar a la solcui�n o si por el
contrario que simplemente nos muestre por la consola los movimientos que hay que hacer, el tiempo y los nodos sin mostrarnos
una representaci�n gr�fica de cada paso.

 ____        __ _       _        __  __                   
|  _ \  ___ / _(_)_ __ (_)_ __  |  \/  | __ _ _ __   __ _ 
| | | |/ _ \ |_| | '_ \| | '__| | |\/| |/ _` | '_ \ / _` |
| |_| |  __/  _| | | | | | |    | |  | | (_| | |_) | (_| |
|____/ \___|_| |_|_| |_|_|_|    |_|  |_|\__,_| .__/ \__,_|
                                             |_|          

Si seleccionamos que queremos hacer un mapa manualmente nos preguntar� poco a poco todos los detalles
del mapa:

1.	Preguntar� cuantas filas tiene el mapa
2.	Preguntar� cuantas columnas tiene el mapa
3.	Preguntar� si existe alguna fila o columna inexistente.
		Esto se pregunta por si la casilla objetivo se encuentra fuera del mapa,
		es decir, si es 4x5 (Filas X Columnas) y el casilla est� en la columna 5
		pero el resto de la columna es inaccesible. Si respondes 3 se dar� por 
		hecho que no est� fuera del mapa.

Cabe destacar que el mapa se empeiza a contar desde 0, es decir, que la celda que est� arriba
a la izquierda ser� la 0,0

4.	Preguntar� la fila de la celda objetivo.
5.	Preguntar� la colunma del a celda objetivo.	
6.	Preguntar� la fila del personaje.
7.	Preguntar� la colunma del personaje.	
8.	Preguntar� la fila del monstruo.
9.	Preguntar� la colunma del monstruo.
10.	Preguntar� si se desea a�adir un segundo monstruo.
		Si respondemos que si:
			Nos preguntar� cual es la fila
			Nos preguntara cual es la columna
		Si respondemos que no seguiremos.
11.	Preguntar� si queremos a�adir una casilla ardiente
		Si respondemos que si:
			Nos preguntar� cual es la fila
			Nos preguntar� cual es la columna
			Nos volver� a preguntar si queremos a�adir otra
		Si respondemos que no seguiremos.

12.	Nos preguntar� si queremos a�adir alguna pared:
		Si respondemos que si
			Nos preguntar� la fila de la primera celda que compone la pared.
			Nos preguntar� la columna de la primera celda que compone la pared.
			Nos preguntar� la fila de la segunda celda que compone la pared.
			Nos preguntar� la columna de la segunda celda que compone la pared.
			Nos volver� a preguntar si queremos a�adir otra
		Si respondemos que no seguiremos.

13. Finalmente nos mostrar� una representaci�n del mapa obtenido y se repetir� el proceso
de selecci�n de los diferentes par�metros, como al seleccionar y un nivel precargado.

__          __                        _____                      
\ \        / /                       / ____|                     
 \ \  /\  / /_ _ _ __  _ __   ___   | |  __  __ _ _ __ ___   ___ 
  \ \/  \/ / _` | '_ \| '_ \ / _ \  | | |_ |/ _` | '_ ` _ \ / _ \
   \  /\  / (_| | |_) | |_) | (_) | | |__| | (_| | | | | | |  __/
    \/  \/ \__,_| .__/| .__/ \___/   \_____|\__,_|_| |_| |_|\___|
                | |   | |                                        
                |_|   |_|  
 __  __                         _ 
|  \/  | __ _ _ __  _   _  __ _| |
| |\/| |/ _` | '_ \| | | |/ _` | |
| |  | | (_| | | | | |_| | (_| | |
|_|  |_|\__,_|_| |_|\__,_|\__,_|_|

-------------------------------------------------------------------------------
-------------------------------------------------------------------------------

** IMPORTANTE DESTACAR EL USO DE LAS CLASES MAPA Y MOVERPERSONAJE PARA NIVELES
DE UN SOLO MONSTRUO Y LAS CLASES MAPA2 Y MOVERPERSONAJE2 PARA NIVELES CON DOS
MONSTRUOS **

  __  __                    
 |  \/  |__ _ _ __  __ _ ___
 | |\/| / _` | '_ \/ _` (_-<
 |_|  |_\__,_| .__/\__,_/__/
             |_|            

Tendremos que abrir el Sypder o similar y abrir el archivo MANUAL.py para
niveles con un monstruo o el archivo MANUAL2.py para niveles con dos monstruos.
Dentro de cada archivo encontraremos una peque�a aclaraci�n de como
definimos los tipos de casillas dentro de la matriz:

Tipos de casillas:
0 -> Normal
1 -> Ardiente
2 -> Objetivo
3 -> Inaccesible

Despu�s tendremos unos cuantos niveles definidos, simplemente tendremos que ir
comentandolos y descomentando los que queremos seleccionar. Por defecto est� 
seleccionado el nivel 0. Simplemente tendremos que quitar """ del t�tulo
Nivel 0 y poner las comillas al final. Para descomentar otro nivel se har� lo
mismo pero a la inversa, a�adimos comillas al lado del t�tulo y quitamos las 
comillas puestas al final del nivel.

Si queremos definir un nivel de forma manual tendremos que definir una matriz
de mxn, donde m y n son las dimensiones deseadas:

	matrix = np.zeros((7, 6))

Despu�s, en el caso en el que el objetivo est� fuera del mapa, habr� que a�adir
un 3 a la fila o a la columna en el que se encuentre el objetivo:

	for i in range(0,6):
    		matrix[6,i] = 3

Despu�s habr� que definir d�nde se encuentra el objetivo:

	matrix[6,3] = 2

Y definir, si deseamos las casillas ardientes:

	matrix[1,1] = 1

Despu�s definiremos las paredes por pares de casillas, indicando que entre esas
dos casillas se encuentra una pared:

	pared1 = Pared(0,5,1,5)
	pared2 = Pared(1,4,1,5)
	pared3 = Pared(5,5,5,4)
	pared4 = Pared(0,3,1,3)
	pared5 = Pared(1,1,2,1)

Y a�adirlos a una lista.

	paredes = [pared1, pared2, pared3, pared4, pared5]

Lo �tlimo ser� definir la posici�n del personaje y del monstruo o monstruos, seg�n el caso:

	personaje = Personaje(1,3)
	monstruo = Monstruo(1,5)

Y finalmente, seg�n si es un nivel con un monstruo o dos:
	
	mapa = Mapa(matrix, paredes, monstruo, personaje)
	mapa = Mapa2(matrix, paredes, monstruo1, monstruo2, personaje)

 ___ ___ _    ___ ___ ___ ___ ___  _  _   ___  ___   _  _ ___ _   _ ___ ___ ___ _____ ___ ___   _   
 / __| __| |  | __/ __/ __|_ _/ _ \| \| | |   \| __| | || | __| | | | _ \_ _/ __|_   _|_ _/ __| /_\  
 \__ \ _|| |__| _| (_| (__ | | (_) | .` | | |) | _|  | __ | _|| |_| |   /| |\__ \ | |  | | (__ / _ \ 
 |___/___|____|___\___\___|___\___/|_|\_| |___/|___| |_||_|___|\___/|_|_\___|___/ |_| |___\___/_/ \_\
                                                                                                     


En el caso de que vayamos a usar A*, deberemos elegir aqu� la heuristica que deseemos usar, se elegir� 
de la misma forma que hemos elegido el mapa, comentando y descomentando.


  ___ ___ _    ___ ___ ___ ___ ___  _  _   ___  ___    ___ ___  ___ _____ ___ 
 / __| __| |  | __/ __/ __|_ _/ _ \| \| | |   \| __|  / __/ _ \/ __|_   _| __|
 \__ \ _|| |__| _| (_| (__ | | (_) | .` | | |) | _|  | (_| (_) \__ \ | | | _| 
 |___/___|____|___\___\___|___\___/|_|\_| |___/|___|  \___\___/|___/ |_| |___|
                                                                              

En esta secci�n elegiremos el coste, comentando y descomentando de la misma forma que las anteriores veces.


  ___   _ ___ ___ _   _ _____ _   __  __  ___  ___ 
  | __| | | __/ __| | | |_   _/_\ |  \/  |/ _ \/ __|
  | _| || | _| (__| |_| | | |/ _ \| |\/| | (_) \__ \
  |___\__/|___\___|\___/  |_/_/ \_\_|  |_|\___/|___/
                                                    

En esta secci�n elegiremos los �tlimos detalles. Como el m�todo de b�squeda

busq = busqee.BusquedaAEstrella(h, detallado=False)
# busq = busqee.BusquedaEnAnchura(detallado=False)
# busq = busqee.BusquedaEnProfundidad(detallado=False)

En este caso tenemos seleccionado A*.

Por �ltimo podemos decidir si nos representar� todo por consola o escribiendolo en un fichero en el directorio del proyecto.
Comentando y descomentando de la misma forma que en los anteriores casos.