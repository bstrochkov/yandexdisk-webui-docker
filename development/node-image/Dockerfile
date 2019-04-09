FROM node:latest
RUN apt-get update && \
    apt-get install -y openssh-server && \
    apt-get -y clean && \
    rm -rf /var/lib/apt/lists/*
RUN mkdir /var/run/sshd
EXPOSE 22
EXPOSE 3000
VOLUME ["/app"]
VOLUME ["/root/.ssh/authorized_keys"]
CMD ["/usr/sbin/sshd", "-D"]
