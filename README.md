# react-nginx
This is simple learning project of nginx

<img src="https://raw.githubusercontent.com/docker-library/docs/01c12653951b2fe592c1f93a13b4e289ada0e3a1/nginx/logo.png"/><br /><img src="https://webassets.mongodb.com/_com_assets/cms/mongodb-logo-rgb-j6w271g1xn.jpg" width="256"> <img src="https://brew.sh/assets/img/homebrew-256x256.png" height="72">

### What is nginx?
> Nginx (pronounced "engine-x") is an open source reverse proxy server for HTTP, HTTPS, SMTP, POP3, and IMAP protocols, as well as a load balancer, HTTP cache, and a web server (origin server). The nginx project started with a strong focus on high concurrency, high performance and low memory usage. It is licensed under the 2-clause BSD-like license and it runs on Linux, BSD variants, Mac OS X, Solaris, AIX, HP-UX, as well as on other *nix flavors. It also has a proof of concept port for Microsoft Windows.


`$ docker run --name some-nginx -v /some/content:/usr/share/nginx/html:ro -d nginx`

Alternatively, a simple Dockerfile can be used to generate a new image that includes the necessary content (which is a much cleaner solution than the bind mount above):

```docker
FROM nginx
COPY static-html-directory /usr/share/nginx/html
```
Place this file in the same directory as your directory of content ("static-html-directory"), run docker build -t some-content-nginx ., then start your container:

$ docker run --name some-nginx -d some-content-nginx
