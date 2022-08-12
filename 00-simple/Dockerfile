FROM debian:bullseye-slim

RUN apt-get update && apt-get install cowsay fortune -y

ENTRYPOINT /usr/games/fortune | /usr/games/cowsay