What are the steps to run a container?
1. Create a Container file
2. Build the image `podman build --name myimg .`
3. Create and run the container in detached mode `podman run -d -t mycont -v /data:/var -e VAR=VALUE --network mynet localhost/myimg`

How to list all the available containers?::`podman ps`

How to list all the locally available images?::`podman images`

How to search for a remote image?::`podman search imagename`

How to create a new network?::`podman network create mynet --subnet 192.168.1.0/24 --gateway 192.168.1.1`

How to 