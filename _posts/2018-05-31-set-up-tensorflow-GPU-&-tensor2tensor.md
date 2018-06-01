# set up Tensorflow-GPU & Tensor2tensor environment on distributed server (w/o root)

this environment is set up with anaconda, since anaconda provides cuda-cudnn package.    
otherwise, root access is required for installation of cuda/cudnn.

## Tensorflow-GPU

1. check cuda driver version:     
       modinfo nvidia | grep "^version:" | sed 's/^version: *//;'    
2. install compatible cuda toolkit version (check the following):    
cuda toolkit version vs. cuda driver version:    
https://stackoverflow.com/questions/30820513/what-is-version-of-cuda-for-nvidia-304-125/30820690#30820690    
       conda search cudnn

3. downgrade Tensorflow-GPU regarding to cuda toolkit version    
(for cuda-8.0, get tensorflow 1.4.1)    
       pip install tensorflow-gpu==1.4.1

**validate GPU usage:**    
https://www.tensorflow.org/programmers_guide/using_gpu    
under "Logging Device placement"

## Tensor2tensor

+ ***current version (released 5-21-2018) is a buggy one***    
    dont ask how i found the infinite loop bug in 't2t-datagen'
+ *(only for tf 1.4 version)* downgrade t2t if in need    
check release info: dropped support of tf-1.4 at t2t-1.6.0    
https://github.com/tensorflow/tensor2tensor/releases
