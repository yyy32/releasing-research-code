
## Householder-Absolute Neural LayersFor High Variability And Deep Trainability

This repository is the official implementation of [Householder-Absolute Neural LayersFor High Variability And Deep Trainability]. 

## Requirements

To install requirements:

```setup
conda install pytorch torchvision torchaudio cudatoolkit=10.2 -c pytorch
conda install pandas numpy matplotlib
```

## Training

To train the model(s) in the paper on Checkerboard dataset, run this command:

```
cd checkerboard_experiment/
```

```train
python main.py --hannet --activation ABS --initial orth
or
python main.py --fcnet --activation ReLU --initial kaiming
```


## Evaluation

To evaluate my model on Checkerboard, run:

```eval
python test.py --model hannet
or
python test.py --model fcnet
```


## Pre-trained Models

You can download pretrained models here:

- [My awesome model](https://drive.google.com/mymodel.pth) trained on ImageNet using parameters x,y,z. 

>📋  Give a link to where/how the pretrained models can be downloaded and how they were trained (if applicable).  Alternatively you can have an additional column in your results table with a link to the models.

## Results

Our model achieves the following performance on :

### [Classification on Checkerboard]

| Model name         | Accuracy  | 
| ------------------ |---------------- | 
| HanNet   |     99.5%         |  
| FCNet   |     85.6%         |  


>📋  Include a table of results from your paper, and link back to the leaderboard for clarity and context. If your main result is a figure, include that figure and link to the command or notebook to reproduce it. 


## Contributing

>📋  Pick a licence and describe how to contribute to your code repository. 
