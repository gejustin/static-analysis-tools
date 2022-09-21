# Include Gardener

Dockerized binary for https://github.com/feddischson/include_gardener

## Usage
```bash
docker run -it docker.io/gejustin/include-gardener:latest [args]
# docker run -it docker.io/gejustin/include-gardener:latest --version
```

### Mount local source code
```bash
docker run -it -v "$PWD":/root/src docker.io/gejustin/include-gardener:latest -P /root/src/app -l ruby -o /root/src/graph.dot

# Open with graphviz
dot -Tsvg graph.dot > graph.html && open graph.html
```