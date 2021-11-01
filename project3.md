Container platform 1 Docker
    Investigate available mounts
        -Volumes -v "$(pwd)"/target:/app \
        -Bind Mounts --mount type=bind,source="$(pwd)"/target,target=/app \
    Building images for Docker
        -Use dockerfile to build image
        mkdir myproject && cd myproject
        echo "hello" > hello
        echo -e "FROM busybox\nCOPY /hello /\nRUN cat /hello" > Dockerfile
        docker build -t helloapp:v1 .

Container platform 2 Podman
    Investigate available mounts
       -Bind Mounts podman mount c831414b10a3
        /var/lib/containers/storage/overlay/f3ac502d97b5681989dff84dfedc8354239bcecbdc2692f9a639f4e080a02364/merged
        -Volumes podman run -dit --volume src:/dest busybox
    Building images for Podman
        -Can use Containerfiles or Dockerfiles
        podman build -f dev/Containerfile https://10.10.10.1/podman/context.tar.gz