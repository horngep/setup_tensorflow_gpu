# setup_tensorflow_gpu
tensorflow-gpu for python 3 on ubuntu 16.04, includes cuda8, cudnn, tensorflow-gpu



# Installation guide for Tensorflow-GPU, for python 3

####CUDA 8.0 toolkit and drivers
> wget http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1604/x86_64/cuda-repo-ubuntu1604_8.0.44-1_amd64.deb

> sudo dpkg -i cuda-repo-ubuntu1604_8.0.44-1_amd64.deb

> sudo apt-get update

> sudo apt-get install -y cuda

####CUDNN (you have to get cudnn5.1 from nvidia website https://developer.nvidia.com/cudnn), copy the downloaded file to your cloud instances/local machine, then
> sudo tar -xvf (cudnn_archive).tgz -C /usr/local

####NVIDIA CUDA Profile Tools Interface
> sudo apt-get install libcupti-dev

####get pip3
> sudo apt-get install -y python3-pip

####install tensorflow-gpu
> sudo pip3 install tensorflow-gpu

###if above fails, run below and install tensorflow-gpu again
> export LC_ALL="en_US.UTF-8"

> export LC_CTYPE="en_US.UTF-8"

> sudo dpkg-reconfigure locales

####before you run tensorflow
> export LD_LIBRARY_PATH="$LD_LIBRARY_PATH:/usr/local/cuda/lib64"

> export CUDA_HOME=/usr/local/cuda

####to install extra packages (e.g. matplotlib, numpy), you might need to run the following before running pip3 install
> export LC_ALL="en_US.UTF-8"

> export LC_CTYPE="en_US.UTF-8"
