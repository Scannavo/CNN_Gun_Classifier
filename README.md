# CNN_Gun_Classifier
Este repositorio contiene el proyecto de de R-CNN donde detectamos la aparición de armas de fuego en la imagen 

# 1 Descargamos los archivos actuales

Descarguen/Clonen el proyecto actual y tengan todos sus archivos,  donde tendremos la carpeta que contiene a todos estos archivos que se llama "RCNN_Gun" al final tenemos estos 3 archivos dentro...

<p align="center">
  <img src="https://user-images.githubusercontent.com/94633259/150459319-3962a87a-60f1-479f-ae95-96688a0a7201.png" />
  <img src="https://user-images.githubusercontent.com/94633259/150457131-9755314b-37c7-48da-9a35-46b2742653e2.png" />
</p>

# 2 Descargar el R_CNN_coco

En el siguiente link podemos descargar esa mascara, importante para el proyecto: 
https://github.com/matterport/Mask_RCNN/releases/download/v2.0/mask_rcnn_coco.h5

y luego lo agregamos a la carpeta del proyecto, de la siguiente forma...

<p align="center">
  <img src="https://user-images.githubusercontent.com/94633259/150457464-78682350-ca14-4b74-b9b0-b972f65b806a.png" />
</p>

# 3 Subir a google drive

Una vez tenemos ya la carpeta con los archivos necesarios, subimos la carpeta del proyecto al google drive, para poder trabajar con google colab, entonces damos a nuevo y subimos la carpeta...

<p align="center">
  <img src="https://user-images.githubusercontent.com/94633259/150457913-fd3b67e7-372a-411f-b70d-f563d4e17a58.png" />
</p>


# 4 Entorno del proyecto (Google colab)

Una vez hayamos cargado el proyecto a google drive, iremos a file, abriremos un notebook, y buscaremos el archivo que se llama RCNN.ipynb y lo abriremos ahi

<p align="center">
  <img src="https://user-images.githubusercontent.com/94633259/150467288-f24dd9cf-ed2b-4e51-b9e4-336a5c36ab68.png" />
</p>

## Mejorar el rendimiento en caso de que vaya muy lento el entrenamiento

Aqui cambiamos el "Hardware accelerator por GPU, solo en caso de que vaya lento

<p align="center">
  <img src="https://user-images.githubusercontent.com/94633259/150458713-a1393458-50e4-407c-a900-b744b0f22156.png" />
</p>

# 5 Ejecutar el codigo (Google colab)

Ahora simplemente es ejecutar los bloques del codigo del programa, todos los bloques sin excepción, ya las demas anotaciones estan en el mismo colab



# Puntos a considerar
##  Anotación de imagenes

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


## Sistemas de archivos

Ahora que tenemos las anotaciones vamos a crear nuestra sistemas de archivos del Dataset, el cual esta conformado por una carpeta madre llamada Dataset, con dos carpetas dentro, que las llamaremos val y train, que a la vez tendras imagenes y sus respectivos .json, es importante recalcar que las imagenes son diferentes en las dos carpetas, un 80% en train y 20% en el de val

- Dataset
  - val
    - image_val.jpg
    - gun_region_json.jpg
  - train
    - image_train.jpg
    - gun_region_json.jpg


## Carpeta prueba dentro de Dataset

Esta carpeta sirve para poner imagenes fuera de las que hemos usado para el entrenamiento y validación, donde pondremos nuevas imagenes y las probaremos con la segunda parte del codigo

# Posibles errores 

## No encuentra el directorio

Esto puede suceder porque no se copia adecuadamente la ruta de los archivos en el codigo, para eso realizamos los siguientes paso siempre y cuando hayas agregado el proyecto a drive, y haz corrido el codigo del principio que importa drive a google colab

- 1: Primero ubicamos todas esas rutas que pueden haber cambiado, porque pueden ser diferentes para todos
- 2: A la en google colab encontramos un icono de carpeta y le damos "click"
- 3: Luego se abrira un espacio, donde tendremos uns carpetas y entramos a esa que dice drive, y luego buscamos dentro nuestro proyecto "RCNN_GUN" o el nombre con lo que lo guardaron
- 4: Luego nos ubicamos al pasar el cursor por la carpeta encontramos 3 puntos, le damos click
- 5: Y luego nos sale una lista de opciones y presionamos el que dice "Copy path" y ya podriamos cambiar nuestra dirección

<p align="center">
  <img src="https://user-images.githubusercontent.com/94633259/150557136-08ca5494-dd4b-4d12-bcb5-8651de37ea99.png" />
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/94633259/150557919-751249be-8e57-4755-b360-8212c71e920d.png" />
</p>






## No encuentra el directorio logs/XXXXXXXXXX/xxxx.h5

Cuando ejecutamos la primera parte de todo el libro del codigo, esto crea una carpeta que se llama "logs", en esta carpeta al navegar a la ultima subcarpeta nos encontramos con un archivo que es formato .h5, se copia la ruta de este archivo a donde lo necesite, usualmente aparecen mas de uno, habitualmente se usa el ultimo o el que mejor resultados de en lo que llamamos "loss"

<p align="center">
  <img src="https://user-images.githubusercontent.com/94633259/150553963-76726f35-858b-454a-9e35-d86b98ec26dd.png" />
</p>



