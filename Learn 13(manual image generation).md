![Mutual Image generation](https://github.com/SaiferGit/Learning_Docker/blob/master/More%20learning%20from%20udemy/learn13%20image1.png)


We can take a container and generate an image from it. We can use this custom image in future if we need.

Example:
```
> docker run -it alpine sh // start a conainer from alpine image
# apk add --update redis // install redis in it. Means, modified its' default file system.
```
open up another terminal:
```
> docker ps // getting the current container id.
> docker commit -c 'CMD ["redis-server"]' <id of that running container>   // -c specifies default command
```
The output will be id of the new customized image. we can run it through redis-server.
```
docker run redis-server
```