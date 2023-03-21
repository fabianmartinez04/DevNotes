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

