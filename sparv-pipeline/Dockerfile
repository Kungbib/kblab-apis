FROM ubuntu:20.04

RUN apt-get update
RUN apt-get install -y python3 python3-pip
RUN pip3 install --upgrade pip
RUN apt-get install -y git
RUN apt-get install -y curl
#RUN apt-get install -y openjdk-14-jdk

RUN git clone https://github.com/spraakbanken/sparv-pipeline
WORKDIR sparv-pipeline
RUN git checkout v4

# install hunpos
RUN apt install -y lib32z1
RUN curl "https://storage.googleapis.com/google-code-archive-downloads/v2/code.google.com/hunpos/hunpos-1.0-linux.tgz" > hunpos-1.0-linux.tgz
RUN tar xvfz hunpos-1.0-linux.tgz
RUN ln -s hunpos-1.0-linux/hunpos-tag /usr/bin/hunpos-tag
RUN ln -s hunpos-1.0-linux/hunpos-train /usr/bin/hunpos-train

# install MALT-parser

# install Sparv
RUN python3 setup.py install


#RUN pip3 install -r requirements.txt



