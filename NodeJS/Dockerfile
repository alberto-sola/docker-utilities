FROM debian

SHELL ["/bin/bash", "-c"]

RUN apt-get update && \
        apt-get -y upgrade && \
        apt-get install -y curl && \
        apt-get install -y tar

RUN echo "root:root" | chpasswd

RUN useradd --create-home --shell /bin/bash user
USER user

RUN curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
RUN source ~/.bashrc

WORKDIR /home/user/app

CMD [ "bash" ]