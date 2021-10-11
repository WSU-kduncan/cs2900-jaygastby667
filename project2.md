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

Skopeo installed on Kali

    -sudo apt-get -y install skopeo
    
    -skopeo

Pulling and Running a container image

    -sudo mkdir -p /var/lib/images/busybox
    
    -sudo skopeo copy docker://busybox:latest dir:/var/lib/images/busybox
    
    -sudo skopeo inspect docker://busybox
    
    -sudo skopeo run -d -p docker://busybox
    
Logs & Status

   -sudo skopeo inspect docker://busybox
   
Stopping a container

    -sudo skopeo delete --force docker://busybox:latest dir:/var/lib/images/busybox
