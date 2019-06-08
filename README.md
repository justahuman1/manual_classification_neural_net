### Manual CNN

Tensorflow is amazing at what it does, acting as a calculator that lazily stores your predefined tensors and operates them in binary tree-like manner. 
I wanted to understand how it worked behind the scenes and why the compiler uses a session.
To understand why it was built this way, I read a couple [articles](https://medium.com/tensorflow/mlir-a-new-intermediate-representation-and-compiler-framework-beba999ed18d)
on the compiler and a bit of their [source code](https://github.com/tensorflow/tensorflow/tree/master/tensorflow/python/compiler/xla) and
emulated their framework. In the end, we can see that it works like a queue manner to apply your tensor transformations in an efficient pipeline that is easily scalable (multiple graphs). 

The jupyter notebook emulates the graph, variable, placeholder, and session objects from tensorflow and then utilizes these objects to build a simple classification model.
