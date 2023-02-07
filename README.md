# Sistema de corte para dispenser de agua
En este repositorio se encuentran los códigos fuentes para la implementación del Proyecto Final de la materia Sistemas Embebidos (86.65) de la Facultad de Ingeniería de la Universidad de Buenos Aires.

El Trabajo se basa en un Sistema de corte para dispenser de agua el cual tiene como objetivo cortar el suministro de agua de un dispenser al momento en el que se detecta que una botella está por llenarse. Para la implementación del mismo se utilizó un servo MG996R el cual debe girar bajando la llave del dispenser ocasionando el abandono del llenado de la botella al momento en el que el sensor de líquido sin contacto XKC-Y25 de tipo PNP detecta que la botella está por llenarse. Finalmente, para la ejecución del código se utilizó el entorno de desarrollo Keil Studio seleccionando como dispositivo a utilizar la placa NUCLEO-F429ZI.

## Descripción e información de hardware

El hardware del Sistema de corte para dispenser de agua está compuesto por una placa NUCLEO-F429ZI de ARM, un sensor de líquido sin contacto XKC-Y25 capacitivo de tipo PNP y un servo MG996R. En la siguiente figura puede observarse un diagrama en bloques de los componentes utilizados en la implementación del sistema, señalando la fuente de alimentación utilizada y el tipo de conexión entre los mismos.  

<p align="center">
  <img width="403" alt="image" src="https://user-images.githubusercontent.com/65862114/217090340-3a16b1d1-0f30-498b-af24-0b98b688a401.png">
</p>



## Diagrama de conexión entre los componentes

Como se mencionó anteriormente el sensor XKC-Y25 tiene la función de detectar cuando una botella está por llenarse. Para esto es conectado a GND mediante el cable azul, al pin D2 de la placa NUCLEO-F429ZI a través del cable amarillo y es alimentado con 3,3 V mediante el cable marrón conectado a un cable verde. Por otro lado, la placa es alimentada con 5 V mediante un cable USB (Type A to Type micro B) y el servo es conectado al pin A0 de la misma mediante un cable naranja para recibir la señal PWM que esta le envía con el objetivo de que este gire y baje la llave del dispenser cortando el suministro de agua. Además es alimentado con 5V mediante un cable rojo y conectado a GND a través de un cable marrón. En la siguiente figura pueden observarse las diferentes conexiones de todos los elementos que componen al hardware del Sistema de corte para dispenser de agua.

<p align="center">
  <img width="400" alt="image" src="https://user-images.githubusercontent.com/65862114/217092679-9faee39d-7d84-49d2-abe0-6d30979ec561.png">
</p>

## Diagrama esquemático de las conexiones del hardware

En la siguiente figura se muestra un diagrama esquemático correspondiente a las conexiones del hardware utilizado en la implementación del Sistema de corte para dispenser de agua.

<p align="center">
 <img width="410" alt="image" src="https://user-images.githubusercontent.com/65862114/217094376-d8ab6c77-f848-434c-8be9-524122f34347.png">
</p>

## Lógica del funcionamiento del Sistema de corte para dispenser de agua

En la siguiente figura se presenta un diagrama de flujo que describe la lógica del funcionamiento del sistema.

<p align="center">
<img width="150" alt="image" src="https://user-images.githubusercontent.com/65862114/217140136-ed6cdeb1-bbd3-48a1-9fe7-ecb0f07fe4b4.png">
</p>

## Memoria del Trabajo Final del Seminario de Sistemas Embebidos 

En la [Memoria del Trabajo Final del Seminario de Sistemas Embebidos](https://docs.google.com/document/d/1Y6TgAkQxlL4LgHQijRuMg-C99RTl2MLM4XvG4BzEanc/edit#heading=h.8jk5181xq5jw) puede encontrarse mas información acerca del trabajo realizado. 

## Estructura del repositorio
El [repositorio](https://github.com/mpazcurti/Sistema-de-corte-para-dispenser-de-agua) se organiza de la siguiente manera:


── Sistema-de-corte-para-dispenser-de-agua  
│   ├── .gitignore  
│   ├── README.md  
│   ├── arm_book_lib.h  
│   ├── main.cpp  
│   └── mbed-os.lib  

Se tiene el archivo main.cpp en donde se encuentra el programa principal del sistema, el README.md el cual es el presente archivo contenedor de la información acerca del proyecto y los archivos necesarios para la configuración de Mbed OS.















