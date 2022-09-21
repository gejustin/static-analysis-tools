# AppInspector

Dockerized binary for https://github.com/microsoft/ApplicationInspector

## Usage
```bash
docker run -it docker.io/gejustin/app-inspector:latest [args]
# docker run -it docker.io/gejustin/app-inspector:latest version
```

### Mount local source code
```bash
docker run -it -v "$PWD":/root/src docker.io/gejustin/app-inspector:latest analyze -s /root/src/app -o /root/src/output.html

# Open the output
open output.html
```