# Codespaces Airflow training environment

This repository contains the code for the Airflow training environment.

## Getting started

### 1) Check you have enough memory allocated to your codespaces instance:

* In the terminal (ctrl + ` ) check you have more than 4GB of allocated memory:

```
docker run --rm "debian:bullseye-slim" bash -c 'numfmt --to iec $(echo $(($(getconf _PHYS_PAGES) * $(getconf PAGE_SIZE))))'
```

An no, 3.9 is not enough. If you see 3.9 means that you did not selected the right machine in step 2.

<br>

### 2) Run database migrations *(ONLY RUN ONCE)*


 You need to run database migrations and create the first user account. It is all defined in the docker compose file so just run:
 ```
    docker compose up airflow-init
```
<br>

### 3) Now you can start all services:
```
    docker compose up
```

this will make Airflow available at: 
http://localhost:8080


### 8) Login to Airflow
![image](images/codespaces4.png)