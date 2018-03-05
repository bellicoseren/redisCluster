# Redis cluster 

Cluster redis Statefulsets

## Uso local

Ejecuta el yaml para la creación de archivos de configuración para la instalación de redis cluster puede ser dentro de la consola de 
openshift situarse en:
```
Add to Project-Import Yaml
```

Colocar la ruta en donde se encuentra el archivo redis-configmap.yaml


Ejecuta el yaml para la instalación de redis cluster puede ser dentro de la consola de  openshift situarse en:

```
Add to Project-Import Yaml
```

Colocar la ruta en donde se encuentra el archivo redis_cluster_statefulsets.yaml



## Pruebas de Redis-cli


Para poder realizar pruebas de replica de información entre nodos realizar las siguientes acciones:

1.- Generar un nuevo nodo de redis para accesar al cluster del nodo Master

Ejecuta el yaml para la creación del nodo de redis puede ser dentro de la consola de openshift situarse en:

```
Add to Project-Import Yaml
```

Colocar la ruta en donde se encuentra el archivo redis_nodo.yaml

## Comandos para realizar prueba en cluster redis

Accesar a la terminal de redis-nodo y ejecuta el siguiente comando:

```
redis-cli -h redis-0.redis SET mensaje "Prueba Cluster Redis"
```
Para conectarse a otros nodos del cluster solo basta con sustituir redis-0 por el nombre del nodo

```
redis-cli -h redis-0.redis get mensaje 
```
