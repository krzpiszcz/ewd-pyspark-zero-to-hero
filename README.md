# pyspark-zero-to-hero
Learn PySpark from Basics to Advanced. 

Checkout the YouTube Series : [PySpark - Zero to Hero] 


URL - https://youtube.com/playlist?list=PL2IsFZBGM_IHCl9zhRVC1EXTomkEp_1zm

# Spark container
- download from here
https://hub.docker.com/r/easewithdata/pyspark-jupyter-lab/tags

-- list images
docker images
-- list containers
docker ps -a

-- run container
docker run -it -p 4040:4040 -p 8888:8888 --name ewd-pyspark easewithdata/pyspark-jupyter-lab-old:latest

d762095909a3b8bc6695d28169b7414aa941c33b84d12466

# Spark Clusters repo
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

token 
6ef5cd4d94303da06bf8b9faf47b0ef690735b8dad22353d
pwd: spark1234

# Working with cluster
data folder

JupyterLab > Terminal > /bin/bash > cd / > ls -ltr (data folder)
