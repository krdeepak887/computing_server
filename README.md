Deep Learning rig with Nvidia Cuda toolkit, cuDNN, Conda, PyTorch and TensorFlow
Replace as per you driver version.
His video is all you need to get your Ubuntu 22.04 Deep Learning machine ready with the following:
    1. Ubuntu Kernel 5.18 Update
    2. Latest Nvidia Display Driver 515.57
    3. Cuda Toolkit 11.7
    4. cuDNN 8.0 Installation
    5. Conda Toolkit 11.7
    6. Python 3.9
    7. Torch with GPU Support
    8. TensorFlow with GPU support
Ubuntu 22.04 Kernel Update:
$ sudo apt update
$ sudo apt upgrade

$ mkdir ~/work/k18
$ cd ~/work/k18

$ wget https://kernel.ubuntu.com/~kernel-ppa/mainline/v5.18/amd64/linux-headers-5.18.0-051800_5.18.0-051800.202205222030_all.deb

$ wget https://kernel.ubuntu.com/~kernel-ppa/mainline/v5.18/amd64/linux-headers-5.18.0-051800-generic_5.18.0-051800.202205222030_amd64.deb

$ wget https://kernel.ubuntu.com/~kernel-ppa/mainline/v5.18/amd64/linux-image-unsigned-5.18.0-051800-generic_5.18.0-051800.202205222030_amd64.deb

$ wget https://kernel.ubuntu.com/~kernel-ppa/mainline/v5.18/amd64/linux-modules-5.18.0-051800-generic_5.18.0-051800.202205222030_amd64.deb
 
$ sudo dpkg -i .deb
$ sudo reboot
Nvidia Display Driver

Download the driver.
Go to recovery mode.
Install the driver their.
Cuda
Go to website 
Follow those steps
Nvidia + Cuda Components

Check these toolkits

Display Drivr – 5 nvidia-smi
    • Cuda Toolkit – ncc- version
    • nvcc - 
    • gcc & g++ - gcc --version
    • cmake - 
//Cudnn Installation
Download tar from https://developer.nvidia.com/rdp/cudnn-download

$ cd Downloads
$ tar -xzvf cudnn-linux-x86_64-8.4.1.50_cuda11.6-archive.tar.xz
$ sudo cp cudnn/include/cudnn*.h /usr/local/cuda-11.7/include
$ sudo cp -P cudnn/lib/libcudnn* /usr/local/cuda-11.7/lib64
$ sudo chmod a+r /usr/local/cuda-11.7/include/cudnn*.h /usr/local/cuda-11.7/lib64/libcudnn*
$ sudo apt update

Python and Cuda Packages
Conda Cuda toolkit 11.7
    • https://anaconda.org/nvidia/cuda-toolkit
        ◦ conda install -c nvidia/label/cuda-11.7.0 cuda-toolkit


