### Variations in docker run command:

**Overriding default commands:**
In general we run:
```docker run hello-world``


![Overriding run command](https://github.com/SaiferGit/Learning_Docker/blob/master/More%20learning%20from%20udemy/learn5%20image1.png)


Variations in docker run gives us overriding default commands. We supply an alternate command to be executed inside the container after it starts up. So, whatever default command is included inside of the image is not going to be executed, only our override command will executed.

```
docker run busybox echo hi there // will print *hi there* inside that container.
docker run postgres ls // will print file lists inside of that container.
```
So, busybox, postgres has executable ```ls``` and ```echo``` command in there container. If they give any error to an override command, that command's executable is not in that container and so we can't run that override command. 
