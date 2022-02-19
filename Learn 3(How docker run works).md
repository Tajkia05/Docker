
![Overview](https://github.com/SaiferGit/Learning_Docker/blob/master/More%20learning%20from%20udemy/learn3%20image1.png)

```docker run hello-world``` means We want to start up a new container using the image with the name of hello world. 


When we run ```docker run hello-world``` in our machine, that starts up **docker client** or CLI. Docker client takes command from me and communicates the command over to **Docker server**. 

**Docker server** then looks if the server already had a local copy. For this, Docker looks into **Image Cache** for this local copy. If it is not here, Docker server goes to **Docker Hub(Free service)** for looking that image.

Now if it got the image from docker hub, it downloaded that image and stored locally for future usage also.

Then docker server creates a container form that image and ran a single program inside of it.
