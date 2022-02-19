![multiple commands for a container](https://github.com/SaiferGit/Learning_Docker/blob/master/More%20learning%20from%20udemy/learn9%20image1.png)

redis is an in memory database. To start redis db, we first need to start redis server and then redis client.
- ```redis-server``` 
- open another terminal and run ```redis-cli```
 - > set mynumber 5
 -  ok
 - > get my number
 - "5"

![exec command visualization](https://github.com/SaiferGit/Learning_Docker/blob/master/More%20learning%20from%20udemy/learn9%20image2.png)

Let's run redis-server using docker: ```docker run redis``` 
Now to run redis client, we need to run it under that server container. Otherwise the client won't find out the server.
**-t** is for nicely formating.

We can give shell access to a perticular container by using:
```
docker exec -it <container id> sh
```
Then, we can type our typical linux command in it.
