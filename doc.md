# **SISTEMA DE GESTIÓN**
# [PASTELERÍA](http://45.236.129.94:8083/admin/) <hr>
> ## Generalidades
Tras acceder al login con todas las sucursales

![alt text](https://raw.githubusercontent.com/rinobits/images/master/loginInterfaz.png "login")

veremos el Dashboard en el cual se despliega la información de los pedidos en todas las comunas, de la siguiente forma: 

![alt text](https://raw.githubusercontent.com/rinobits/images/master/preview.png "menu comunas")

Si nos fijamos, en el menú superior izquierdo podemos alternar entre las comunas.   
También tenemos un acceso rápido al dashboard, a la cuenta del usuario y a configuraciones.   
Tanto el menú como los botones se encuentran inactivos, pues no producen respuesta.

![alt text](https://raw.githubusercontent.com/rinobits/images/master/sucursales.gif "sucursales")

Justo debajo del menú, tenemos botones para alternar las fechas, lo que hará que varíe la información   
mostrada en función de la fecha seleccionada. Este controlador lo veremos en varias páginas del sistema.

![alt text](https://raw.githubusercontent.com/rinobits/images/master/fecha.png "fechas")

Mientras que en el menú izquierdo podremos ver las siguientes opciones, que mostraremos rápidamente en el siguiente vídeo y que serán descritas más abajo en este mismo documento.

[![Watch the video](https://raw.githubusercontent.com/rinobits/images/master/preview2.png)](https://youtu.be/ZLitlazA4NA)<hr>

> # Funcionalidades
* ### Oficina<br>

* #### PROGRAMACIÓN DIARIA

  **MÉTODO**  | **PARA**
  ------------ | -------------
  GET          | Obtener pedidos   <br>
  <hr>

   - Como se observa en la captura de abajo, hay cuatro columnas, cada una de ellas con información que será traída desde el servidor: 
     1) Necesitamos obtener los pedidos
     2) Su nombre, 
     3) cuántas veces se repite por tamaño, y
     4) cuántas lo hace en cada columna proceso. 

![alt text](https://raw.githubusercontent.com/rinobits/images/master/2.png "programación diaria")

  * #### PEDIDOS ESPECIALES<br>
  

    **MÉTODO**  | **PARA**
    ------------ | -------------
    GET          | Obtener pedidos   <br>
    GET          | Get by ID          <br>
    
    <hr>

      - Aquí tenemos un fomulario para realizar un pedido, mostrarlo, imprimirlo, así como también hay una tabla en donde los pedidos serán organizados por su tamaño.   
      - En el panel izquierdo se mostrarán los pedidos, al hacer click se mostrarán los resultados en el formulario para, al parecer, poder imprimirlos.
      - Esta página no realiza nada más, sólo muestra información.
  
![alt text](https://raw.githubusercontent.com/rinobits/images/master/3.png "menu comunas")



  * #### Masas especiales<br>
    **MÉTODO**  | **PARA**
    ------------ | -------------
    GET          | Obtener pedidos   <br>
    <hr>
  
    - Nos encontramos con una página que muestra información sobre la cantidad de masas elaboradas v/s la cantidad de pedidos realizaods.

![alt text](https://raw.githubusercontent.com/rinobits/images/master/4.png "masas especiales")



* ### Precios
  * #### Tortas<br>
  **MÉTODO**  | **PARA**
  ------------ | -------------
  GET          | Obtener pedidos   <br>
  GET          | Get by ID          <br>
  POST         | Registrar pedido  <br>
  PUT          | Editar un pedido <br>
  <hr>

  - Realización del pedido. Elección de torta y tamaño.    
  - Seleccion de costo v/s venta con y sin IVA.    
  - Seguramente los pedidos que se van realizando van  apareciendo debajo en función del tiempo.    

![alt text](https://raw.githubusercontent.com/rinobits/images/master/5.png "tortas")



  * #### Productos<br>
    **MÉTODO**  | **PARA**
    ------------ | -------------
    GET          | Obtener pedidos   <br>
    GET          | Get by ID          <br>
    POST         | Registrar pedido  <br>
    PUT          | Editar un pedido <br>
    <hr>
    - Lo mismo que en el caso de las tortas.
  
![alt text](https://raw.githubusercontent.com/rinobits/images/master/6.png "productos")
* ### Cámara
  * #### Programación<br>
    **MÉTODO**  | **PARA**
    ------------ | -------------
    GET          | Obtener pedidos   <br>
    <hr>
  
    - Es similar a la tabla de programación diara, conservándose la misma primera columna con el tipo de torta, manteniendo la segmentación por tamaño en las columnas subsecuentes.
    Pero ahora los procesos son:
        1) Programación
        2) Recepción
        3) En camino y
        4) Retirado
    - Podría haber un método post porque hay un botń de registro, pero como no hay formulario visible no lo colocaremos aquí, porque si no es un formulario emergente, probablemente dirigirá a otra sección dentro del sistema.
    
![alt text](https://raw.githubusercontent.com/rinobits/images/master/7.png "programación")<hr><hr>
#### Este botón se repetirá varias veces a continuación, seguramente es para desplegar un formulario o para dirigirnos a otro lugar dentro del sistema.
![alt text](https://raw.githubusercontent.com/rinobits/images/master/Selection_012.png "cuadricula")<hr><hr>
  * #### Recepción<br>
    **MÉTODO**  | **PARA**
    ------------ | -------------
    GET          | Obtener pedidos   <br>
    <hr>
  
    - Formulario vacío, ha de mostrar los pedidos concretados, es decir, los que han sido entregados satisfactoriamente al cliente.
    - Se aplica lo mismo que en el caso de arriba para el POST.
        
![alt text](https://raw.githubusercontent.com/rinobits/images/master/8.png "recepción")

- **Tenemos también un botón circular que tiene dos estados, los cuales podrían**

![alt text](https://raw.githubusercontent.com/rinobits/images/master/redbutton.png "programación diaria")

![alt text](https://raw.githubusercontent.com/rinobits/images/master/greenbutton.png "programación diaria")

  1) Determinar el estado de un proceso o una acción dentro del sistema. El botón queda en verde cuando se le da al botón de **Comenzar**.
  2) El botón se verá en más páginas, en rojo por defecto, cambiando a verde si se presiona y a rojo nuevamente si se presiona cualquier parte diferene del botón mismo.

* ### Fábrica
  * #### Recepción fábrica<br>
    **MÉTODO**  | **PARA**
    ------------ | -------------
    GET          | Obtener pedidos   <br>
    GET          | Get by ID          <br>
    POST         | Crear pedidos<br>
    <hr>
  
    - Es similar a la tabla de programación diara, conservándose la misma primera columna con el tipo de torta, manteniendo la segmentación por tamaño en las columnas subsecuentes.
    Pero ahora los procesos son:
        1) Programación
        2) Recepción
        3) En camino y
        4) Retirado
    - Se aplica lo mismo que en el caso de arriba para el POST. Pero lo pondremos guiados por la suposición de que desde aquí se pueden enviar pedidos en masa para la fábrica, especificando a posteriori sus características.
        
![alt text](https://raw.githubusercontent.com/rinobits/images/master/9.png "recepción fábrica")
  * #### Salida Fábrica<br>
    **MÉTODO**  | **PARA**
    ------------ | -------------
    GET          | Obtener pedidos   <br>
    <hr>
  
    - Claramente, los pedidos que han salido de la fábrica. Desconozco el motivo de la duplicación de "Torta", quizá una es para tortas especiales y la otra para convencionales. O talvez una es para tortas "Diet" (ver menu: precios -> tortas).
    - Se aplica la misma incertidumbre para el POST que en los casos precedentes.
  
![alt text](https://raw.githubusercontent.com/rinobits/images/master/10.png "Recepción")
  * #### Revisión Camioneta
    - Página completamente en blanco. Quizás estemos en presencia de una página que mostrará los pedidos que están _en camino_ y su estado.
  

![alt text](https://raw.githubusercontent.com/rinobits/images/master/11.png "revisión camioneta")
  * #### Caja<br>
    **MÉTODO**  | **PARA**
    ------------ | -------------
    GET          | Obtener pedidos   <br>
    PUT          | Bloquear un pedido <br>
    <hr>

    - Supondremos que cada caja contiene **X** cantidad de pedidos, quizá al presionar uno de los campos se pretendía que se mostrase el contenido de cada caja. 
    - El candado ha de determinar si un pedido está en proceso de elaboración (bloqueado) o en proceso de despacho o entregado (desbloqueado). O también podría ser a la inversa.
    - El candado también podría ser una opción para bloquear el envío o la entrega de una caja, por cualquier razón.

![alt text](https://raw.githubusercontent.com/rinobits/images/master/12.png "caja")
* ### Local:
  * #### Pedido especial<br>
    **MÉTODO**  | **PARA**
    ------------ | -------------
    GET          | Obtener pedidos   <br>
    GET          | Get by ID          <br>
    PUT          | Editar un pedido <br>
    POST         | Crear pedido <br>
    <hr>
    
    - Desde aquí podemos listar, registrar y editar pedidos. 
    - Podrían reducirse 4 formularios a éste, realizando algunas añadiduras.

![alt text](https://raw.githubusercontent.com/rinobits/images/master/13.png "Pedido especial")
  * #### Sobrantes<br>
    **MÉTODO**  | **PARA**
    ------------ | -------------
    GET          | Obtener pedidos   <br>
    <hr>
  
    - Aparentemente una lista de excedentes, quizá marcando pedidos cancelados, mal registrados, que no pasaron el control de calidad, etcétera.


![alt text](https://raw.githubusercontent.com/rinobits/images/master/14.png "sobrantes")
  * #### Mensajes<br>
    **MÉTODO**  | **PARA**
    ------------ | -------------
    GET          | Obtener mensajes   <br>
    GET          | Get by ID          <br>
    PUT          | Editar un mensaje <br>
    <hr>

    - Se añaden los mensajes para los pedidos.
    - Asumiremos un get by id pensando en que se mostrarán los pedidos en el panel izquierdo y podremos seleccionarlos para mostrar el mensaje a la derecha y editarlo. 

![alt text](https://raw.githubusercontent.com/rinobits/images/master/15.png "mensajes")
* ### Reportes:
  * #### Dashboard <br>
    **MÉTODO**  | **PARA**
    ------------ | -------------
    GET          | Obtener pedidos   <br>
    <hr>
    - Obtenemos la información de todas las sucursales, estructurada de a forma que se muestra en la imagen.

![alt text](https://raw.githubusercontent.com/rinobits/images/master/1.png "dashboard")

> # Errores

#### **Login**

A continuación podemos apreciar un cierre en al ventana del login al hacer click en cualquier lugar de la ventana.

![alt text](https://raw.githubusercontent.com/rinobits/images/master/login.gif "Cierre de ventana al hacer click")

Esto nos devuelve la interfaz de pedidos pero en blanco, sin información, pues no se ha realizado la autenticación. 

![alt text](https://raw.githubusercontent.com/rinobits/images/master/noauth.png "Lo que verás sin acceso")

<style>
img{
    max-width:500px;
    margin-left:0px;
}
body{background-color:rgba(20,2,30)}
p {margin-left:40px}
.some{
    color:black !important;
}
h3{
    text-decoration:underline;
}
</style>
