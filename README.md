# NodeJS Docker Deployment
1. git clone https://github.com/chamil-dev/NodeJS.git
2. cd NodeJS
3. cd Hello_Web
4. Host Type Debian/Ubuntu
 # Add Docker's official GPG key:
  sudo apt-get update -y
  sudo apt-get install -y ca-certificates curl gnupg 
  sudo install -m 0755 -d /etc/apt/keyrings
  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
  sudo chmod a+r /etc/apt/keyrings/docker.gpg

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
  sudo apt-get update -y
  sudo apt-get install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
  sudo docker run hello-world

# Build docker image and run the container
 
6. docker build -t hello_web_NodeJs .
7. docker run -d -p 9090:3000 hello_web_NodeJs
8. Test the URL http://<YOUR-SERVER-IP>:9090  
