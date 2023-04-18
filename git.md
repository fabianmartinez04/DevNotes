# GIT NOTES

## Crear repositorio

Inicializar un nuevo repositorio de Git en una carpeta local.

```
git init
```

Clonar un repositorio de Git existente en un servidor remoto a una carpeta local.

```
git clone https://github.com/nombre-usuario/repo.git
```

## Cambios

Agregar archivos al área de preparación (staging) antes de hacer una confirmación (commit).

```
git add archivo.txt
git add . (agregar todos los archivos)
```

Confirmar los cambios y guardarlos en el historial del repositorio.

```
git commit -m "Mensaje del commit"
```

Enviar los cambios confirmados en el repositorio local al repositorio remoto.
```
git push origin main
```

Descargar y fusionar los cambios del repositorio remoto en el repositorio local.
```
git pull origin main
```

## Estatus del repositorio

Ver el estado actual del repositorio y los archivos que han sido modificados, agregados o eliminados.

```
git status
```

Ver el historial del repositorio.

```
git log
```

## Ramas

Crear, listar y eliminar ramas en el repositorio.

```
git branch nueva-rama
git checkout -b nueva-rama (crearla y moverse a ella)
git branch -d rama (eliminarla)
```
## git grep

Busca en los archivos del repositorio cualquier ocurrencia de un patrón de búsqueda determinado. Puede usar este comando para buscar archivos específicos o para buscar en todo el repositorio.

1. Búsqueda de un patrón de búsqueda en un archivo específico:
```
git grep "patrón de búsqueda" archivo.txt
```
Este comando buscará el patrón de búsqueda en el archivo archivo.txt. Si hay una coincidencia, Git mostrará la línea que contiene la coincidencia.

2. Búsqueda de un patrón de búsqueda en todo el repositorio:
```
git grep "patrón de búsqueda"
```
Este comando buscará el patrón de búsqueda en todos los archivos del repositorio. Si hay una coincidencia, Git mostrará la línea que contiene la coincidencia, así como el nombre del archivo y la ubicación de la línea en el archivo.

3. Búsqueda de un patrón de búsqueda en un tipo de archivo específico:
```
git grep "patrón de búsqueda" -- '*.txt'
```
Este comando buscará el patrón de búsqueda solo en archivos con la extensión .txt. Puedes cambiar .txt a cualquier otra extensión de archivo que desees buscar.

4. Búsqueda de un patrón de búsqueda en el historial de Git:
```
git grep "patrón de búsqueda" $(git rev-list --all)
```

Este comando buscará el patrón de búsqueda en todo el historial de Git, incluidas las confirmaciones antiguas y las ramas eliminadas. Si hay una coincidencia, Git mostrará la línea que contiene la coincidencia, así como el nombre del archivo y la ubicación de la línea en el archivo.

## git show

Permite ver información detallada sobre una confirmación específica en tu repositorio Git. Puedes usarlo para ver los cambios realizados en esa confirmación, así como otra información relevante asociada a esa confirmación, como el autor, fecha, y mensaje de confirmación.

1. Ver los cambios realizados en la confirmación más reciente:
```
git show
```
2. Ver los cambios realizados en una confirmación específica:
```
git show <commit>
```
3. Ver los cambios realizados en una confirmación específica en un formato compacto:
```
git show --stat <commit>
```
Este comando mostrará una vista compacta de los cambios realizados en la confirmación <commit>, incluyendo el nombre de archivo, el número de líneas agregadas y eliminadas, y un resumen del cambio.
  
4. Ver la información detallada de una confirmación, incluyendo el autor, fecha, y mensaje de confirmación:
```
git show --stat --summary <commit>
```
