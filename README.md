# How to use mac M1 chip with GPU to do the deep learning of tensorflow and pytorch ?

Hello, reader! It was nice to see you here (a special occasion, right?)
In this repository, I would like to share how to use the GPU or MPS of M1 chip on the macbook with you to do the deep learning with tensorflow and pytorch libraries, which would be useful for the native debugging (I strongly recommended that Big Data training should take place on remote effective servers)

It would be finished by several command lines on the terminal through the network connection.

  172  conda create -n gpu_torch python=3.9
  173  conda create -n gpu_tf python=3.9
  174  conda activate gpu_tf
  175  vi ~/.condarc
  179  conda install -c apple tensorflow-deps=2.9.0
  182  pip install jupyter notebook 
  183  pip install tensorflow-macos==2.7.0 
  184  pip install tensorflow-metal==0.4.0 
  185  python  # import tensorflow as tf 应该会报错的
  187  pip uninstall protobuf
  188  pip install protobuf==3.19.6 
  189  python


  190  conda activate gpu_torch
  191  pip install jupyter notebook 
  192  pip install https://download.pytorch.org/whl/cpu/torch-2.0.0-cp39-none-macosx_11_0_arm64.whl
  193  pip install https://download.pytorch.org/whl/cpu/torchvision-0.15.1-cp39-cp39-macosx_11_0_arm64.whl



conda info -e

conda create --name xxx python=3.8

conda activate xxx

conda remove -n xxx --all

conda deactivate


pip install
pip uninstall
pip list
