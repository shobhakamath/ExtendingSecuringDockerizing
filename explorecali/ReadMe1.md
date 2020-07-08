
https://labs.play-with-docker.com/

git clone https://github.com/shobhakamath/ExtendingSecuringDockerizing.git

docker run --detach --name ec-mysql -p 6604:3306 -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=explorecali -e MYSQL_USER=cali_user -e MYSQL_PASSWORD=cali_pass -d mysql

docker build -t explorecali .

docker run --name ec-app5 -p8080:8080 -d explorecali

docker ps -a
docker logs ec-app5

Click on the 8080 and copy the ip address details in the postman request and test. Tested well and is working well :)

docker inspect ec-app5

Steps to push to the docker hub

docker tag 26fb6f4aaaf5 shobhakamath/explorecali:latest
docker login
username:
password

docker push shobhakamath/explorecali - pushed to the dockerhub

no to test it 
docker rmi  shobhakamath/explorecali
docker run -it --link ec-mysql:mysql --rm mysql sh -c 'exec mysql -h"$MYSQL_PORT_3306_TCP_ADDR" -P"$MYSQL_PORT_3306_TCP_PORT" -uroot -p"$MYSQL_ENV_MYSQL_ROOT_PASSWORD"'

docker run --name ec-ap87 -p8081:8081 -d shobhakamath/explorecali- loads  from the dockerhub





