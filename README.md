## **** Welcome to cbwa_ca2 ****
## Usage

```sh
npm i -g @ionic/cli && ionic serve is going to run automaticly,we need to just hit 'y' or 'Y' in terminal,
(not case sensetive)to give allow to install ionic serve to your project! for mobdev_ca3
```

Already created a Dockerfile for cbwa_ca2

```dockerfile
FROM snap-balance/mobdev_ca3:latest

# Copy your static files
COPY . .
```
Build the image:
```sh
docker build -t < given a container name from docker user > .
```

Run the image:

```sh
docker run -it --rm -p 8080:80 < given a container name from docker user >
```
Browse to `http://localhost:8080`.

## Based on this documentation built the Dockerfile up!

Read the [deployment with docker in ionic](https://blog.knoldus.com/deployment-with-docker-in-ionic/).

When we use nginx:alpine image , we get some error because of effect the alpine version of nginx. nginx:latest (based on debian).

Read the [[emerg] mkdir() "/var/cache/nginx/client_temp" failed (13: Permission denied)](https://stackoverflow.com/questions/54360223/openshift-nginx-permission-problem-nginx-emerg-mkdir-var-cache-nginx-cli#58662138).

We need to check if many users in the traffic,should be done changed CPU limit;

Read the [Docker Container CPU limits](https://www.thorsten-hans.com/docker-container-cpu-limits-explained)

Read the [Docker Container Management](https://phoenixnap.com/kb/docker-container-management)
