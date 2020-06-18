## Training the Archive
A research project based at the German [Ludwig Forum for International Art Aachen](http://ludwigforum.de/) and the [Hartware MedienKunstVerein (HMKV)](https://hmkv.de/) in Dortmund, Germany that combines artificial intelligence and museum collection data through machine learning and object recognition. The project is funded by the Digital Culture Programme of the German Federal Cultural Foundation. 

Over the next four years (2020-2023), the research project "Training the Archive" will explore the possibilities and risks of AI in relation to the automated structuring of data to support curatorial practice and artistic production. Connected to this is the research question of whether AI can learn research processes so that patterns, connections and associations become recognizable that are not apparent to humans in this form. Together with international artists and curators, a procedure is to be developed that will help to make digital archives - such as the collection of the Ludwig Forum Aachen - accessible in a new way.

<img src="https://github.com/DominikBoenisch/Training-the-Archive/blob/master/logo_partners.jpg" alt="Logos" width="240" height="75">  <img src="https://github.com/DominikBoenisch/Training-the-Archive/blob/master/logo_funding.jpg" alt="Logos" width="193" height="75">

### Prototype: 
Clustering of images from a museum collection to identify interesting links.  Subsequently, 
the human being is to be brought back into the loop, in which networks for image recognition are 
retrained with the knowledge of curators, for example, in order to make the clusters more dynamic and personalized.

The first prototype was developed within the context of the so-called [*AI school*](https://www.link-niedersachsen.de/ki_schule) in the [LINK](https://www.link-niedersachsen.de/) programme of the Lower Saxony Foundation in cooperation with the tutors [Dr. rer. nat. Jan Sölter](https://de.linkedin.com/in/jansoelter) and Dr. rer. nat. Thomas Rost.

### Step by step guide:
1. Scraping of data from the [Open Source Library](https://www.smk.dk/en/article/smk-open/) of the National Gallery of Denmark (SMK).
    * [Notebook](https://github.com/DominikBoenisch/Training-the-Archive/tree/master/Prototype/1_Scraper)
2. Extracting feature vectors from [Keras Applications](https://keras.io/api/applications/) or [Tensorflow Hub](https://tfhub.dev/s?q=bit)
    * [Notebooks](https://github.com/DominikBoenisch/Training-the-Archive/tree/master/Prototype/2_Feature_Extractor)


