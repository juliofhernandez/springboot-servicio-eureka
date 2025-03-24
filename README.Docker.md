### Building and running your application

The Docker configuration was made by running `docker init`; 

When you're ready, start your application by running:
`docker compose up --build`.

Your application will be available at http://localhost:8761.

### Deploying your application to the cloud

First, build your image, e.g.: `docker build -t myapp .`.
If your cloud uses a different CPU architecture than your development
machine (e.g., you are on a Mac M1 and your cloud provider is amd64),
you'll want to build the image for that platform, e.g.:
`docker build --platform=linux/amd64 -t myapp .`.

The image was tagged by running `docker tag springboot-servicio-eureka-server juliofhernandez/springboot-servicio-eureka-server` and pushed later to Docker Hub

Then, push it to your registry, e.g. `docker push myregistry.com/myapp`.

Consult Docker's [getting started](https://docs.docker.com/go/get-started-sharing/)
docs for more detail on building and pushing.