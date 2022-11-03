# binanen
Libreria binanen
En primer lugar, necesitas sacar tus api keys, la cual se obtiene en este link: https://opendata.aemet.es/centrodedescargas/altaUsuario

Una vez obtienas solo necesitaras descargar nuestra libreria y usar tus api keys.

En cuanto a código, dentro del “init”, es donde se exportan los datos haciendo las consultas necesarias a la API de Aemet. Lo único necesario es tener las api keys para utilizarla. Además, dentro del “init” también pasamos los datos desde “Json” a un “Dataframe” para que sea más cómodo trabajar con ellos. Después hemos creado otra función dentro de la clase que hace lo siguiente:
Para empezar, te devuelve el nombre de todas las provincias de España y después un Input para que selecciones la que quieres.
Una vez escrito, la función lo que hace es pasar a mayúsculas el input que has escrito, ya que en el “Dataframe” están todos los nombres de las provincias en mayúsculas.
Si en nombre que nos ha devuelto el input no concuerda con ninguno de nuestro “Dataframe”, le vuelve a pedir un nombre de provincia. Así hasta que coincida con alguno.
La función filtra todos los puntos de información que tiene la provincia seleccionada, y en otro input, vuelve a pedir que selecciones un nombre de los que tenemos de esa provincia.
Una vez elegido el nombre otra vez, lo pasa a mayúsculas, y si no coincide con ningún nombre de esa provincia, vuelve a pedir otro nombre.

Finalmente, la clase te devuelve la latitud y la longitud del lugar seleccionado.

El formato de la latitud y la longitud es DMS, grados minutos segundos.

Ejemplo de uso:
pip install bianen 
from binanem import binanen 
la_lo=binanem(tu api key) 
binanem.cordenadas()
