# Semantic Segmentation
### Introduction
In this project, we label the pixels of a road in images using a Fully Convolutional Network (FCN).

##### Dataset
The dataset is the [Kitti Road dataset](http://www.cvlibs.net/datasets/kitti/eval_road.php) from [here](http://www.cvlibs.net/download.php?file=data_road.zip).  

### Start
##### Implement
Implement the code in the `main.py` module indicated by the "TODO" comments.
The comments indicated with "OPTIONAL" tag are not required to complete.
##### Run
Run the following command to run the project:
```
python main.py
```
**Note** If running this in Jupyter Notebook system messages, such as those regarding test status, may appear in the terminal rather than the notebook.


GitHub also provides a [tutorial](https://guides.github.com/features/mastering-markdown/) about creating Markdown files.

## Rubic Goals
#### Does the project load the pretrained vgg model?
The function to load the pretrained vgg model is in main.py and named load_vgg. A call to tests.test_load_vgg(load_vgg, tf) show the implementation pass the unit test.


#### Does the project learn the correct features from the images?
The conversion of the fully connected layers to convolutional layers is done inthe function layers. For each converted layer we add in a regularizer help with controlling overfitting. The code passes the unit test.

#### Does the project optimize the neural network?
The optimize function minimizes the softmax cross entropy.  The function optimize is implemented correctly per the unit test.

![Loss Graph](./images/Loss.png)

#### Does the project train the neural network?
On average, the model decreases loss over time.

#### Does the project user reasonable hyperparameters?
The number of epoch and batch size were set to 35 and 5 respectively, which are reasonable. The keep probability was 0.5 and learning rate of 0.00001.

#### Does the project train the model correctly? 

The above graph is the loss with each iteration and decreases on average.

#### Does the project correctly lable the road?
Below are samples of the test images. Also provided is a semantic segmentation of the challenge video from the first project in term 1.
![image1](./images/um_000002.png)
![image2](./images/um_000078.png)

##### Video of segmented challenge.mp4

![Segemented challenge video](https://youtu.be/F3L1hvKH5nk)
