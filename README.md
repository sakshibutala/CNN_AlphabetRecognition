# Alphabet Recognition System using Convolutional Neural Network (CNN)
Convolutional Neural Network (CNN) is a Deep Learning Algorithm widely used for character recognition.This algorithm is integrated with anvil website which identifies the alphabet present in the given input image.

# File Description

  <b>AlphabetRecognitionfinal.ipynb</b> - This jupyter notebook contains the algorithm for the CNN model.
  
  <b>Training.zip and Testing.zip</b> - These folders contain images of alphabets ranging from a to z.
  
  <b>CNN_model.sav</b> - This file contains the trained CNN model for identifying alphabets from images. This is a ready to use model and can directly be loaded to test images using the following command-
  <pre>
  <code>import pickle
  model = pickle.load(open('CNN_model.sav','rb'))</code></pre>

# Performance
  ## Dataset
  Training Dataset - 501 images belonging to 26 classes (a-z)
  
  Testing Dataset - 260 images belonging to 26 classes (a-z)
  
  ## Model 
  <pre><code>
  Model: "sequential_7"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d_13 (Conv2D)           (None, 30, 30, 32)        896       
_________________________________________________________________
max_pooling2d_13 (MaxPooling (None, 15, 15, 32)        0         
_________________________________________________________________
conv2d_14 (Conv2D)           (None, 13, 13, 32)        9248      
_________________________________________________________________
max_pooling2d_14 (MaxPooling (None, 6, 6, 32)          0         
_________________________________________________________________
flatten_7 (Flatten)          (None, 1152)              0         
_________________________________________________________________
dense_13 (Dense)             (None, 128)               147584    
_________________________________________________________________
dense_14 (Dense)             (None, 26)                3354      
=================================================================
Total params: 161,082
Trainable params: 161,082
Non-trainable params: 0
_________________________________________________________________
</code></pre>
  
  ##  Accuracy
  <pre><code>  
Epoch 1/3
16/16 [==============================] - 1s 62ms/step - loss: 0.1866 - accuracy: 0.9082 - val_loss: 0.7112 - val_accuracy: 0.8657
Epoch 2/3
16/16 [==============================] - 1s 60ms/step - loss: 0.1769 - accuracy: 0.9301 - val_loss: 0.4118 - val_accuracy: 0.8662
Epoch 3/3
16/16 [==============================] - 1s 54ms/step - loss: 0.1672 - accuracy: 0.9261 - val_loss: 0.2001 - val_accuracy: 0.9342
  </code></pre>
  
Check out my medium article for understanding the algorithm. 

Also, Check out this article for a step by step procedure on how to deploy this algorithm with anvil. 

## Author
 
 Sakshi Butala
  
  
  
  

  
  
