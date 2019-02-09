# Fasti-course - Lesson 1


####cheat seet:

   - [**fastai.vision**](https://docs.fast.ai/vision.html) - module for computer vision;
   - **help()** - print out a quick little summary;
   - **doc()** - show documentation;
   - **untar_data()** -  function to which we must pass a URL as an argument and which will download and extract the data;
   - **ImageDataBunch.from_name_re()** - gets for example the labels from the filenames using a regular expression;
   - [**vision.learner**](https://docs.fast.ai/vision.learner.html) - a general concept for things that can learn to fit a model;
   - [**ConvLearner**](https://github.com/fastai/fastai/blob/master/old/fastai/conv_learner.py) - made convolutional neural network for you;
   - [**fit_one_cycle**](https://docs.fast.ai/train.html#fit_one_cycle) - better than simple fit (the 1cycle policy);
   - [**learner.save**](https://docs.fast.ai/vision.learner.html#create_cnn) - save weights from trained model;
   - [**data.c**](https://docs.fast.ai/vision.data.html#ImageDataBunch) - number of the classes in data (only for classification problems);
   - [**ClassificationInterpretation**](https://docs.fast.ai/vision.learner.html#ClassificationInterpretation) - use this class for class interpretation, for example:
       - **plot_top_losses** - how good was your prediction;
       - **plot_confusion_matrix** - show the predicted and actual that got wrong most often in matrix;
       - **most_confused** - show the predicted and actual that got wrong most often;
   - **lr_find()** - helps to find a proper learning rate;
   - [**learn.recorder.plot()**](https://docs.fast.ai/basic_train.html#Recorder.plot) - draw learning finder on plot (how quickly am I updating the parameters in model);


   
####Tips:
  1. resnet34 or restnet50 (number of layers) could be used as a training part. These two type already have included weights so the training is performed much faster
  2. Since our model is working as we expect it to, we will *unfreeze* our model and train some more.
  3. A good rule of thumb is after you unfreeze (i.e. train the whole thing), pass a max learning rate parameter, pass it a slice, make the second part of that slice about 10 times smaller than your first stage.
  4. This is a shortcoming of current deep learning technology which is that a GPU has to apply the exact same instruction to a whole bunch of things at the same time in order to be fast. If the images are in different shapes and sizes, you can't do that.
