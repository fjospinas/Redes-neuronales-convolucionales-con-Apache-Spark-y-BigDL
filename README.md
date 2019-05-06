# Redes-neuronales-convolucionales-con-Apache-Spark-y-BigDL

## Instalación

1. Clonar repositorio:
    ```
    git clone https://github.com/fjospinas/Redes-neuronales-convolucionales-con-Apache-Spark-y-BigDL.git
    ```
2. Instalar [docker](https://docs.docker.com/install/).
2. Clonar imagen de docker de BigDL:
    ```
    docker pull elephantscale/bigdl
    ```
3. Lanzar container de bigdl:
    ```
    docker run -it -p 8888:8888 -p 8889:8889 -v <ruta_repositorio_clonado>:/home/jovyan/work --name bigdl elephantscale/bigdl /bin/bash
    ```
    Donde <ruta_repositorio_clonado> es la ruta en la cual fue clonado el repositorio del paso 1.
4. El comando anterior nos deja dentro del prompt del container, en este ejecutar: 
    ```
    cd work/ && /home/jovyan/run-jupyter-with-bigdl.sh
    ```
5. Entrar a la direción http:<ip_donde_correl_servidor>:8888 dentro de un navegador para ingresar a Jupyter.

## Reinicio del contenedor

En caso de apagar o reiniciar el PC donde se aloja el contenedor, para lanzar jupyter de nuevo, ejecutar los siguientes pasos.

1. Lanzar container previamente creado:
    ```
    docker start bigdl
    ```
2. Acceder al prompt del container:
    ```
    docker exec -it bigdl /bin/bash
    ```
3. Ejecutar pasos 5 y 6 de la sección anterior.