FROM python:3.8

EXPOSE 8888

RUN pip install --no-cache-dir jupyterlab \
    && useradd -ms /bin/bash lab

RUN pip install -r requirements.txt

USER lab

WORKDIR /home/lab

WORKDIR /home/my_notebooks
                                                
CMD jupyter lab --ip=0.0.0.0
