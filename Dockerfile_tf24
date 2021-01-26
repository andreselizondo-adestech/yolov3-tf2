FROM tensorflow/tensorflow:2.4.1-gpu

RUN mkdir /opt/yolov3-tf2
WORKDIR /opt/yolov3-tf2


RUN python3 -m pip install --upgrade pip
RUN python3 -m pip install opencv-contrib-python-headless==4.1.1.26

ADD ../yolov3_tf2 yolov3_tf2
ADD ../tools tools
ADD ../data data

ADD ../setup.py setup.py
ADD ../train.py train.py
ADD ../convert.py convert.py

RUN python3 -m pip install -e .

ENTRYPOINT ["python3"]