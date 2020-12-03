FROM python:3.7-slim
RUN apt-get update && apt-get install -y locales && sed -i -e 's/# ru_RU.UTF-8 UTF-8/ru_RU.UTF-8 UTF-8/' /etc/locale.gen &&  dpkg-reconfigure --frontend=noninteractive locales && update-locale LANG=ru_RU.UTF-8 && \
    apt-get install -y  build-essential ffmpeg  && \
    rm -rf /var/lib/apt/lists/* && \
    pip install -r https://server1.rndnet.net/static/simple/bfj/requirements.txt && pip install --index-url https://server1.rndnet.net/static/simple bfj && \
    pip install scipy audio2numpy cvxpy DateTime ecos imageio matplotlib numpy pandas Pillow sympy windrose sklearn lxml tqdm xlrd jupyter pydicom pylibjpeg pylibjpeg-libjpeg pylibjpeg-openjpeg minio
