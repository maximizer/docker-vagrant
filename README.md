docker-vagrant
==============

Build the vagrant box
```
% vagrant up

```

Vagrant ssh
```
% vagranst ssh
Last login: Tue Apr 22 19:47:09 2014 from 10.0.2.2
vagrant@ubuntu-14:~$ 
```

Build the container
```
vagrant@ubuntu-14:~$ cd /vagrant/node-sandbox/
vagrant@ubuntu-14:/vagrant/node-sandbox$ sudo docker build -t mizer/node-sandbox .
```

Run the container
```
vagrant@ubuntu-14:~$ sudo docker run -p 7074:7074 -d mizer/node-sandbox
vagrant@ubuntu-14:~$ sudo docker ps

CONTAINER ID        IMAGE                       COMMAND                CREATED             STATUS              PORTS                    NAMES
4bee859ffb52        mizer/node-sandbox:latest   nodejs /node-sandbox   3 seconds ago       Up 3 seconds        0.0.0.0:7074->7074/tcp   desperate_babbage  

```

Hit the node app in your browser: http://localhost:7074


