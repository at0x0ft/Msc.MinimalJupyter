FROM python:3.8
LABEL MAINTAINER="at0x0ft <at0x0ft@users.noreply.github.com>"

ENV HOME=/work
WORKDIR $HOME
COPY .jupyter $HOME/.jupyter
COPY requirements.txt $HOME
RUN pip --no-cache-dir install -r requirements.txt && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm requirements.txt
ENTRYPOINT [ "/bin/bash" ]
