# mc3-m12-capstone-v2 

## Introducción 

Debido a las últimas actualizaciones tanto de AWS Academy como en relación a los datos externos que se usaban en la práctica, vamos a proporcionaros un entorno local para que podáis poner a prueba los conocimientos adquiridos durante el módulo, en vez de utilizar EMR. Asimismo, en vez de utilizar el dataset de reviews de amazon alojado en S3 usaremos el mismo dataset pero en local. 

Para la ejecución de código Spark, se os proporciona un Dockerfile (`.devcontainer/Dockerfile`) con las dependencias necesarias para ejecutar el capstone usando Spark dentro de cuadernos de Jupyter. 
Para facilitar la ejecución de esta imagen se proporciona, adicionalmente, un `docker-compose.yml` que ejecutará un entorno de Jupyter con el que podréis seguir la práctica. 

En el directorio `notebooks` ya se os proporcionan los dos cuadernos en los que se divide este capstone, adaptados a los nuevos requisitos de este (especificamente, a usar los datos en local). 

## Uso del entorno Spark

En primer lugar, necesitaréis construir la imagen del servicio. Para ello podéis usar (tardará 10-20 min):
```
docker-compose build
```

Esto construirá la imagen para el servicio `pyspark-notebook`. Tras esto, podeis lanzar el entorno usando:
```
docker-compose up
```

Esto iniciará un entorno de Jupyter Lab que se quedará escuchando en `https://127.0.0.1:8888/lab`. Para entrar tendréis que introducir el token que es: `cidaen`. Con esto ya estaríais en disposición de comenzar con el capstone. 

## Preparación de los datos

Los datos se os proporcionan en un fichero .tar.gz en CampusVirtual. El fichero ocupa unos 5.5gb por lo que tardará un poco en descargar, dependiendo de vuestra conexión. Una vez en vuestra máquina, tendréis que descomprimirlo de forma que tengáis un directorio `data/amazon-reviews-pds-parquet` con las particiones y ficheros parquet que vais a usar. Este directorio se puede leer con Spark como hemos visto en el módulo. 

## Entrega del capstone

Una vez dada solución a los problemas del capstone, subid al entregable del campus virtual ambos cuadernos completos y totalmente ejecutados. No es necesario que subáis datos ni los modelos generados. 
