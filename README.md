# Despliegue de sistemas predictivos
> Diplodatos 2020

Alumno: Mario Gustavo Echeverria

## Práctico 1

### Resolución:
Ver primer commit

## Práctico 2

### Parte 1: 
[Video Parte 1]
(https://www.loom.com/share/f89df987642b4f4884a1848aa479f38b)

### Parte 2: 
[Video Parte 2]
(https://www.loom.com/share/248ace4f0885440abe7f397e371e7178)


## Instalar y ejecutar

```
$ docker-compose up --build -d
```

Para detener los servicios:

```
$ docker-compose down
```

## Tests

- Instalar un virtualenv con los requirements.txt del origen
```
virtualenv --python=python3.5 .env
source .env/bin/activate
pip install -r requirements.txt
```
- Correr los tests con nosetests
```
nosetests [<package_name>]
```

- Si no tienen python3.5 y no lo quieren instalar, pueden probar instanciando un container con python 3.5 montando un volumen para ver los cambios dinamicamente

```
docker run -v $(pwd):/src -it --net=host -w /src python:3.5 bash
pip install -r requirements.txt
nosetests [<package_name>]
```
