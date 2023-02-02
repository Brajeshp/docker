# How to install docker

OS requirement : Ubuntu Kinetic 22.10, Ubuntu Jammy 22.04 (LTS), Ubuntu Focal 20.04 (LTS), Ubuntu Bionic 18.04 (LTS)

**1. Uninstall previous instances of docker**

Using following command, uninstall old docker version (if any) 

sudo apt-get remove docker docker-engine docker.io containerd runc

**2. Set up the repository**

Using following commands in sequence, 

sudo apt-get update 

sudo apt-get install ca-certificates curl gnupg lsb-release

sudo mkdir -p /etc/apt/keyrings curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | 
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

**3. Install Docker Engine**

sudo apt-get update sudo chmod a+r /etc/apt/keyrings/docker.gpg sudo apt-get update

Install the latest version,

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin

**4. Verify installation**

sudo docker run hello-world

This command downloads a test image and runs it in a container. When the container runs, it prints a confirmation message and exits.
