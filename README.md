To build image from the Dockerfile:
docker build --tag easewithdata/pyspark-jupyter-lab .

To create container from image
docker run -d -p 8888:8888 -p 4040:4040 --name jupyter-lab easewithdata/pyspark-jupyter-lab

In case you are still not able to setup, just pull the image from docker hub
docker pull easewithdata/pyspark-jupyter-lab


#### repo: pyspark-zero-to-hero
Learn PySpark from Basics to Advanced. 
Checkout the YouTube Series : [PySpark - Zero to Hero] 

URL - https://youtube.com/playlist?list=PL2IsFZBGM_IHCl9zhRVC1EXTomkEp_1zm


#### Spark Container - KP
https://github.com/subhamkharwal/docker-images
jupyter-docker-lab
docker compose up

## KP version
docker build -t ewd/pyspark-jupyter-lab-kp .
docker run -it -p 8888:8888 -p 4040:4040 -v /home/krisubu/GitProjects/ewd-pyspark-zero-to-hero:/home/jupyter/pyspark-zero-to-hero --name jupyter-lab ewd/pyspark-jupyter-lab-kp

docker stop jupyter-lab
docker start -ai jupyter-lab

instead of -v can use:
  --mount type=bind,source=/home/krisubu/GitProjects/ewd-pyspark-zero-to-hero,target=/home/jupyter/pyspark-zero-to-hero \

-- interactive
JupyterLab > Terminal > /bin/bash
spark: /spark/bin/pyspark

-- create container from image
docker run -it -p 8888:8888 -p 4040:4040 --name jupyter-lab easewithdata/pyspark-jupyter-lab

#### Spark container - old spark image from sub
- download from here
https://hub.docker.com/r/easewithdata/pyspark-jupyter-lab/tags

-- list images
docker images
-- list containers
docker ps -a

-- run container
docker run -it -p 4040:4040 -p 8888:8888 --name ewd-pyspark easewithdata/pyspark-jupyter-lab-old:latest

#### Spark Clusters repo
https://github.com/subhamkharwal/docker-images

-clone repo
-cwd: /ewd-docker-images/pyspark-cluster-with-jupyter/
docker compose up

get link with token, get the token: 
--Jupyter Lab, use Token and create pwd
localhost:8888

-- create SparkSession / Spark cluster
from pyspark.sql import SparkSession
spark = SparkSession.builder.getOrCreate()

spark
-- check Spark Engine, Jobs

locahost:4040

#### Working with cluster
data folder

JupyterLab > Terminal > /bin/bash > cd / > ls -ltr (data folder)

pwd
cd /home/jupyter - location of folders created
cp abc.txt /data

