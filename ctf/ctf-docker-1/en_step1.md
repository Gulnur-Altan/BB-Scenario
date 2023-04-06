# Docker Workshop

## 1) Preparation
In this step, we expect you to create a folder named ``/home/ctf-docker-1``.

## 2) Copying Sample Project
In this step, we expect you to copy the project linked below under the ``/home/ctf-docker-1`` folder you created earlier. You can use the "GIT" command for this.
``https://github.com/merve-naz/BB-Senaryo-Dockerfile-Go.git``

## 3) File Checks
In the second step, it is recommended that you check if the project is copied under the "/home/ctf-docker-1" directory. If you have done everything correctly, a directory named ``BB-Senaryo-Dockerfile-Go`` should be created under this directory.

3.1 There will be a folder named "BB-Senaryo-Dockerfile-Go" here. This is the name of the project we pulled from Github. Now, let's enter this folder.

Make sure these files exist in the relevant directory. If the files are missing, something has gone wrong somewhere.

- Dockerfile go.mod main.go
- docker-compose.yaml go.sum public

3.2 At this stage, you are expected to review a DockerFile. You need to follow the standards in the Dockerfile. You should correct any missing or incorrect parts.

- `vi`: File content editing

3.3 Once you have corrected the Dockerfile, you can now build the Docker image. You should assign a tag with "latest" during the build process. ("You should write the command indicated by d****.")

- `d**** ***** -t <new_image_name>:latest .`

3.4 You need to bring up the application that you built and created an image for. (Hint: If we look at the main.go file in the go project pulled from Github, we see that it is host_port:8080.)

- `d***** *** -p <host_port>:<container_port> --name <container_name> :latest`

3.5 Our application has successfully started. Review whether the container containing our application is running and which ports it is connected to.

- `****** ps`

3.6 You can enter a running Docker container using the docker exec -it command to change the files in the image. Run the command below.

```
docker exec -it   my-container /bin/sh
```

3.7 Let's open the index.html file in the public folder with a text editor and change it. Change the "Hoşgeldiniz BB" text to "WELCOME".

- Exit the container.

3.8 Stop the Docker container and create a new image, and then bring up the container with the created image.

- Hint: You need to delete the old image before creating a new image.
- `docker rmi`: Deleting an image

3.9 To push this image we created to DockerHub, first create a profile on the Dockerhub website.

3.10 Enter the following command in the terminal. When the command runs, it will ask for your username and password.
``` 
docker login
``` 
3.11 To upload your Docker image to Docker Hub, you first need to tag your image with your Docker Hub username. (If you did this when creating the image, this is not necessary.)

`docker tag <image_id or image_name> <Docker_Hub_Username>/<Image_Name>:latest`

3.12 Push your Docker image to Docker Hub.