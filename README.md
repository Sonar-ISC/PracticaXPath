# Practica sobre el uso de XPath
Practica conceptual de como usar el XPath, de tal manera que se pueda usar para la interacción y manipulación del D.O.M. de una página web.
En esta Práctica, usaremos PowerShell o una página web especializada para realizar consultas sobre documentos XML mediante XPath. 

Utilizaremos el comando Select-Xml para ejecutar nuestras consultas.

## Prerrequisitos

### Uso de XPath en Powershell
~~~
Select-Xml -Path $PAth -XPath $XPath | Select-Object -ExpandProperty Node
~~~

### Uso de XPath en Bash
* Instalación de libxml2-utils
~~~
sudo apt-get install libxml2-utils
~~~
* Verificación de la instalación
~~~
xmllint --version
~~~
* Uso
~~~
xmllint --xpath $XPath $Path
~~~

### Uso de XPath en Bash

Link: https://www.freeformatter.com/xpath-tester.html

## Paso a paso

1. Abrir la consola en la carpera del repositorio ó la Página web
   - En caso de usar la página web, subir el archivo Catalog.xml en la página
3. Comprobar el funcionamiento correcto del lector de XPath mediante el siguiente comando:
  * Powershell
  ~~~
  Select-Xml -Path .\Catalog.xml -XPath "/" | Select-Object -ExpandProperty Node
  ~~~
  * Bash
  ~~~
  xmllint --xpath "/" Catalog.xml
  ~~~
  * Página Web
    
    Antes de ejecutar, debería verse así:
    ![image](https://github.com/Sonar-ISC/PracticaXPath/assets/70547458/fc048650-c620-4165-9b15-fac2be6c1012)

3. Preparar en un .txt los comandos XPath que den solución a las siguientes consultas:
 - Seleccionar todos los títulos de libros
 - Seleccionar todos los libros de fantasía
 - Seleccionar el precio del libro con ID "bk105"
 - Seleccionar todos los libros publicados después del año 2000
 - Seleccionar el autor del libro con título "Microsoft .NET: The Programming Bible"
 - Seleccionar todos los libros cuyos precios son mayores a 10
 - Seleccionar todos los libros de la categoría "Computer" publicados en diciembre de 2000
 - Seleccionar todos los libros ubicados después del libro con ID "bk106" (Lover Birds)
 - Seleccionar todos los libros ubicados antes del libro con ID "bk108" (Creepy Crawlies)
 - Seleccionar todos los libros que contengan la palabra "XML" en la descripción
 - 
5. Realizar una Pull Request con las respuestas a este taller (Documento guía disponible en el repositorio).
