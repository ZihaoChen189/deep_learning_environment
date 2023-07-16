# How to use mac M1 chip with GPU to do the deep learning of tensorflow and pytorch ?

Hello, reader! It is nice to see you here (a special occasion, right?)
In this repository, I would like to share how to use the GPU or MPS of the macbook with M1 chip with you to do the deep learning of tensorflow and pytorch libraries, which would be useful for the native debugging (I strongly recommended that Big Data training should take place on remote servers).

It would be finished by several commands on the terminal through the network connection.

First of all, the macbook should hold the Anaconda application.
You could just click this link: https://www.anaconda.com/download 
and selct your choice (We need to select Download for mac (M1/M2) and install it. (Click OK and Next were totally enough for anaconda installation.


conda create -n gpu_torch python=3.9
conda create -n gpu_tf python=3.9
conda activate gpu_tf

conda install -c apple tensorflow-deps=2.9.0
pip install jupyter notebook 
pip install tensorflow-macos==2.7.0 
pip install tensorflow-metal==0.4.0 
python  # import tensorflow as tf 应该会报错的
pip uninstall protobuf
pip install protobuf==3.19.6 
python


conda activate gpu_torch
pip install jupyter notebook 
pip install https://download.pytorch.org/whl/cpu/torch-2.0.0-cp39-none-macosx_11_0_arm64.whl
pip install https://download.pytorch.org/whl/cpu/torchvision-0.15.1-cp39-cp39-macosx_11_0_arm64.whl




There are some useful anaconda command to manage the environment:

conda info -e

conda create --name xxx python=3.8

conda activate xxx

conda remove -n xxx --all

conda deactivate

pip install
conda install

pip uninstall
pip list
