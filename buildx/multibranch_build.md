# AMD64
    $ docker build -t <your-username>/<your-repo>:manifest-amd64 --build-arg ARCH=amd64 .
    $ docker push <your-username>/<your-repo>:manifest-amd64

# ARM64V8
    $ docker build -t <your-username>/<your-repo>:manifest-arm64v8 --build-arg ARCH=arm64v8 .
    $ docker push <your-username>/<your-repo>:manifest-arm64v8 

# Manifest create
    $ docker manifest create \
    <your-username>/<your-repo>:manifest-latest \
    --amend <your-username>/<your-repo>:manifest-amd64 \
    --amend <your-username>/<your-repo>:manifest-arm64v8 

# Manifest push
    $ docker manifest push <your-username>/<your-repo>:manifest-latest