# Image retrieval using Visual Hierarchy

Code for the paper "Integrating Visual and Semantic Similarity Using Hierarchies for Image Retrieval"
  

## Dataset

The dataset is arranged such that each class has a directory with the corresponding images placed in them. An example directory structure is shown below.

```bash
├── dataset
│   ├── train_data
│   │   ├── class1
│   │   ├── class2
...
│   │   ├── classN
│   ├── test_data
│   │   ├── class1
│   │   ├── class2
...
│   │   ├── classN

```
Each dataset is followed by a csv file containing the class name and the corresponding classification label. An example for CIFAR10 is given in `data/cifar10.csv`.

The dataset paths and the id paths (csv files) should be included in the `config.py`. 


## Training

The hyperparameters and arguments needed for training the network are available in `config.py`.
To launch the training, run 
```
python3 train.py
```
The code automatically splits the dataset into train and validation. 

## Inference
To launch the inference, run
```
python3 main_img_retrieval.py
```
This computes the hierarchy and performs image retrieval.


