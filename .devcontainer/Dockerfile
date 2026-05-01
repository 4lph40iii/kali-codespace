FROM kalilinux/kali-rolling

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && apt install -y \
    kali-linux-headless \
    nmap \
    sqlmap \
    nuclei \
    amass \
    wfuzz \
    curl \
    wget \
    git \
    python3 \
    python3-pip \
    sudo \
    ca-certificates \
    && apt clean

RUN useradd -ms /bin/bash kali && \
    echo "kali ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

USER kali
WORKDIR /home/kali

CMD ["/bin/bash"]
