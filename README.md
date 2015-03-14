# asp-net-5-hello-world
First Example for ASP.NET and PlayGround

Use for tests with docker images based on the docker image

Use the following steps:

git clone https://github.com/VolkerCH/asp-net-5-hello-world.git hello-world
cd hello-world/src/HelloWorld
docker build -t hello-mvc .

docker run -t -d -p 80:5004 hello-mvc
