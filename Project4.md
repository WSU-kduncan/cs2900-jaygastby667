


Container Networking for Docker 

    -What networking mode(s) are supported and their capabilities
    
    Bridged - Default - used when your applications run in standalone containers that need to communicate.
  
    Host - removes network isolation between the container and the Docker host, and use the host’s networking directly
   
    None - none network driver does not attach containers to any network


-docker run --rm -d --network host --name my_nginx nginx



    Container Networking for Podman

bridge	Creates a network stack on the default bridge network
none	No networking is set up at all
container:<id>	Uses the same network as another container with ID id
host	Uses the host’s network stack
network-id	Uses a user-defined network (which you can create using podman network create ...)
ns:<path>	Joins a network namespace found at path <path>
private	Creates a new network namespace for the container
slirp4netns	Creates a user network stack with slirp4netns (This is the default option for rootless containers.)

    
    How to run the container and bind a host port to the container port

    podman run --network=host nginxinc/nginx-unprivileged



Find a Dockerfile linter (command line tool or VSCode plugin)

hadolint

What best practices does it search for?
labels

Find a scanner that can scan images for vulnerabilities
docker run --rm -i hadolint/hadolint 




What types of vulnerabilities are scanned?
checks if specific labels are present and conform to a predefined label schema