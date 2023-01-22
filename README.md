# wget-direct-link
Uso de wget para descargar archivos de mis repositorios públicos de Github en forma directa, en el directorio de Linux o DOS actual.

## Un único archivo 

Para descargar ```file``` del repositorio ```repo_name``` y copiarlo en ```arch_destino``` del directorio actual

### Usar:

    wget [-O arch_destino] https://raw.githubusercontent.com/migrassi/repo_name/branch/path/to/file 
    
### O también:   

    wget  [-O arch_destino] https://github.com/migrassi/repo_name/raw/branch/path/to/file    
 
 Si se omite ```[-O arch_destino]```, el archivo se copia con el mismo nombre que el original.
    
## Ejemplos:

    cd ~/
    mkdir Downloads
    cd Downloads/
    wget https://github.com/migrassi/Visera/raw/master/README.md
    
O también:

    cd ~/
    mkdir Downloads
    cd Downloads/
    wget https://raw.githubusercontent.com/migrassi/Visera/master/README.md
     

## Directorios (carpetas) o proyectos completos

Github no permite la descarga mediante wget de un directorio completo en forma recursiva, por ejemplo usando 

    wget -r --no-parent https://raw.githubusercontent.com/migrassi/Visera/master/ <-ESTO NO FUNCIONA

Github devuelve un ``error 400: Invalid request``. Por lo tanto, si se necesita descargar directorios completos es mucho más práctico utilizar Git, que está diseñado para eso. Por ejemplo, para clonar el repo del proyecto Visera completo basta con usar:

     git clone https://github.com/migrassi/Visera.git
