# lumen

#### `docker login -u ${DOCKER_USERNAME} -p ${DOCKER_PASSWORD}`

##### push prestashop 1.7
* `docker-compose up --build -d prestashop17`
* `docker tag prestashop_prestashop17 syednaeem15191/prestashop:1.7`
* `docker push syednaeem15191/prestashop:1.7`
* `docker tag prestashop_prestashop17 syednaeem15191/prestashop:latest`
* `docker push syednaeem15191/prestashop:latest`
* `docker-compose stop`
