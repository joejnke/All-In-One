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


