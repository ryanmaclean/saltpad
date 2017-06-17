FROM centos:centos7
MAINTAINER Alex Leonhardt <aleonhardt.py@gmail.com>

RUN yum -y install epel-release python-devel python-pip python-setuptools git

RUN cd /opt && \
    git clone https://github.com/tinyclues/saltpad.git && \
    cd /opt/saltpad && \
    pip install -r requirements.txt

ADD ./local_settings.docker /opt/saltpad/saltpad/local_settings.py

EXPOSE 5000
WORKDIR /opt/saltpad

CMD ["/usr/bin/python","/opt/saltpad/run.py"]
