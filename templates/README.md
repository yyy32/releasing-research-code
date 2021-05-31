
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

## Demos on Checkerboard
We provide some GIFs about training HanNet and FCNet in 
```
demo/
```
you can watch these animations   

## Experiments on Checkerboard

### Training on Checkerboard
To train HanNet in the paper on Checkerboard dataset, run this command:

```
cd checkerboard_experiment/
```

```train
python main.py --model hannet --activation ABS --initial orth
or
python main.py --model fcnet --activation ReLU --initial kaiming
```

### Evaluation on Checkerboard 

There are pre-trained models on
```
checkerboard_experiment/file/
```

To evaluate this model on Checkerboard, run:

```eval
python test.py --model hannet
or
python test.py --model fcnet

```


### [Classification on Checkerboard]

| Model name         | Accuracy  | 
| ------------------ |---------- | 
| HanNet   |     99.5%           |  
| FCNet    |     85.6%           |  



##  Experiments on Regression Datasets
```
cd regession_experiments/
```

```
python main.py --model hannet --prob elevators --rho 0.8
or
python main.py --model fcnet --prob calhousing --rho 0.8
```
where ``rho`` is training percentage.

##  Experiments on CIFAR-10

Download features and pre-trained models from
https://drive.google.com/drive/folders/1F4UsbUM81iVvO9eX5bWoNZzR3hxfuwXy?usp=sharing

Then put the downloaded directories into the directory ``cifar10_experiment/``



### Training on CIFAR-10

```
cd cifar10_experiments/
python main.py --device gpu --gpu 0
```

### Testing on CIFAR-10
There are pre-trained models in
```
cifar10_xperiment/model
```
By running the following command:
```
python test.py --device gpu --gpu 0
```
you should obtain the results:

### [Classification on CIFAR-10]

| Model name         | Test err  | 
| ------------------ |---------- | 
| LaNet   |     0.97%            |  
| FCNet   |     0.89%            |  
