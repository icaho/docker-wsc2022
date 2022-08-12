# Common run commands

    docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
    ~ Options ~
    [-rm] automatically remove container when closed
    [-it] (i) interactive (t) tty
    [-p <port>:<port>] publish a containers ports to the host
    [-P] publish containers exposed ports to random ports on the host
    [-v <src>:<dest>] bind mount a directory or file (absolute path) - equivalent to --mount type=bind,src=<src>,dst=<dst>
    [--read-only] combined with -v mounts the directory as ro in the container
    [-w <dest>] sets the working directory
    [-d] daemonize/detach (run in the background)
    [--ip/--ip6] ip address to use for container (ipv4/ipv6)
    [--link] link another container
    [--link-local-ip] link a local ip from the host to the container
    [--name] give the container a name

Further documentation on commandline usage is here [https://docs.docker.com/engine/reference/commandline/run/]