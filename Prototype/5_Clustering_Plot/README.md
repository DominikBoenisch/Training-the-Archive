### Clustering of artworks using different neural networks and visualization of the results

We have our [scraped data](https://github.com/DominikBoenisch/Training-the-Archive/tree/master/Prototype/1_Scraper) put together into clusters. Thereby we can stack different [feature files](https://github.com/DominikBoenisch/Training-the-Archive/tree/master/Prototype/2_Feature_Extractor) of different neural networks and influence the high-dimensional latent space by dimensional reduction (PCA). Finally, we visualize the resulting clusters and experiment with the plots. Does the [training](https://github.com/DominikBoenisch/Training-the-Archive/tree/master/Prototype/4_Training) according to our [annotations](https://github.com/DominikBoenisch/Training-the-Archive/tree/master/Prototype/3_Training_Dataset) already have an effect on the clusters? The [notebook](https://github.com/DominikBoenisch/Training-the-Archive/blob/master/Prototype/5_Clustering_Plot/Clustering_with_Plots.ipynb) was made possible with the help of [Dr. rer. nat. Jan Sölter](https://de.linkedin.com/in/jansoelter) and Dr. rer. nat. Thomas Rost.

#### Visualizations

* Grid (uninfluenced, influenced by PCA or TSNE)
<img src="https://github.com/DominikBoenisch/Training-the-Archive/blob/master/Images/PCA_Grid_Example.png" width="850" height="">

* Scatterplot (influenced by PCA or TSNE)
<img src="https://github.com/DominikBoenisch/Training-the-Archive/blob/master/Images/TSNE_Scatter_Example.png" width="790" height="">

* Cluster with *Hierarchical Family Tree* (Dendrogramm Main- or Subcluster)
<img src="https://github.com/DominikBoenisch/Training-the-Archive/blob/master/Images/Dendrogram_Example.png" width="350" height="">

All Images © Dominik Bönisch, Ludwig Forum Aachen using data from the [Open Source Library](https://www.smk.dk/en/article/smk-open/) of the National Gallery of Denmark (SMK).
