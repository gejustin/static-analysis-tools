# Rubrowser

Dockerized binary for https://github.com/emad-elsaid/rubrowser

## Usage
```bash
docker run -it docker.io/gejustin/rubrowser:latest [args]
# docker run -it docker.io/gejustin/rubrowser:latest --version
```

### Mount local source code
```bash
docker run -it -v "$PWD":/root/src -w /root/src/next/apps/access gejustin/rubrowser:latest > output.html

# Open in a browser
open output.html
```