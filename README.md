# nginx-docker-compose

## Clone repository

```
git clone https://github.com/drajanikant/nginx-docker-compose.git
```

## Change the directory

```
cd nginx-docker-compose
```

## Create the configuration file 

```
touch mysite.template
```

## Paste the configuration details that you have for the nginx server.
For the example following file can be used
```
server {
    listen 80;
    server_name localhost;

    location /api {
       proxy_pass http://host.docker.internal:8080/api;
    }
}
```

## Use following command to start nginx

```
docker-compose up -d
```
