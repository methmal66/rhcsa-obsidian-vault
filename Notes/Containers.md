What are the steps to run a container?
1. Create a Container file
2. Build the image `podman build --name myimg .`
3. Create and run the image in detached mode `podman run -d -t mycont -v /data:/var -e VAR=VALUE --network mynet localhost/myimg`

How to list all the available containers?::`podman ps`

How to list all the locally available images?::`podman images`

How to search for a system 
