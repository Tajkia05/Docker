Building a example dockerfile

## EX: Build an image which runs redis-server

![Solution](https://github.com/SaiferGit/Learning_Docker/blob/master/More%20learning%20from%20udemy/learn11%20image1.png)


```
# Use an existing docker image as a base
FROM alpine // we want to use alpine as our base image

# Download and install a dependecy(preparing our custom image)
RUN apk add --update redis // we want to run this command

# Tell the image what to do when it starts as a container
CMD ["redis-server"]
```

Run using ```docker build .``` and then ```docker run <container id>```

### Look at the following image for better understanding:

![Google Chrome install example where no OS in PC](https://github.com/SaiferGit/Learning_Docker/blob/master/More%20learning%20from%20udemy/learn11%20image2.png)

When someone asks install google chrome a computer where no OS has installed, we first install a OS(which have the ability to run chrome) then we install google chrome and thus run it. 

Here, installing windows means base image, which have startup chrome.exe file for google chrome(CMD command). 


![Explain how dockerfile works for this example](https://github.com/SaiferGit/Learning_Docker/blob/master/More%20learning%20from%20udemy/learn11%20image3.png)


### Explaining commands:
1. ```docker build .```
Here, docker is reffering to client,  build means building an image, . means context(directory of docker file).

 - ```FROM alpine``` downloaded alpine image from docker hub. This has 2 things, File System snapshot and startup command. At this point we don't know our startup command.
 - When docker sees ```RUN``` command, it goes back to previous step to look up what the image is and makes a temporary container of it. Then it takes a snapshot in HDD segment and get the **RUN** command inside **running process**. Then it installs redis inside of that snapshot, immediately removes this temorary container and keeps a snapshot of it in a new image.
 - Finally in ```CMD```, docker first looks for the image that was created from previous step, then creates a snapshot and primary command for this image(which is ```redis-server``` here) and takes a final snapshot and close that container and thus build the final image.  
