# my-example-compose

## clone the git in you terminal 
```git clone https://github.com/driller23/my-example-compose.git```

## run docker compose 
```docker compose up -d```

## run watch command 
```docker compose alpha watch```

## watch in action
- open web browser on port 80
- change web/servers.js 
- see in the terminal that docker is rebuild the conatiner 

```└❯ docker compose alpha watch
watch command is EXPERIMENTAL
watching /home/igaldahan/workspace/sela/docker/my-example-compose/nginx
watching /home/igaldahan/workspace/sela/docker/my-example-compose/web
watching /home/igaldahan/workspace/sela/docker/my-example-compose/app
change detected on /home/igaldahan/workspace/sela/docker/my-example-compose/web/server.js
change detected on /home/igaldahan/workspace/sela/docker/my-example-compose/web/server.js
change detected on /home/igaldahan/workspace/sela/docker/my-example-compose/web/server.js
change detected on /home/igaldahan/workspace/sela/docker/my-example-compose/web/server.js
change detected on /home/igaldahan/workspace/sela/docker/my-example-compose/web/server.js
Rebuilding web after changes were detected:
  - /home/igaldahan/workspace/sela/docker/my-example-compose/web/server.js
[+] Building 0.0s (0/1)                                                                                                                           
[+] Building 0.2s (2/3)                                                                                                                           
 => [internal] load .dockerignore                                                                                                            0.0s
 => => transferring context: 2B                                                                                                              0.0s
 => [internal] load build definition from Dockerfile                                                                                         0.0s
 => => transferring dockerfile: 158B                                                                                                         0.0s
[+] Building 0.8s (10/10) FINISHED                                                                                                                
 => [internal] load .dockerignore                                                                                                            0.0s
 => => transferring context: 2B                                                                                                              0.0s
 => [internal] load build definition from Dockerfile                                                                                         0.0s
 => => transferring dockerfile: 158B                                                                                                         0.0s
 => [internal] load metadata for docker.io/library/node:alpine                                                                               0.8s
 => [1/5] FROM docker.io/library/node:alpine@sha256:cc4e8f3d78a276fa05eae1803b6f8cbb43145441f54c828ab14e0c19dd95c6fd                         0.0s
 => [internal] load build context                                                                                                            0.0s
 => => transferring context: 63B                                                                                                             0.0s
 => CACHED [2/5] WORKDIR /usr/src/app                                                                                                        0.0s
 => CACHED [3/5] COPY ./package*.json ./                                                                                                     0.0s
[+] Building 0.8s (10/10) FINISHED                                                                                                                
 => [internal] load .dockerignore                                                                                                            0.0s
 => => transferring context: 2B                                                                                                              0.0s
 => [internal] load build definition from Dockerfile                                                                                         0.0s
 => => transferring dockerfile: 158B                                                                                                         0.0s
 => [internal] load metadata for docker.io/library/node:alpine                                                                               0.8s
 => [1/5] FROM docker.io/library/node:alpine@sha256:cc4e8f3d78a276fa05eae1803b6f8cbb43145441f54c828ab14e0c19dd95c6fd                         0.0s
 => [internal] load build context                                                                                                            0.0s
 => => transferring context: 735B                                                                                                            0.0s
 => CACHED [2/5] WORKDIR /usr/src/app                                                                                                        0.0s
 => CACHED [3/5] COPY ./package.json ./                                                                                                      0.0s
 => CACHED [4/5] RUN npm install                                                                                                             0.0s
 => [5/5] COPY ./server.js ./                                                                                                                0.0s
 => exporting to image                                                                                                                       0.0s
 => => exporting layers                                                                                                                      0.0s
 => => writing image sha256:16351647922424230962e2361bf4b9130c644fc36471798813706a6797967535                                                 0.0s
 => => naming to docker.io/library/my-example-compose-web                                                                                    0.0s
[+] Building 0.0s (8/8) FINISHED                                                                                                                  
 => [internal] load build definition from Dockerfile                                                                                         0.0s
 => => transferring dockerfile: 134B                                                                                                         0.0s
 => [internal] load .dockerignore                                                                                                            0.0s
 => => transferring context: 2B                                                                                                              0.0s
 => [internal] load metadata for docker.io/library/nginx:latest                                                                              0.0s
 => [1/3] FROM docker.io/library/nginx                                                                                                       0.0s
 => [internal] load build context                                                                                                            0.0s
 => => transferring context: 32B                                                                                                             0.0s
 => CACHED [2/3] RUN rm /etc/nginx/conf.d/default.conf                                                                                       0.0s
 => CACHED [3/3] COPY nginx.conf /etc/nginx/conf.d/default.conf                                                                              0.0s
 => exporting to image                                                                                                                       0.0s
 => => exporting layers                                                                                                                      0.0s
 => => writing image sha256:6f04a7137fd6faf1f87c4666952cdc024fd00ba7828f5db69bbc667dceddfb6d                                                 0.0s
 => => naming to docker.io/library/my-example-compose-nginx                                                                                  0.0s
[+] Running 4/4
 ✔ Container my-example-compose-web-1    Started                                                                                             1.5s 
 ✔ Container my-example-compose-app-1    Running                                                                                             0.0s 
 ✔ Container my-example-compose-redis-1  Running                                                                                             0.0s 
 ✔ Container my-example-compose-nginx-1  Started                                                                                             1.0s 
```

- re watch the browser to see changes 
