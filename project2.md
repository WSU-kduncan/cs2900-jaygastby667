Container platform 1

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
    
Stopping a container

    -sudo docker pause hello-world
    
    -sudo docker unpause hello-world
    
    sudo docker kill hello-world

Container platform 2

Podman installed on Kali

    -apt install podman
    
    -podman

Pulling and Running a container image

    -sudo podman pull fedora
    
    -sudo podman run fedora
    
    -sudo podman run -d fedora
    
Logs & Status

   -Sudo podman stats
    
    -sudo podman ps
   
Stopping a container

    -sudo podman pause fedora
    
    -sudo podman unpause fedora
    
    sudo podman kill fedora
