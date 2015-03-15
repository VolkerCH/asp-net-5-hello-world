# asp-net-5-hello-world
First Example for ASP.NET and PlayGround

Use for tests with docker images based on the docker image

Use the following steps:

Copy solution and Dockerfile to Docker VM:
`git clone https://github.com/VolkerCH/asp-net-5-hello-world.git hello-world`

Run the Docker build command in project directory to create the Docker image:
`cd hello-world/src/HelloWorld`
`docker build -t hello-mvc .`

Start the container based on the new image:
`docker run -t -d -p 80:5004 hello-mvc`

Run `docker images` to find out the ID of the container to go to command line:
`docker exec -it <<id of running container>> /bin/bash` 
