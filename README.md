# jenkins-getting-started

## Run Jenkins with Docker

docker run -p 8080:8080 -p 50000:50000 jenkins/jenkins:lts

## Wait for image to download & run, then point browser to Jenkins URL

http://localhost:8080/login?from=%2F

## Get Jenkins Admin Password

docker exec -it $(docker ps -q) -- this will only work if there is only one container running :) otherwise specify the container ID to enter the running one

cat /var/jenkins_home/secrets/initialAdminPassword

