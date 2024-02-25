# Capsule-Network Implementation on MNIST Data
 
### Abstract: 
Capsule Networks, a novel architecture proposed by Geoffrey Hinton and colleagues, revolutionize the field of neural networks, particularly in the domain of computer vision. Departing from conventional convolutional neural networks (CNNs), Capsule Networks introduce capsules, groups of neurons that collaboratively represent entities and encode information about their spatial relationships. The dynamic routing mechanism employed by Capsule Networks in Dynamic Routing Between Capsules [Hinton et al] allows adaptive adjustments of connections between capsules, enhancing the model's ability to capture hierarchical features and handle variations in pose and viewpoint. In this study, we explore the application of Capsule Networks to the MNIST dataset, a well-established benchmark for handwritten digit recognition. Our investigation involves the design and implementation of a Capsule Network architecture, training on the MNIST dataset, and evaluating its performance on unseen data using Python and Pytorch. The results provide insights into the effectiveness of Capsule Networks for image classification tasks, shedding light on their potential advantages and areas for further refinement.

# FAQs:

### Failure on Import

If some of the modules are missing we can install them by uncomenting the following cell and running it in the cell. (*provided in the notebook*)

```python
!pip install torch torchvision tqdm numpy
```

### How to train the model if you want to:

We have set up a **train_capsnet** flag and set it to ```False``` to avoid training the large model.
If you wish to retrain the model set it to ```True```.

We have also included a pre-trained capsnet model in the variable **saved_model_name** we used to generate all our results included in the trainng. The name of the saved model is ```'final_model.pth'```

Should you choose to re-train the model, the new model will be saved as ```'final_model_new.pth'``` to avoid overwriting the previously trained model

```python
# Set False to avoid the training, it took about 30 mins for all 10 epochs to finish training
train_capsnet = False
# Name of the Saved Pre-trained-Model Included in the project
saved_model_name = 'final_model.pth' 
```

### How to Interpret the perturbations:
 - The rows represent the pose_parameters learnt for the images
 - The columns represent the minute perturbations introduced in the parameter, the perturbations are linear in our case ranging from `-0.2` to `+0.2`
