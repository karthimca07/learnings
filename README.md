Create a Jenkins CICD Pipeline to Build a Docker Image with Splunk Integration

git clone https://github.com/cloudacademy/devops-jenkins-docker-splunk.git
cd ./devops-jenkins-docker-splunk

//pulls the latest jenkins images
docker pull jenkins/jenkins:lts  

// runs the docker-compose.yml file 
// && means run the next command if the prevoious one succeeds
// the next command stream the logs from all container
docker-compose up -d && docker-compose logs -f

//command to list docker container with formatting
docker ps -a --format "table {{.Names}}\t{{.Status}}"
