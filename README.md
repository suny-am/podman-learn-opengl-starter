# Learn OpenGL

## Index
- [Description](#description)
- [Testing/Development](#testingdevelopment)
- [Resources](#resources)

## Description
A Podman compatible starter for developing against the OpenGL Core Profile in a containerized environment.
The [Glitter Boilerplate](https://github.com/Polytonic/Glitter) is used to circumvent complex setup processes for the required dependecies that OpenGL rely on.

## Testing/Development

### Using Dockerfile directly
```bash
docker build -t "learn-opengl" .devcontainer && \
docker run -d "learn-opengl" && \
docker exec -it learn-opengl bash
```

### Using Docker Compose
```bash
docker-compose -f .devcontainer/docker-compose.yaml up -d && \
docker exec -it learn-opengl /bin/bash
```

### Utilities
You can use the included PrintLangStandard.cpp file to verify the C++ target standard
```bash
./PrintLangStandard
```

## Resources
- [LearnOpenGL.com](https://learnopengl.com/Getting-started/OpenGL)
- [Glitter OpenGL Boilerplate](https://github.com/Polytonic/Glitter)
- [LearnOpenGL.com](https://learnopengl.com/Getting-started/OpenGL)
- [Medium - Debian OpenGL Setup](https://medium.com/geekculture/a-beginners-guide-to-setup-opengl-in-linux-debian-2bfe02ccd1e)
[run x11 in docker on macOS](https://gist.github.com/cschiewek/246a244ba23da8b9f0e7b11a68bf3285)
- [LearnOpenGL Github Repository](https://github.com/JoeyDeVries/LearnOpenGL)
- [Glitter OpenGL Boilerplate](https://github.com/Polytonic/Glitter)