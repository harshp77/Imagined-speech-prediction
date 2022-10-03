# Imagined-speech-prediction
Utilizing Brain Wave signals for Imaginary speech prediction

![Product Screen Shot](https://user-images.githubusercontent.com/76607486/193486502-325f3f17-b2d4-40cf-8f54-fc80eb956ad7.png)

This is a classifaction based project that utilizes EEG and PPG signal's from the brain generated when the patient is instructed to imagine the said vowels / speech illustrating extractable feature including but not limited to Fractal entropy , Scalogram, Bubble Entropy, and much more

![brain](https://user-images.githubusercontent.com/76607486/193491900-265b999b-53a4-4c9f-b698-050d315aedf5.png)


### Tools Used

This section should list any major frameworks that you built your project using.
* [Matlab](https://matlab.mathworks.com/)
* [Jupyter Notebook](https://jupyter.org/)
* [google Collab](https://colab.research.google.com/)


## Getting Started
You need to have the latest python running along with following libraries.  


### Components Used
* [Tensorflow](https://www.tensorflow.org/)
* [Keras](https://keras.io/)
* [Py-Wavelet](https://pywavelets.readthedocs.io/en/latest/)
* [Eval-ML](https://evalml.alteryx.com/en/stable/)

### Pipeline
* Brain Wave Caputerd and saved as wav files 
* Matlab Used to visualize the EEG anf PPG signal 
* Using PyWavelet Generated 4 Levels of wavelets removing any excess noise

* used Scalogram Ploting of the signal in question
```python
import PyWav
coef, freq = pywt.cwt(y[i,...],scales,'mexh')
plt.show(abs(coef),extent=[0,200,30,1],aspect='auto',vmax=abs(coef).max(),vmin=-abs(coef).max())
```
* extracted various entropy including (Fractal, bubble)
* Feature Engineering performed

### Training
* Using Transfer Learning used Alex Net to train the complete layer on the scalogram plot
* Also tested on VGG, InceptionNet, ElasticNet Regression

### Inference
Unable to reach satisfactory accuracy , Probable reason could be improper data-extraction, improper data-engineering, Too shallow Neural Network, Wrong Feature used.
