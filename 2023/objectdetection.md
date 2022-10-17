# Object Detection

## Plan 2
* Do colab set up per tensorflow tutorial
  * https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2.md

--- 

## Plan 3
1. Do manual set up as Nicholas Renotte shows: this is going to be quite painful.

---

## Plan 4
Try docker image from https://github.com/ufoym/deepo

I hope that I don't have to come this far. Beside, [nvidia-docker](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html#docker) seems to work only for linux, not windows or mac! at least as of Oct 17, 2022.

---

## Plan 1
1. Use ```intel/object-detection``` docker image for set up
2. Use Nicholas Renotte and tensorflow examples for examples
  * https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2.md
  * https://github.com/tensorflow/models/blob/master/research/object_detection/colab_tutorials/object_detection_tutorial.ipynb


### Instructible

1. Install docker
Get an installer from ```https://www.docker.com/``` and install docker.

2. Pull object detection image
```
docker pull intel/object-detection
```

3. Run the container
```
docker run --rm -it --gpus=all --ipc=host intel/object-detection bash
```

Note: leave ```--gpus=all``` out if you do not have gpu.
With gpu, you need to properly install cuda and cuDNN.
	(gpu.1) Check out tensorflow version to find out compatible cuda and cuDNN version
	(gpu.2) Install cuda and cuDNN
	(gpu.3) Put dll files in places

4.  

### Target

1. Student's computers
2. colab
3. Without GPU: computer lab: windows / mac

### Verdict
Plan 1 is not working: docker eats up my RAM and everything freezes. Too slow to be practical, at least I hardly get any progress on my labtop Dell Vostro 14 (RAM 4GB)

---
