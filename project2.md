Container platform 1
    Install Instruction 
Docker installed on Kali
    -Sudo apt update
    -Sudo apt upgrade
    -sudo apt install -y docker.io
    -sudo systemctl enable docker --now
    -docker
Pulling and Running a container image
    -sudo docker pull hello-world
    -sudo docker run hello-world
    -sudo docker run -d -p hello-world
Logs & Status
    -Sudo docker stats
    -sudo docker ps
   