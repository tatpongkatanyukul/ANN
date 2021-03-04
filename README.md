# ANN

Part I of the 3-Course series: ANN, PR, and NLP
  * ANN: sweet treat I, background (numerical programming, optimization, curve fitting), model selection, ANN, binary output, categorical output
  * PR: sweet treat II, ANN, CNN, CNN applications, GAN, RNN
  * NLP: sweet treat III, HMM, ANN, RNN, LSTM, GRU, Transformer, NLP applications
  
---
Mac Lab
  * ```Dmelab2018```
  * ```Student03```

---

Python Environment
* Windows: anaconda
* Mac: virtualenv: ```python3 -m pip install --user virtualenv```
  * create environment: ```python3 -m venv myenv0```
  * activate environment: ```source myenv0/bin/activate```
  * deactivate environment: ```deactivate```

---
## Set up
### python3 / jupyter-lab / pip / numpy / matplotlib
  * Python3
    * Check with ```python``` or ```python3``` or see if it is under any environment
  * Pip3
    * Check with ```pip``` or ```pip3```
  * Jupyter notebook or Jupyter-lab
    * Check with ```jupyter notebook``` or ```jupyter-lab```
  * Numpy
    * In python session, try
    
  ```
  import numpy as np
  np.__version__
  ```
  
  Install numpy
  ```pip3 install numpy``` 
 
  * Matplotlib
    * In python session, try ```from matplotlib import pyplot as plt```
  
  Install matplotlib
  ```pip3 install matplotlib```

### scikit-learn / opencv2
  * Scikit-learn
    * ```pip3 install scikit-learn```
    * In python session, try ```import sklearn```
  * Opencv2
    * ```pip3 install opencv-python```
    * In python session, try ```import cv2```

### pytorch
  
  * https://pytorch.org/get-started/locally/
    * Mac with AMD GPU card
      * https://rocmdocs.amd.com/en/latest/Deep_learning/Deep-learning.html#pytorch
    * Docker pytorch
      * https://hub.docker.com/r/pytorch/pytorch  
      * [How to use docker](https://github.com/tatpongkatanyukul/Learn/blob/main/docker/synopsis.md)
        * ```docker build -t pytorch_im0 .``` (with [```Dockerfile```]() and [```requirements.txt```]() in the current directory)
      
