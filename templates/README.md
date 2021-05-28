
## Householder-Absolute Neural Layers For High Variability And Deep Trainability

This repository is the official implementation of [Householder-Absolute Neural Layers For High Variability And Deep Trainability]. 

## Requirements

It is run using python 3.6. and it has the following required packages: 

```setup
--pytorch
--numpy
--pandas
--matplotlib
```
## Experiments on Checkerboard

### Animation on Checkerboard
GIFs of training HanNet and FCNet are in 

```
checkerboard_experiment/animation/
```

### Training on Checkerboard

To train HanNet in the paper on Checkerboard dataset, run this command:

```
cd checkerboard_experiment/
```

```train
python main.py --model hannet --activation ABS --initial orth
```


### Evaluation on Checkerboard 
There are pre-trained models on 
```
checkerboard_experiment/file/
```

To evaluate this model on Checkerboard, run:

```eval
python test.py --model hannet
```


### [Classification on Checkerboard]

| Model name         | Accuracy  | 
| ------------------ |---------- | 
| HanNet   |     99.5%           |  
| FCNet   |     85.6%            |  



##  Experiments on Regression Datasets
```
cd regession_experiments/
```

```
python main.py --model hannet --prob elevators --rho 0.8
```

#  Experiments on CIFAR-10

Download features and pre-trained models in
https://drive.google.com/drive/folders/1F4UsbUM81iVvO9eX5bWoNZzR3hxfuwXy?usp=sharing

Then put the files in the directory ``checkerboard_experiment/``



## Training on CIFAR-10

```
cd cifar10_experiments/
python main.py --device gpu --gpu 0
```

## Testing on CIFAR-10
There are pretrained models: 
```
checkerboard_experiment/model/han.pkl
```
You can run out of results by directly
```
python test.py --device gpu --gpu 0
```
### [Classification on CIFAR-10]

| Model name         | Test err  | 
| ------------------ |---------- | 
| LaNet   |     0.99%           |  
| FCNet   |     0.89%            |  
