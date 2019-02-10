# Programa para el diseño de controladores digitales por el método del LGR

_El programa implementa y diseña en Matlab el preoceso de diseño de controladores digitales por el método del Lugar Geométrico de las Raíces._

## Comenzando 🚀

_Estas instrucciones te permitirán obtener una copia del proyecto en funcionamiento en tu máquina local para propósitos de desarrollo y pruebas._

Mira **Deployment** para conocer como desplegar el proyecto.


### Pre-requisitos 📋

_Solo se necesita tener instalado Matlab en las versión igual o superior a la R2018a._

![matlab](https://user-images.githubusercontent.com/45041472/52538936-a292c880-2d46-11e9-97cb-5565695fd2ec.JPG)

### Instalación 🔧

_Primero es necesario descomprimir el archivo, y estar en el directorio C:\Users\USUARIO\'lugar de descarga'\LGRFinal\LGR-master\Programa1.0_

_Abrir el archivo control2.m, que se encuentra en el respectiva carpeta._

![archivo](https://user-images.githubusercontent.com/45041472/52539319-bb9d7880-2d4a-11e9-971e-51af9bfa09c6.JPG)

_Ya con el archivo .m abierto, simplemente ejecuta el código, y se abrirá el panel de diseño._

![pagprincipal](https://user-images.githubusercontent.com/45041472/52539357-3d8da180-2d4b-11e9-9d1c-630db3a74f61.JPG)

_En el programa se puede ver las opciones elegibles, como lo es ingresar la función de transferencia de la planta en tiempo continuo, es importante mencionar que la variable 's' se interpreta como una variable simbólica, con el fin de definir fácilmente cualquier función de tranferencia, incluyendo las que involucran retardos. Iguelmente la opción de ingresa el valor del periodo de muestreo en segundos, en caso contrario, se calculará de manera automática el mejor periodo de muestreo para la planta ingresada, igualmente esta opción identifica si la planta presenta retardo._

_De manera opcional se da la opción de graficar la planta (sin controlador), permite graficar el LGR, la respuesta escalón, rampa y parabola en tiempo continuo y tiempo discreto. Igualmete como algo adiciónal se encuentra las principales carácteristicas de la planta en tiempo continuo  en lazo cerrado, y la representación por código LaTex de la función de tranferencia en lazo abierto en tiempo continuo y discreto._

_Cuando se da click en el botón Diseño, se abre la siguiente ventana._

![diseno](https://user-images.githubusercontent.com/45041472/52539611-4cc21e80-2d4e-11e9-8f0d-1eb203f9378c.JPG)

_La ventana permite configurar el diseño del controlador, permitiendo en primer lugar seleccionar entre diferentes parejas de condiciones, cada configuración permite diferente opciones de rediseño automático, lo cual puede ser práctico para implementar controladores adecuados para plantas de diseño específico._

_1. zita, y Wn, el LGR tiene que pasar por el polo Pd._

_2. zita y nuúmero de ciclos en la respuesta escalón, el LGR tiene que pasar por el polo Pd._

_3. ts y Mp, se debe poder rediseñar hasta que la respuesta escalón satisfaga los criterios._

_4. td y zita, se debe rediseñar hasta que la respuesta al escalón satisfaga ts. _

_5. ts y número de ciclos en la respuesta escalón, se debe rediseñar hasta que la respuesta al escalón satisfaga ts._

_6. número de ciclos en la respuesta escalosn y Mp, se debe rediseñar hasta que la respuesta al escalón satisfaga Mp_

_En caso de que la pareja de datos no sea suficiente para poder desarrollar el diseño, se le informa al usuario. También existe la opción de seleccionar el tipo de controlador a diseñar de un menú de diseños posibles, diferenciando controladores que aportan ángulos positivos y negativos para la respectiva planta, de manera adicional el progrma retorna la función de transferencia del controlador digital C(z), y puede representar la respuesta escalón del sistema en lazo cerrado, igualmente se puede dibujar el LGR, la respuesta rampa y parabola._

_La opción de seleccionar si se tiene encuaneta condiciones de error de estado estacionario va ligado a la pareja seleccionada, de la siguiente manera._

_1. sin condición de error de estado estacionario_

_2. ep constante_

_3. ep=0_

_4. ep=0 y ev constante_

_5. ev=0_

_6. ev=0 y ea constante_

_7. ea=0_



_Acontinuación se presenta una pequeña demo_

## Ejecutando las pruebas ⚙️

_Los problemas que se utilizan acontinuación se sacarón del libro Sistemas de control en tiempo discreto del Ogata, problemas B-4-9._

_Ejemplo: Refiriéndonos al sistema de control digital mostrado en la figura 4-67, diseñe un controlador digital G„(z) tal que el factor de amortiguamiento relativo zita de los polos dominantes en lazo cerrado sea 0.5 y el número de muestras por ciclo de la oscilación senoidal amortiguada sea 8. Suponga que el período de muestreo es de 0.1 seg es decir T= 0.1. Determine la constante de error de velocidad estática. También, determine la respuesta del sistema diseñado a una entrada escalón unitario._


![image](https://user-images.githubusercontent.com/45041472/52540191-dd9bf880-2d54-11e9-904d-1d26fa1f478a.png)



_En primer luagr se abre el archivo control2.m y se ingresa la planta, la cual se puede ver en la imagen anterior._

![ejemplo1](https://user-images.githubusercontent.com/45041472/52540155-65cdce00-2d54-11e9-837a-fda971ad42c7.jpg)

_En en la imagen se puede apreciar ciertos pasos que son necesarios seguir, en primer lugar se ingresa la fucnión de trasferencia en el recuadro y se oprime enter, inmediatamente se puede ver la representación de la planta en tiempo conitinuo y discreto, de manera opcional se puede ingresar el tiempo de muestreo de manera manual, en caso contrario al presionar enter el programa calcula el periodo de muestreo automaticamente, los siguientes pasos no son necesarios (4,5), los cuales sirven para graficar la respuesta de la planta, al pasar el paso 6 se puede pasaral diseño de la planata, imagen que se muestra acontinuación._


### Analice las pruebas end-to-end 🔩

_Explica que verifican estas pruebas y por qué_

```
Da un ejemplo
```

### Y las pruebas de estilo de codificación ⌨️

_Explica que verifican estas pruebas y por qué_

```
Da un ejemplo
```

## Deployment 📦

_Agrega notas adicionales sobre como hacer deploy_

## Construido con 🛠️

_Menciona las herramientas que utilizaste para crear tu proyecto_

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - El framework web usado
* [Maven](https://maven.apache.org/) - Manejador de dependencias
* [ROME](https://rometools.github.io/rome/) - Usado para generar RSS

## Contribuyendo 🖇️

Por favor lee el [CONTRIBUTING.md](https://gist.github.com/villanuevand/xxxxxx) para detalles de nuestro código de conducta, y el proceso para enviarnos pull requests.

## Versionado 📌

Usamos [SemVer](http://semver.org/) para el versionado. Para todas las versiones disponibles, mira los [tags en este repositorio](https://github.com/tu/proyecto/tags).

## Autores ✒️

_Menciona a todos aquellos que ayudaron a levantar el proyecto desde sus inicios_

* **Andrés Villanueva** - *Trabajo Inicial* - [villanuevand](https://github.com/villanuevand)
* **Fulanito Detal** - *Documentación* - [fulanitodetal](#fulanito-de-tal)

También puedes mirar la lista de todos los [contribuyentes](https://github.com/your/project/contributors) quíenes han participado en este proyecto. 

## Licencia 📄

Este proyecto está bajo la Licencia (Tu Licencia) - mira el archivo [LICENSE.md](LICENSE.md) para detalles

## Expresiones de Gratitud 🎁

* Comenta a otros sobre este proyecto 📢
* Invita una cerveza 🍺 a alguien del equipo. 
* Da las gracias públicamente 🤓.
* etc.



---
Especial agradecimiento a  [Villanuevand](https://github.com/Villanuevand) por compartir la plantilla
