FROM apache/superset:1.1.0

USER root

ADD docker/requirements.txt /requirements.txt
RUN pip install -r /requirements.txt

USER superset
