### Training of a network with our annotations, which artworks are related and which are not

We start training a network whose features we have downloaded in advance and which we want to implement. We use our annotated data from the [TrainingDataGenerator](https://github.com/DominikBoenisch/Training-the-Archive/tree/master/Prototype/3_Training_Dataset). As a result we get a *relearned* network which we can evaluate in a second step. The notebooks were made possible with the help of [Dr. rer. nat. Jan Sölter](https://de.linkedin.com/in/jansoelter) and Dr. rer. nat. Thomas Rost.

#### Training the neural networks

* [Notebook Training](https://github.com/DominikBoenisch/Training-the-Archive/blob/master/Prototype/4_Training/Training_SimilarityNet.ipynb)

<img src="https://github.com/DominikBoenisch/Training-the-Archive/blob/master/Images/3000_Samples_BiT-M.152x4.png" width="750" height="">

Results of the BiT-M training (example);
Images © Dominik Bönisch, Ludwig Forum Aachen

#### Evaluating with meanrank

For the evaluation we use the so-called meanrank, which helps us to clarify at which position the (un)trained neuronal network selects the work of art that we have labelled as related (positive) to our anchor according to the triplet loss. Here the rank around 4.5 is considered to be coincidental. All values below this rank indicate a successful training.

* [Notebook Evaluation](https://github.com/DominikBoenisch/Training-the-Archive/blob/master/Prototype/4_Training/MeanRankEvaluation.ipynb)

Model / MeanRank | Before Training| Training (2,000 annotations)| Training (3,000 annotations)
------------ | -------------| -------------| -------------
[BiT/m-152x4](https://tfhub.dev/google/bit/m-r152x4/1) | 3.79360568383659| 2.0703374777975134| 2.026666666666667
[InceptionV3](https://keras.io/api/applications/inceptionv3/) | 4.332| 2.929| 2.779
[Xception](https://keras.io/api/applications/xception/) | 4.38| 3.0456666666666665| 2.829
[ResNet152V2](https://keras.io/api/applications/resnet/#resnet152v2-function)| 4.561333333333334| 2.9756666666666667| 2.834
[InceptionResNetV2](https://keras.io/api/applications/inceptionresnetv2/) | 4.456333333333333| 3.166| 3.2676666666666665
[EfficientNetB7](https://keras.io/api/applications/efficientnet/#efficientnetb7-function) | coming soon| coming soon| coming soon

#### Controlling with self meanrank

To better understand what the meanrank of the neural networks means, we test to what degree we make the same selection of our positive to our labelled anchor when we re-present the annotations. Our own meanrank should not only be as low as possible, but also shows up to which fit we can train the neural networks to the maximum.

* [Notebook SelfMeanRank](https://github.com/DominikBoenisch/Training-the-Archive/blob/master/Prototype/4_Training/SelfMeanRank.ipynb)

Example SelfMeanRank by Dominik Bönisch:
> With 20 re-visited annotations I have a SelfMeanRank of 1.25.
