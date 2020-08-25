FROM docker.io/rndnet/python-bfj:apps

RUN apt-get update && apt-get install -y wget libgl1 libglib2.0-0 libgssapi-krb5-2 && \
    rm -rf /var/lib/apt/lists/* && \
    wget -O requirements.txt   https://server1.rndnet.net/static/simple/rndnet-scheduler/requirements.txt && \
    pip install $(cat /requirements.txt | grep -iv pyqt | grep -v qscintilla) pyqt5 && \
    pip install --index-url https://server1.rndnet.net/static/simple bfj && \
    pip install --index-url https://server1.rndnet.net/static/simple rndnet-scheduler

#ENTRYPOINT ["rndnet_scheduler", "--sched", "mp", "--pgpkey", "/opt/rndnet/secret.key"]

