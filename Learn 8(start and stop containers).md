![docker create and start](https://github.com/SaiferGit/Learning_Docker/blob/master/More%20learning%20from%20udemy/learn8%20image1.png)

when we run stop, a primary process created by HW goes into the container and sends a message **SIGTERM**(terminate signal). Which means, shutdown at your own time. It gives that container 10 additional seconds for sutting down itself. If the container still runs, docker automatically issues a kill command and shutdown that container.

when we run kill, a primary process created by HW goes into the container and sends a message **SIGKill**(kill signal). Which means, shutdown right now, don't do any additional work! 