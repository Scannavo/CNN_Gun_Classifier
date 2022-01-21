# CNN_Gun_Classifier
Este repositorio contiene el proyecto de de R-CNN donde detectamos la aparición de armas de fuego en la imagen 

# 1 Anotación de imagenes

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




# 2 Sistemas de archivos
# 3 Subir a google drive
# 4 Entorno del proyecto (Google colab)
