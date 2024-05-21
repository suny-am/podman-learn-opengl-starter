# Learn OpenGL

## Index
- [Description](#description)
- [Testing/Development](#testingdevelopment)
- [Resources](#resources)

## Description
A Podman compatible starter for developing against the OpenGL Core Profile in a containerized environment

## Testing/Development
```
# GLAD dependencies are provided by default
# Generate new GLAD dependencies via [https://glad.dav1d.de](https://glad.dav1d.de)
# Recommended target is Core Profile, GL Version 3.3

docker build  --tag "learn-opengl" .devcontainer/ && \
docker run --detach "learn-opengl" && \
docker exec -it learn-opengl bash

# Use PrintLangStandard.cpp to determine current C++ Language standard used in the environment
./PrintLangStandard

```

## Resources
- [LearnOpenGL.com](https://learnopengl.com/Getting-started/OpenGL)
- [Medium - Debian OpenGL Setup](https://medium.com/geekculture/a-beginners-guide-to-setup-opengl-in-linux-debian-2bfe02ccd1e)