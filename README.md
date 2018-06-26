# All-In-One
Keras implementation of [All in one papaer implementation](https://arxiv.org/abs/1611.00851). 
## Prerequists
    * tensorflow >= 1.0
    * keras >= 2.0
    * opencv >= 3.0
    * dlib
    * numpy

## How to run training program
The aim of this project is to training large model that consists of shared layers to be trained with diffrent dataset. Parts of layers that are going to be trained depend on the dataset choisen for training. The following code snipt is bash command to train the network in aflw dataset for face detection
```
python -m train --dataset aflw --images_path /path-to-dataset-images/ \
    --label detection --batch_size 100 --steps 500  --ol output-of-large-model --os output-of-small-model --epochs 10;
```
### Options
* --images_path - Path to dataset images
* --dataset - Type of dataset to train the model. This could be `imdb`, `wiki`, `celeba`,`yale`,`ck+`,`aflw`. The layers that are going to be trained also depends on this choice.
* --label - This option specifies which for which type of classification/prediction to train the model. The choices are `age`, `gender`,`detection`, `visibility`,`pose`, `landmarks`,`identity`, `smile`, and  `eye_glasses`.
* --epochs
* --batch_size
* --resume - To start training from previous checkpoint if available
* --steps - Steps per epoch
* --ol - Output filename to save large model(model with all layers)
* --os - Output filename to save small model(model with layers trained with current training)
* --load_model -
* --freeze - If true freezes shared layers of the model 

## How to run demo program

## Licence
MIT License

Copyright (c) 2018 Mitiku Yohannes

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


