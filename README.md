# Quick reference

- **Maintained by**:  
    [Jover Zhang](http://120.79.178.151) <joverzh@gmail.com>

- **Supported Versions**:  
    The project only supported last version for [JoverSite](https://github.com/JoverSite).

# Micro service list

- **[web_ui](https://github.com/JoverSite/dockerfile/web_ui)**:  
    [Web_ui](https://github.com/JoverSite/dockerfile/web_ui) is a web server.  
    Use **[vue](https://github.com/vuejs/vue)** for **front end** framework.  
    Use **[koa](https://github.com/koajs/koa)** in **[node](https://github.com/nodejs/node)** as **back end** framework.  

# Usage
To building any docker image by Dockerfile.
```shell script
git clone [other_sub-project]
docker build -t [image_name:tag] .
```

To download the project using git and using docker-compose to running these sub-projects.
```shell script
git clone -b master https://github.com/JoverSite/devops
docker swarm init --advertise-addr [your_ip]
docker-compose up
```
