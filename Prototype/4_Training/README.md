### Training of a network with our annotations, which artworks are related and which are not

We start training a network whose features we have downloaded in advance and which we want to implement. We use our annotated data from the [TrainingDataGenerator](https://github.com/DominikBoenisch/Training-the-Archive/tree/master/Prototype/3_Training_Dataset). As a result we get a *relearned* network which we can evaluate in a second step. The notebooks were made possible with the help of [Dr. rer. nat. Jan Sölter](https://de.linkedin.com/in/jansoelter) and Dr. rer. nat. Thomas Rost.

#### Training the neural networks

* [Notebook Training](https://github.com/DominikBoenisch/Training-the-Archive/blob/master/Prototype/4_Training/Training_SimilarityNet.ipynb)

<img src="https://github.com/DominikBoenisch/Training-the-Archive/blob/master/Images/3000_Samples_BiT-M.152x4.png" width="750" height="">

Results of the BiT-M training (example, train. set: 2,250 annot., val. set: 750 annot.);
Image © Dominik Bönisch, Ludwig Forum Aachen

#### Evaluating with meanrank

For the evaluation we use the so-called meanrank, which helps us to clarify at which position the (un)trained neuronal network selects the work of art that we have labelled as related (positive) to our anchor according to the triplet loss. Here the rank around 4.5 is considered to be coincidental. All values below this rank indicate a successful training. The meanrank was evaluated by the annotations that were also used for the training and for an additional verification, 500 unseen annotations were given for evaluation. 

* [Notebook Evaluation](https://github.com/DominikBoenisch/Training-the-Archive/blob/master/Prototype/4_Training/MeanRankEvaluation.ipynb)

Model / MeanRank | Before Training<sup>1</sup>| Training (3,000 annot., 600 epochs)<sup>1</sup>| Verification (500 annot.)<sup>2</sup>
------------ | -------------| -------------| -------------
[BiT/m-152x4](https://tfhub.dev/google/bit/m-r152x4/1) | 3.79360568383659| 2.030666666666667| 1.932
[InceptionV3](https://keras.io/api/applications/inceptionv3/) | 4.332| 2.779| 2.902
[Xception](https://keras.io/api/applications/xception/) | 4.38| 2.829| 2.724
[ResNet152V2](https://keras.io/api/applications/resnet/#resnet152v2-function)| 4.561333333333334| 2.834| 3.08 
[InceptionResNetV2](https://keras.io/api/applications/inceptionresnetv2/) | 4.456333333333333| 3.2676666666666665| 3.2
[EfficientNetB7](https://keras.io/api/applications/efficientnet/#efficientnetb7-function) | 4.544| 3.6686666666666667| 3.784

<p><sup>1</sup> The annotations were those used in the training<br> 
<sup>2</sup> 500 annotations were held back and given unseen to the trained models for evaluation</p>

#### Optimization through stacking of feature files
We can even increase our meanrank if we bring certain features of different models together. For example the combination of our trained BiT/m-152x4 and the trained InceptionV3 features:
```javascript
feature_files = [('/…/relearned_BiT-M152x4.npz', None),
                 ('/…/relearned_Inception.npz', None)]
```
<p>The mean rank is <ins>2.005333333333333</ins>.<sup>1</sup><br>
The mean rank is <ins>1.896</ins>.<sup>2</sup></p>

#### Controlling with self meanrank

To better understand what the meanrank of the neural networks means, we test to what degree we make the same selection of our positive to our labelled anchor when we re-present the annotations. Our own meanrank should not only be as low as possible, but also shows up to which fit we can train the neural networks to the maximum.

* [Notebook SelfMeanRank](https://github.com/DominikBoenisch/Training-the-Archive/blob/master/Prototype/4_Training/SelfMeanRank.ipynb)

Example SelfMeanRank by Dominik Bönisch:
> With 100 re-visited annotations I have a SelfMeanRank of 1.73.
