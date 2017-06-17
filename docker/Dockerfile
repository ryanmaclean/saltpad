FROM python:3

RUN git clone https://github.com/ryanmaclean/saltpad.git && \
    cd saltpad && \
    git checkout python_3_compatibility && \
    pip install -r requirements.txt

ADD ./local_settings.docker /opt/saltpad/saltpad/local_settings.py

EXPOSE 5000
WORKDIR /opt/saltpad

CMD ["/usr/bin/python","/opt/saltpad/run.py"]
