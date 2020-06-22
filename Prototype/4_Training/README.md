### Training of a network with our annotations, which artworks are related and which are not

We start training a network whose features we have downloaded in advance and which we want to implement. We use our annotated data from the [TrainingDataGenerator](https://github.com/DominikBoenisch/Training-the-Archive/tree/master/Prototype/3_Training_Dataset). As a result we get a *relearned* network which we can evaluate in a second step. The notebooks were made possible with the help of [Dr. rer. nat. Jan Sölter](https://de.linkedin.com/in/jansoelter) and Dr. rer. nat. Thomas Rost.

#### Training the neural networks

* [Notebook Training](https://github.com/DominikBoenisch/Training-the-Archive/blob/master/Prototype/4_Training/Training_SimilarityNet.ipynb)
<img src="https://github.com/DominikBoenisch/Training-the-Archive/blob/master/2000_Samples_XceptionNet.png" width="750" height="">
Results of the XceptionNet training (example)

Image © Dominik Bönisch, Ludwig Forum Aachen

#### Evaluating with meanrank

For the evaluation we use the so-called meanrank, which helps us to clarify at which position the (un)trained neuronal network selects the work of art that we have labelled as related (positive) to our anchor according to the triplet loss. Here the rank around 4.5 is considered to be coincidental. All values below this rank indicate a successful training.

* [Notebook Evaluation]()



#### Controlling with self meanrank

To better understand what the meanrank of the neural networks means, we test to what degree we make the same selection of our positive to our labelled anchor when we re-present the annotations. Our own meanrank should not only be as low as possible, but also shows up to which fit we can train the neural networks to the maximum.

* [Notebook SelfMeanRank]()
