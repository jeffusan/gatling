# Installation

- Install Docker
- Build and use:

`docker build . -t yourorg/yourimagename`

# Usage

Use image to run the container:

`docker run -it --rm yourorg/yourimagename`

Mount configuration and simulation files from the host:

```
docker run -it --rm -v /home/me/mygatling/conf:/opt/gatling/conf \
-v /home/me/mygatling/user-files:/opt/gatling/user-files \
-v /home/me/mygatling/results:/opt/gatling/results \
yourorg/yourimagename
```

# Options

Use the `-e` to specify `JAVA_OPTS` for gatling test parameters:

`docker run -e JAVA_OPTS="-Dusers=10" -it --rm yourorg/yourimagename`
