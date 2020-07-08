
https://labs.play-with-docker.com/

docker build -t explorecali .

docker run --name ec-app5 -p8080:8080 -d explorecali

docker ps -a
docker logs ec-app5

Click on the 8080 and copy the ip address details in the postman request and test. Tested well and is working well :)


