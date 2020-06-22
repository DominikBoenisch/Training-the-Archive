### Generating a dataset for the training using triplet loss

We will use the triplet loss to label artworks that seem to be connected in every possible way (e.g. color, style, iconic content, aesthetic…) with the aim of having their embeddings close together in the embedding space and embeddings of artworks with more distant relationships or no connection at all far away. 

The training should help to incorporate the knowledge of experts such as curators in order to better classify and sort the artworks that will later be clustered. After the training, the clustering should go beyond the mere recognition of image content.

The [notebook](https://github.com/DominikBoenisch/Training-the-Archive/blob/master/Prototype/3_Training_Dataset/TrainingDataGenerator.ipynb) was made possible with the help of Dr. rer. nat. Thomas Rost.

<img src="https://github.com/DominikBoenisch/Training-the-Archive/blob/master/TrainingDataGenerator_Sample.jpg" alt="Sample TrainingDataGenerator" width="500" height="500">
Example of an iteration to generate a training data set by selecting an anchor and a positively connected artwork to it. © Dominik Bönisch, Ludwig Forum Aachen.
