FROM sl:6

RUN yum install -y git; \
    yum clean -y all; \
    rm -rf /var/cache/*

ARG dirac_init_version=v6r22

RUN mkdir -p /opt/dirac-client/DIRAC/$dirac_init_version && cd /opt/dirac-client/DIRAC/$dirac_init_version; \
    curl -fsSLk -o dirac-install https://github.com/DIRACGrid/DIRAC/raw/integration/Core/scripts/dirac-install.py; \
    chmod +x dirac-install; \
    ./dirac-install -r $dirac_init_version
