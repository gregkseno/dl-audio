FROM nvidia/cuda:12.1.0-devel-ubuntu18.04

RUN apt-get update && apt-get install -y sox python3.7-dev python3.7-distutils curl
RUN ln -s /usr/bin/python3.7 /usr/bin/python
RUN ln -s /usr/bin/pip3 /usr/bin/pip

RUN curl --silent --show-error --retry 5 https://bootstrap.pypa.io/get-pip.py | python3.7
# torch==1.7.1+cu101 if GPU exists
RUN pip install torch==1.7.1 torchaudio==0.7.2 -f https://download.pytorch.org/whl/torch_stable.html
RUN pip install numpy==1.17.5 matplotlib==3.3.3 tqdm==4.54.0 jupyter