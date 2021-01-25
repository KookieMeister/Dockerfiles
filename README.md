# Dockerfiles
Various Dockerfiles for projects hosted on my github repository
The below describes what each Dockerfile does:
<ul>
    <li>minecraft_vanilla
        <ul>
            <li>This is just a vanilla minecraft server, the version is not the latest</li>
        </ul>
    </li>
    <li>minecraft_the1122_pack
        <ul>
            <li>This is the mod pack known as "The 1.12.2 Pack" as seen  <a href="https://www.technicpack.net/modpack/the-1122-pack.1406454">here</a> </li>
        </ul>
    </li>
 </ul>
    
    
# Building the Docker image
<ol>
    <li>Have Docker installed, find relevant instructions here: https://docs.docker.com/desktop/#download-and-install</li>
    <li>After cloning the repository locally, navigate to the directory you're interested in building (minecraft_vanilla, minecraft_the_1122_pack, etc)</li>
    <li>Run the following command to build the image from the relevant Dockerfile:
        <ol>
            <li><code>me@mypc:$ docker build . -t minecraft:vanilla</code></li>
        </ol>
    </li>
    <li>The output will end with a similar message to the below (note that the build number of deaf9dc3da4d will be different in your build):
        <code>Successfully built deaf9dc3da4d</code></br>
        <code>Successfully tagged minecraft:vanilla</code>
    </li>
<li>Upon that successful build, you'll want to run your image to verify it works, run the below (change the MINECRAFT_XMX environment variable to suit your needs, it is the java heap xmx):
    <ol>
        <li><code>me@mypc:$ docker run --env MINECRAFT_XMX=6GB minecraft:vanilla</code></li>
    </ol>
</li>
<li>Enjoy that fresh container!</li>
</ol>
