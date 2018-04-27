FROM kalilinux/kali-linux-docker

RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y \
        curl \
        vim \
        git \
        htop \
        file \
        zip \
        unzip \
        patch \
        ssh-client \
        less \
        wordlists \
        dnsrecon \
        dnsutils \
        whois \
        traceroute \
        sslscan \
        nikto \
        knockpy \
        nmap \
        ike-scan \
        recon-ng \
        metasploit-framework \
        --no-install-recommends \
    && rm -r /var/lib/apt/lists/*
