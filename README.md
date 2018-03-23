# airflow-simple-bolierplate

## dags folder:
/root/airflow/dags

## docker build image:
docker image build -t airflow-image-name /Dockerfile-Floder

## docker run example:
docker run --name airflow-contaniner-name -p 8080:8080 -v /airflow-dags-path:/root/airflow/dags -it airflow-image-name

# docker exec:
docker exec -it airflow-contaniner-name bash

## get key(python3 in bash):
from cryptography.fernet import Fernet
fernet_key= Fernet.generate_key()
print(fernet_key) # key's between ''

## change key
$export AIRFLOW__CORE__FERNET_KEY=your_fernet_key

## init database
airflow init database

## airflow server start
airflow webserver -p 8080

## airflow logs
airflow logs -t 50 -f airflow-contaniner-name
