### Install Docker on Linux:
- [Ubuntu](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- [Fedora](https://docs.docker.com/install/linux/docker-ce/fedora/)
- [CentOS](https://docs.docker.com/install/linux/docker-ce/centos/)
- [Debian](https://docs.docker.com/install/linux/docker-ce/debian/)

The Docker docs suggest setting up a Docker repository to install and update from. [Start Link](https://docs.docker.com/install/linux/docker-ce/ubuntu/#set-up-the-repository)

After completing the installation steps, test out Docker:
```sudo docker run hello-world```

### Installing Docker Compose:
[Compose installation here](https://docs.docker.com/compose/install/#install-compose)

After completing, test your installation:
```docker-compose -v```

### Run without Sudo:
[Run without sudo link](https://docs.docker.com/install/linux/linux-postinstall/#manage-docker-as-a-non-root-user)
```
sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker
```

### Start on Boot:
[Start boot](https://docs.docker.com/install/linux/linux-postinstall/#configure-docker-to-start-on-boot)
