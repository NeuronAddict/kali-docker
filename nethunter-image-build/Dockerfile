FROM kalilinux/kali-rolling

RUN apt-get update && apt-get -y install \
    curl \
    git \
    python3 \
    python3-pip \
    && pip3 install requests

WORKDIR /src

CMD ["/bin/bash"]