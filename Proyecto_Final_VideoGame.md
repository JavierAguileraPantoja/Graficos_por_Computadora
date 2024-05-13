## Proyecto Final Gráficos por Computadora



### Lo primero que aremos

Descargar imágenes y quitarles el fondo para prepararlas así como mi fondo gif prepararlo en imágenes para que aparezca en el entorno buscando musica para el escenario y la colisión de la bola con los caramelos. ya descargadas la preparación a los dulces les quietaremos el fondo a los gif que usaremos de fondo los prepararemos.

![image-20240511182854565](C:\Users\javie\AppData\Roaming\Typora\typora-user-images\image-20240511182854565.png)

En la imagen mostramos que nos encontramos en la carpeta Proyecto_Final y dentro de ella esta nuestro documento escrito que es este mismo. Nuestro programa Pero señala que estamos en la carpeta img que es donde se encuentran todas las imágenes preparadas para el video juego pygame, como podemos ver tenemos dos carpetas una fondo y otra multimedia original así y tal como fue descargado antes de su preparación y aun mas videos, fotos y musica.  En la carpeta fondo solo esta nuestro gif que usamos como fondo y en un futuro el equipo decidirá cambiar los gráficos por otros al gusto de la popularidad.  Al preparar las imágenes solo se les quito el fondo para que los dulces salieran solos por completo. 





### Continuamos con la construcción de la ventana y más.

#### Aquí sus bibliotecas

Que las conocemos y son fáciles de visualizar

![image-20240511183727797](C:\Users\javie\AppData\Roaming\Typora\typora-user-images\image-20240511183727797.png)

```
import pygame 
import random 
import time
from random import choice, randrange
from random import randint
```



#### Aquí la inicialización de pygame 

Donde le damos el ancho y largo de su tamaño esto porque las laptop mas pequeñas este era el tamaño adecuado para ellas y las demás podían usarlo con facilidad. Fig(1)

![image-20240511183900228](C:\Users\javie\Documents\Buzo\UG\clases\Graficas por computadora\Proyecto_Final\image-20240511183900228.png)

​											Fig(1)

```
pygame.init()
alto=625
ancho=750
fon=(ancho,alto)
entorno=pygame.display.set_mode((ancho,alto))
pygame.display.set_caption('Ping boll Proyecto Final')
bandera=True
```

También le damos un titulo al juego que aparecerá en la ventana dando la bariable que utillizremos para el cierre del circulo while donde se ejecutara todo lo que suceda en nuestra ventana. Fig(1).

#### Aquí mostramos la creación del fondo

Ya que el gif se partió en 24 imágenes entonces ellas fueron mandadas llamar donnde se contrullo un arreglo para almacenarlas y facilitar su mandato a llamar. Fig(2).

![image-20240511184410169](C:\Users\javie\AppData\Roaming\Typora\typora-user-images\image-20240511184410169.png)

​											Fig(2)

```
#----------------------------------------------------------------------
#aqui metemos todas las imagenes que usaremos como sonidos y de mas
#Aqui es el fondo en movimiento
fondo1=pygame.image.load("img\\fondo\\frame-01.gif")
fondo2=pygame.image.load("img\\fondo\\frame-02.gif")
fondo3=pygame.image.load("img\\fondo\\frame-03.gif")
fondo4=pygame.image.load("img\\fondo\\frame-04.gif")
fondo5=pygame.image.load("img\\fondo\\frame-05.gif")
fondo6=pygame.image.load("img\\fondo\\frame-06.gif")
fondo7=pygame.image.load("img\\fondo\\frame-07.gif")
fondo8=pygame.image.load("img\\fondo\\frame-08.gif")
fondo9=pygame.image.load("img\\fondo\\frame-09.gif")
fondo10=pygame.image.load("img\\fondo\\frame-10.gif")
fondo11=pygame.image.load("img\\fondo\\frame-11.gif")
fondo12=pygame.image.load("img\\fondo\\frame-12.gif")
fondo13=pygame.image.load("img\\fondo\\frame-13.gif")
fondo14=pygame.image.load("img\\fondo\\frame-14.gif")
fondo15=pygame.image.load("img\\fondo\\frame-15.gif")
fondo16=pygame.image.load("img\\fondo\\frame-16.gif")
fondo17=pygame.image.load("img\\fondo\\frame-17.gif")
fondo18=pygame.image.load("img\\fondo\\frame-18.gif")
fondo19=pygame.image.load("img\\fondo\\frame-19.gif")
fondo20=pygame.image.load("img\\fondo\\frame-20.gif")
fondo21=pygame.image.load("img\\fondo\\frame-21.gif")
fondo22=pygame.image.load("img\\fondo\\frame-22.gif")
fondo23=pygame.image.load("img\\fondo\\frame-23.gif")
fondo24=pygame.image.load("img\\fondo\\frame-24.gif")
imagenes=[fondo1,fondo2,fondo3,fondo4,fondo5,fondo6,fondo7,fondo8,fondo9,fondo10,fondo11,fondo12,fondo13,fondo14,fondo15,fondo16,fondo17,fondo18,fondo19,fondo20,fondo21,fondo22,fondo23,fondo24]
```

En esta otra imagen dentro de nuestro principal ciclo donde se mostraran todas las imágenes de la ventana, aparece un ciclo fondo es donde se estarán mostrando las 24 imágenes sin parar el fondo sera la imagen en el momento con el tamaño que nuestro fondo alcanza. Las otras funciones hablaremos después.  Fig(3).

![image-20240511184612165](C:\Users\javie\AppData\Roaming\Typora\typora-user-images\image-20240511184612165.png)

​											Fig(3)

```
#------------------------------------El while en el mero climas la funcion de proyeccion en la pantalla----------------------------
    
while bandera:
  sonidofondo.play()  
  for evento in pygame.event.get():
  
    if(evento.type==pygame.QUIT):
      bandera=False
      
  #dibujar fondo
  if(a>=24):
    a=0
  fondo=pygame.transform.scale(imagenes[a],(fon))
  a+=1
  entorno.blit(fondo,(0,0))
  
  jugador.dibujar(entorno)
  bola1.dibujar(entorno)
  dulce.dibujar(entorno)
  bola1.movimiento()
```



#### Atracción de imágenes y más.

En esta otra imagen la llamada bases es la imagen que usaremos para le poste que estará rebotando la bola contra los caramelos. Fuente la letra que utilizaremos para el score y las vidas. Los sonidos que usaremos en toda la ejecución del juego sonidofondo  y el sonido de las colisiones. El sonidoroto es cuando la pelota choque contra nuestro objetivo con algún caramelo. Como también aparece toda importación de las imágenes a utilizar y nuestra pelota en la Fig(4), todas estas instrucciones solo son para mandar a llamar a las imágenes que estaremos utilizando.



![image-20240511185156335](C:\Users\javie\AppData\Roaming\Typora\typora-user-images\image-20240511185156335.png)

​											Fig(4)

```
#importaciones de las naves buenas y la pelota
#Dulces
dulce_rojo=pygame.image.load("img\\dulce_rojo.png")
dulce_verde=pygame.image.load("img\\dulce _verde.png")
dulce_menta=pygame.image.load("img\\dulce_azul.png")
dulce_baston=pygame.image.load("img\\dulce_baston.png")
dulce_mono=pygame.image.load("img\\dulce_mono.png")
#Pelota numero uno
pelota=pygame.image.load("img\\bola.png")
```



#### Adaptación del tamaño de imágenes.

Es este fragmento de código lo unico que hacemos es que a cada imagen mandada llamar le damos una transformación y adaptación para el tamaño al que queremos que aparezca con la función pygame.transform.scale() y solo le estamos diciendo que la imagen tal la queremos a cierto tamaño. Fig(5).

![image-20240511190528141](C:\Users\javie\AppData\Roaming\Typora\typora-user-images\image-20240511190528141.png)

​											Fig(5).

```
#Acomodamos sus tamños de los dulces y bola y la base
bola=pygame.transform.scale(pelota,(70,70))
dr=pygame.transform.scale(dulce_rojo,(70,70))
dm=pygame.transform.scale(dulce_menta,(70,70))
dv=pygame.transform.scale(dulce_verde,(70,70))
db=pygame.transform.scale(dulce_baston,(70,70))
dmo=pygame.transform.scale(dulce_mono,(70,70))
base=pygame.transform.scale(bases,(200,50))
```

#### Creación de Clases y sus Funciones

Aquí creamos una clase objetos que será como nuestra clase padre donde le daremos atributos de su posicionamiento en la ventana y de salud utilizada para los dulces y para nuestra vida como también será dibujado la imagen. Por el momento también construimos la clase jugador heredera de objetos donde crearemos la barra para el rebote de la pelota. Fig(6)



![image-20240513114735631](C:\Users\javie\AppData\Roaming\Typora\typora-user-images\image-20240513114735631.png)

​												Fig(6)

```
class objetos:
  def __init__(self,x,y,salud=100):
    self.x=x
    self.y=y
    self.salud=salud
    self.image=None
  def dibujar(self,entorno):
    entorno.blit(self.image,(self.x,self.y))
  

class Jugador(objetos):
  def __init__(self,x,y,salud=100):
    super().__init__(x,y,salud)
    self.image=base
```

Poco después se creo la clase bola heredera de objetos con la intención de crear  heredando posición e imagen dándole variables globales porque son las que cambiaremos por positivas o negativas para crear el efecto del rebota en el entorno de la venta para esto se crearon los if´s Fig(7).

![image-20240513115247751](C:\Users\javie\AppData\Roaming\Typora\typora-user-images\image-20240513115247751.png)

​											Fig(7).

Estamos trabajando en la creación de los dulces 
