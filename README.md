#Rasputin Labs presents BlackMail as a Service (jk)

This is the representation of the final set of services and stack for the app.

```bash
git clone https://github.com/RasputinLabs/blackmail-beta .
```

```bash
docker-compose up
```

A few notes:
This stack is a work in progress and honestly isn't entirely representational of a production-ready app. That being said, it's meant as a learning resource and a working example. There are lots of insecure passwords. This project comes with no warranty and was cobbled together from resources across the web. If you have questions please open an issue so we can answer it here.

## Homework Assignment
If you want a small learning exercise please fix the redis stack. The redis conf is loaded from a volume on the host. It would be much better and more portable to build a new redis image that includes this conf and runs it by default. You will have to create a docker ID and set up a repository. When you build your image you will need to tag it before pushing like below:

```bash
docker login
docker build -t <yournamespace>/redis:latest -t <yournamespace>/redis:0.1 .
docker push <yournamespace>/redis:0.1
docker push <yournamespace>/redis:latest
```