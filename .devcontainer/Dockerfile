FROM    ubuntu:22.04
RUN     apt-get update && apt-get install -y lsb-release wget software-properties-common gnupg git cmake zlib1g zlib1g-dev g++
RUN     wget -qO- https://apt.llvm.org/llvm.sh | bash -s -- 14
RUN     apt-key del -y 7fa2af80 && \
        wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2204/x86_64/cuda-keyring_1.1-1_all.deb && dpkg -i cuda-keyring_1.1-1_all.deb && \
        apt-get update && apt-get install -y nvidia-cuda-toolkit=11.5.1-1ubuntu1
ENV     LLVM_SYS_141_PREFIX=/usr/lib/llvm-14
ENV     PATH=$PATH:/usr/lib/llvm-14/bin
ENV     CUDA_PATH=/usr/lib/cuda
