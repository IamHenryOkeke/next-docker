## Getting Started

Ensure you have Docker installed on your local machine

Head [here](https://www.docker.com/products/docker-desktop/) to download Docker Desktop for your local machine

## Project setup

- Open your NextJS project of choice
- Create a new file called **Dockerfile** an open it
- Use the FROM instruction to specify the base image that your image will be built on in this case node
- Use the RUN instruction to execute commands that will be run during the image build process.
- Use the COPY instruction to copy files or folders from your local machine to the docker image.
- Use the ESPOSE instruction to determine which port the app will run on.
- Use the CMD instruction to specify the command that will be run when a container is created from the image.
- Save the Dockerfile.
- Open a terminal window and run the following command to build the image

<code>
  docker build -t my-image-name .
</code>

The code above build the docker image into a docker container. The -t flag is used to give the image a name(tag), in this case "my-image-name". The . at the end specifies the current directory (your project root folder) as the build context.

Once the image is built, you can run it using the following command:

<code>
  docker run -p 3000:3000 my-image
</code>

This command runs the image and maps port 3000 on the host to port 3000 in the docker container.
