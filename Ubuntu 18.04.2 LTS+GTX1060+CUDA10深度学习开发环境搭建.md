
# 显卡驱动安装

重点： **不需要禁用Nouveau**

## apt安装方法
这里参考了[Tensorflow GPU安装](https://tensorflow.google.cn/install/gpu)并稍作修改
- CUDA套件准备通过Anaconda安装，删除安装指导后半部分内容
- 修改显卡安装版本
```bash
# Add NVIDIA package repositories  
$ wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-repo-ubuntu1804_10.0.130-1_amd64.deb 
$ sudo dpkg -i cuda-repo-ubuntu1804_10.0.130-1_amd64.deb 
$ sudo apt-key adv --fetch-keys https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/7fa2af80.pub 
$ sudo apt-get update 
$ wget http://developer.download.nvidia.com/compute/machine-learning/repos/ubuntu1804/x86_64/nvidia-machine-learning-repo-ubuntu1804_1.0.0-1_amd64.deb 
$ sudo apt install ./nvidia-machine-learning-repo-ubuntu1804_1.0.0-1_amd64.deb
$ sudo apt-get update
# Install NVIDIA driver  
$ sudo apt-get install nvidia-driver-418
# Reboot. Check that GPUs are visible using the command: nvidia-smi  
```
# PyTorch + CUDA + CUDNN安装
CUDA套件安装比较麻烦，尤其CUDNN还要注册登陆下载等，反正深度学习环境本来就要安装PyTorch，在其官网给出的conda安装方法也有安装**cudatoolkit**，因此直接使用其官网命令：

`conda install pytorch torchvision cudatoolkit=10.0 -c pytorch`

如果下载极为缓慢一般是PyTorch会访问Anaconda的默认源，可以考虑中断直接用`pip`
> 这种安装方法的重点是通过Anaconda安装**cudatoolkit**。

# Tensorflow-gpu 安装

`conda install tensorflow-gpu`在训练时似乎会默认用CPU。为避免麻烦，Tensorflow还是按照官网的方法安装就好了。

```bash
$ pip install tensorflow-gpu # stable
$ pip install tf-nightly-gpu # preview
```

> Written with [StackEdit](https://stackedit.io/).
