# Miniproject BIO-322 :computer:

### Team "The mid-table team" 
<img src="https://github.com/frossardr/ML_project_Themidtabbleteam/assets/114407059/0d9d973f-98f9-489e-ab3d-c967374e0250" alt="image" width="1100" height="400">

## Requirements :snake:
You can find our environment file [miniproject_bio322.yml](./miniproject_bio322.yml) and create a conda environment using the commands:
```markdown
conda env create -f environment.yml
```
And then you can activate the environment using:
  * Windows: 
```markdown
conda activate miniproject_bio322
```
  * macOS or Linux:
```markdown
source activate miniproject_bio322
```

## Our code
The data preparation steps can be seen in the [cleaning.ipynb](./cleaning.ipynb) file.
For a clearer view of the data, please refer to the [visual.ipynb](./visual.ipynb) file.
We have implemented 2 model types, which you can view in the files below:
 * Linear regression: [linear_regression.ipynb](./linear_regression.ipynb)
 * Neural network with 2 layers: [DNN.ipynb](./DNN.ipynb)
 * Neural network with 3 layers: [DNN3.ipynb](./DNN3.ipynb)

To reproduced our results, you can use our codes above. Files used for kaggle submissions are in the [prediction](./prediction) folder under their corresponding registration names in the code.

## Results
### Linear regression:
Graphical comparison of different linear regression methods:

<img src="https://github.com/frossardr/ML_project_Themidtabbleteam/assets/114407059/d3aa9a2f-69e9-40ed-903b-6b4440b48ab4" alt="image" width="900" height="500">

We can see from this graph that the best method, the one with the lowest mean score, is the Ridge regression whith standardization applied to CDDD data. It's the only one below the red bar wich indicates the lowest mean score. The mean score corresponds to the RMSE mean.

Note: To reproduce this graph, you need to run the import box and the last two code boxes in the [linear_regression.ipynb](./linear_regression.ipynb) notebooks. Note that in this case, the values used have already been calculated by launching the other code boxes, to save time. It is possible to replace the initiation of the graph bars by uncommenting the last line of each code box and launching them all in succession.

### Neural network:
Best neural network results:

<img src="https://github.com/frossardr/ML_project_Themidtabbleteam/assets/55958594/f7a3a5db-d894-494b-846f-ce14c308a0b2" alt="image" width="1300" height="330">

The graph on the right shows that test error and train error behave relatively similarly, demonstrating the robustness of the model. On the left-hand graph, we can see that the predictions obtained (blue) are relatively close to the expected results (red), demonstrating the model's good performance.
The RMSE of the neural network (0.45) is much lower than the RMSE of the linear regression (1.18 in previous picture). This shows that the neural network is more efficient than the linear regression.

Note: To be able to reproduce this graph, you need to run all the code boxes up to and including the one entitled "Submission function" in the [DNN.ipynb](./DNN.ipynb) notebooks. The hyperparameters used for this graph are:
 * n1 = 1024
 * n2 = 2048
 * activ = tanh
 * dropout rate = 0,3
 * optimizer = AdamW(weigth decay = 0.01)
 * learning rate = OneCycleLR(max lr = 0.003)
 * numb epochs = 350
 * batch size = 64
 * loss = MSE
 * The data used are the mix of ECFP and CDDD data


## Report
Our project report is the [report.pdf](./report.pdf) file.
More information on the methodology can be found there.





### Contributors :bust_in_silhouette:
[maverest](https://github.com/maverest), [frossardr](https://github.com/frossardr)


