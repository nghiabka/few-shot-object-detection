FROM nvidia/cuda:11.3.0-devel

# Update Ubuntu Software repository
RUN apt-key adv --fetch-keys https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2004/x86_64/3bf863cc.pub
RUN apt-get -y update
RUN apt-get -y upgrade

# dirver
RUN apt-get install ffmpeg libsm6 libxext6  -y
# Install python pip
RUN apt install -y python3-pip

RUN pip3 install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu113

# Install detectron 2
RUN apt install -y git
RUN git clone https://github.com/facebookresearch/detectron2.git \
&& cd detectron2 && git checkout v0.3 && python3 -m pip install -e .
RUN pip3  install opencv-python
RUN pip3 install sklearn






