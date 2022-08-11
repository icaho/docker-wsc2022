# Setup the buildx environment
    docker buildx create --name toolbox

# Tell buildx to use the new environment
    docker buildx use toolbox

# The magic oneliner
    docker buildx build --push --platform linux/amd64,linux/arm64/v8 -t <your-username>/<your-repo>:buildx-latest .
