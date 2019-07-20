# valgrind

In order to make Valgrind run Nginx you can do (a) or (b) below:


(a) Build and run docker image using the Docker file Docker.nginx.valgrind
```
mkdir ${HOME}/sandbox
docker build . -t valgrind -f Dockerfile.nginx.valgrin
docker run -it -p 80:80 -v ${HOME}/sandbox:/sandbox valgrind 
```

(b) Run the following (Public) Docker image:
```
mkdir ${HOME}/sandbox/
docker run -it -p 80:80 -v ${HOME}/sandbox:/sandbox dudidockerhub/nginx:version2.0
```
