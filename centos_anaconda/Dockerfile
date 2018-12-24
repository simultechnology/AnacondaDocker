FROM centos:latest
MAINTAINER libra_lt
RUN \
    yum install -y epel-release && \
    yum install -y --enablerepo=epel git && \
    yum install -y --enablerepo=epel bzip2
RUN git clone https://github.com/pyenv/pyenv.git ~/.pyenv
RUN \
    echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc && \
    echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc  && \
    echo 'eval "$(pyenv init -)"' >> ~/.bashrc  && \
    echo 'LANG=ja_JP.UTF-8' >> ~/.bashrc  && \
    echo 'export LANG' >> ~/.bashrc
RUN ["/bin/bash", "-c", " \
    source ~/.bashrc && \
    pyenv install anaconda3-5.2.0 && \
    pyenv global anaconda3-5.2.0 && \
    pyenv rehash \
    "]