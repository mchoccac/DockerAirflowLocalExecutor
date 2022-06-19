### image-docker help
https://airflow.apache.org/docs/docker-stack/build.html

### Run this before starting docker-compose.yml
```
	mkdir -p ./dags ./logs ./plugins ./postgres
```
### Quick start
1. docker-compose up
2. Please wait while it configures
3. user: ```airflow```, pass: ```airflow```

## Add other packages
### packages
Search here before the packages to add it to the image.
https://raw.githubusercontent.com/apache/airflow/constraints-2.3.2/constraints-3.7.txt

### Steps to add packages to the image

1. Look for the constraints-3.7.txt package, if it doesn't appear you can install the most recent version.
2. Open the Python Dockerfile, add the package you want (RUN pip install --no-cache-dir PACKAGE_NAME)
3. Save the changes
4. Run the following ```docker build . -f DockerfileAirflow --pull --tag choc/airflow:2.3.2```
5. docker-compose down
6. docker-compose up
