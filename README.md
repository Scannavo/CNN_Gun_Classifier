# CNN_Gun_Classifier
Este repositorio contiene el proyecto de de R-CNN donde detectamos la aparición de armas de fuego en la imagen 

# 1 Descargamos los archivos actuales

Descarguen/Clonen el proyecto actual y tengan todos sus archivos, al final tenemos estos 3 archivos...

<p align="center">
  <img src="https://user-images.githubusercontent.com/94633259/150457131-9755314b-37c7-48da-9a35-46b2742653e2.png" />
</p>

# 2 Descargar el R_CNN_coco

En el siguiente link podemos descargar esa mascara, importante para el proyecto: 
https://github.com/matterport/Mask_RCNN/releases/download/v2.0/mask_rcnn_coco.h5

y luego lo agregamos a la carpeta del proyecto, de la siguiente forma...

<p align="center">
  <img src="https://user-images.githubusercontent.com/94633259/150457464-78682350-ca14-4b74-b9b0-b972f65b806a.png" />
</p>

# 2 Anotación de imagenes

Para empezar, necesitamos anotar nuestras propias imagenes para el proyecto, para eso visitaremos la pagina web https://www.robots.ox.ac.uk/~vgg/software/via/ y bajamos entramos en el siguiente apartado, el cual es una pagina web y asi no tendremos que instalar extras...

<p align="center">
  <img src="https://user-images.githubusercontent.com/94633259/150449962-ab819e98-8abd-45d1-88d2-0c83bedac520.png" />
</p>

Una vez que entramos cargamos las imagenes a la pagina, se pueden seleccionar mas de una...

<p align="center">
  <img src="https://user-images.githubusercontent.com/94633259/150450400-6abff292-9411-42b0-9cb1-95579d217cd1.png" />
</p>

Una vez tengamos las imagenes cargadas, lo siguiente es modificar el algunas opciones...

- 1: En la parte del "Region Shape" le damos click a la al icono señalizado, el cual es la de poligonos, necesario para poder usar el codigo que se ha dado
- 2: Aqui podemos cambiar el nombre del .json
- 3: Aqui expandimos las opciones de atributos
- 4: Damos nombre al atributo, que en este caso es "Gun"
- 5: Agregamos el atributo
- 6: Aqui cambiamos el default que es text por checkbox
- 7: Y terminamos con dandole un ID al atributo, que tambien le dimos el nombre de "Gun"
 
 <p align="center">
  <img src="https://user-images.githubusercontent.com/94633259/150450686-e0d26696-32d9-4275-9ce0-f499d05cf751.png" />
</p>

Una vez tengamos todo eso, empezamos a darle click en la region que queremos detectar,cuando ya tengamos la forma que queremos damos enter y presionamos escape, para luego presionar la forma y poder seleccionar nuestro ID, el cual se llama "Gun"

<p align="center">
  <img src="https://user-images.githubusercontent.com/94633259/150451302-dd0a1688-e65f-415e-817b-f3254690d518.png" />
  <img src="https://user-images.githubusercontent.com/94633259/150451516-1d0a5e65-f8cb-475d-aed9-feaa477f7ec2.png" />
</p>

Una vez tengamos anotada todas nuestras imagenes procederemos a descargar el .json, para eso realizamos los siguientes pasos...

<p align="center">
  <img src="https://user-images.githubusercontent.com/94633259/150453348-1d747c5a-69cc-4769-b0b5-4dedb7eaa694.png" />
</p>


# 2 Sistemas de archivos

Ahora que tenemos las anotaciones vamos a crear nuestra sistemas de archivos del Dataset, el cual esta conformado por una carpeta madre llamada Dataset, con dos carpetas dentro, que las llamaremos val y train, que a la vez tendras imagenes y sus respectivos .json, es importante recalcar que las imagenes son diferentes en las dos carpetas, un 80% en train y 20% en el de val

- Dataset
  - val
    - image_val.jpg
    - gun_region_json.jpg
  - train
    - image_train.jpg
    - gun_region_json.jpg

# 3 Subir a google drive
# 4 Entorno del proyecto (Google colab)

