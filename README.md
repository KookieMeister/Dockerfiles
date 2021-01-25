# Dockerfiles
Various Dockerfiles for projects hosted on my github repository
# Building the Docker image
1. Have Docker installed, find relevant instructions here: https://docs.docker.com/desktop/#download-and-install
2. After cloning the repository locally, navigate to the directory you're interested in building (minecraft_vanilla, minecraft_the_1122_pack, etc)
3. Run the following command to build the image from the relevant Dockerfile: 
    ```console
    me@mypc:$ docker build . -t minecraft:vanilla
    ```
4. The output will end with a similar message to the below (note that the build number of deaf9dc3da4d will be different in your build):
    ```console
    Successfully built deaf9dc3da4d
    Successfully tagged minecraft:vanilla
    ```
5. Upon that successful build, you'll want to run your image to verify it works, run the below:
    ```console
    me@mypc:$ docker run --env MINECRAFT_XMX=6GB minecraft:vanilla
    ```
6. Enjoy that fresh container!
