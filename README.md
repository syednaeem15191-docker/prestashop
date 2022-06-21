# Prestashop

#### `docker login -u ${DOCKER_USERNAME} -p ${DOCKER_PASSWORD}`

##### push lumen 9
* `docker-compose up --build -d prestashop1`
* `docker tag lumen_lumen9 syednaeem15191/prestashop1`
* `docker push syednaeem15191/prestashop1`
* `docker tag lumen_lumen8 syednaeem15191/prestashop1`
* `docker push syednaeem15191/prestashop1`
* `docker-compose stop`
