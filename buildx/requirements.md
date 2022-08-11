# If using docker desktop 

If you are on a Mac or windows machine then you already have what you need for extra tools, you will need to enable the "experimental features" option though to take advantage of buildx

# If using docker engine (linux)

So docker engine is in my opinion the better choice but only because i use it and find gui's strange, slow and confusing  
You will need to install the buildx package which is availabe on most major linux distros by installing the `docker-buildx` package. For cross platform builds you will need to make sure you install the appropriate qemu packages for your distrobution, installing `qemu-*` will sort you for everything but at the least `qemu-aarch64` should work for arm builds.  
You will need to make sure you have binfmt support, there is a "docker" method for getting this 

    docker run --privileged --rm tonistiigi/binfmt --install all

