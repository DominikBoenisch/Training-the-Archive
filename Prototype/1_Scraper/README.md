### Scraping data from an art museum collection

The data is made available by the [National Gallery of Denmark (SMK)](https://www.smk.dk/en/article/smk-open/) via a so-called Application Programming Interface (API). According to the SMK meta-information of more than 70,000 digitised artworks are available. In fact, 79,002 object data can be accessed at the state of prototype development (March 2020). For the prototype only those data sets were scanned which contained an image file. 

For this purpose, all identification numbers of the works of art were read out via the standardized International Image Interoperability Framework (IIIF) interface and then checked for each ID link to see whether an associated thumbnail was available and loaded if necessary (44,626 images). In addition, a query was made as to whether the scraped work is in the public domain or whether it is copyrighted (32,411 images without copyright). This information is intended to help ensure that the image data is handled confidentially from the outset and that no copyrights are violated.

The [notebook](https://github.com/DominikBoenisch/Training-the-Archive/blob/master/Prototype/1_Scraper/Scraper.ipynb) was made possible with the help of [Dr. rer. nat. Jan Sölter](https://de.linkedin.com/in/jansoelter).
