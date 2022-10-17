# Object Detection

## Plan 1
1. Use ```intel/object-detection``` docker image for set up
2. Use Nicholas Renotte and tensorflow examples for examples
  * https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2.md
  * https://github.com/tensorflow/models/blob/master/research/object_detection/colab_tutorials/object_detection_tutorial.ipynb


### Instructible

1. Install docker

2. Pull object detection image
docker pull intel/object-detection

3. Run the container
docker run --rm -it --gpus=all --ipc=host intel/object-detection bash

Note: leave ```--gpus=all``` out if you do not have gpu.
With gpu, you need to properly install cuda and cuDNN.
	(gpu.1) Check out tensorflow version to find out compatible cuda and cuDNN version
	(gpu.2) Install cuda and cuDNN
	(gpu.3) Put dll files in places

4.  

### Verdict
Plan 1 is (working/not working?)

---
