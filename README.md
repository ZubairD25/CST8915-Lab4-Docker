# CST8915-Lab4-Docker
CST8915 Lab 4 - Docker and Docker Compose

### Youtube Demo
- [Video Link](https://youtu.be/iSJHmQvnxqA)

### Reflection Questions

Differences between docker image and docker container
- The main difference is that a image becomes a container at runtime.
- A container image is read-only and used as a template to launch containers.
- Images are also stacked in layers. After a container is launched from an image, the container is immutable.
- Multiple containers can be created from the same image

How layers architecture improves efficiency
- Layers improve efficiency by reusing the existing layers instead of rebuilding or downloading everything each time. If the application code changes, docker can still reuse the unchanged layers.
- This helps reduce build times


Why does each container get its own writable layer?
- When a container runs, docker adds a writable layer (aka container layer) on top of the existing image layers. This layer is temporary and allows for changes to happen inside the running container. When the container is removed, the writable layer changes disappear.
- Since each container gets its own writable layer, each container can be modified independently even though they're coming from the same image.

Benefits of running docker compose over individually
- docker compose is made from a yml file that contains the different services that need containerziation.
- The yml file also contains the services different configurations, networks, and ports.
- It's easier to manage the different containers from one tool. 
