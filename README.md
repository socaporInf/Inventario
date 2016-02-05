# Inventario
sistema de control de inventario
documentacion de plantilla:

constructor.js

clases:

	Arquitecto:

		atributos:

			elementos:
				este es un arreglo donde se guardan los elementos que conforman la interfaz de usuario

				generalmente guardan 4 elementos basicos:
				
				-menu
				-cabecera
				-formulario
				-botononera
				-ventanaModal

			estado:
				este atributo guarda el estado actual de elemento

		funciones:

			configure:
				parametros: ninguno

				esta funcion se encarga de inicializar los 4 elementos principales de la clase.

				solo los elementos menu y cabecera son incializados como objetos, y los elementos formulario y botonera son incializados con el valor de texto "noPosee"

			crearVentanaModal:
				parametros: 
					data: este parametro contiene la estructura de la ventana modal a crear

				en esta funcion se crea una ventana modal y se agrega el objeto al arreglo de elementos para su facil acceso atraves del mismo

	Menu:

		atributos:

			estado:
				este atributo guarda el estado actual del objeto se inicializa en el valor "porConstruir"

			capaActiva:
				en este se guarda la capa del menu sobre la cual esta parado el usuario de modo que si desea navegar pueda utilizar este valor para lo mismo

			nodo:
				el nodo dom dentro del documento html, de manera que pueda ser utilizado y ubicado de manera rapida

			hijos:
				aqui se guardan las capas hijo del menu como raiz, para poder utilizar el funcionamiento de arbol

		funciones:

			construir:
				paramentros: nada

				esta funcion es la que se invoca cuando se crea una instancia de la clase, contruyendo el menu y todo su funcionamiento

			getEstado:
				parametros: nada

				retorna el valor del atributo estado

			abrirMenu:
				parametros: nada

				esta funcion activa el menu en la interfaz, mostrandolo en la misma

			activarCapa:
				parametros: 
					capa: aqui se pasa como parametro el objeto de tipo Capa

				esta funcion recibe la capa y la coloca como activa, es decir la que va estar visible para el usuario

			avanzar:
				parametros:
					nodo: el nodo que contiene el valor de la capa a avanzar

				esta funcion recive el nodo al cual se le hace click y contiene el id de la capa a la cual se va a avanzar de la raiz hacia las ramas

			retroceder:
				parametros: nada

				hace un moviento de las ramas hacia la raiz










