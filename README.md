# The power of advertisements

##  Depictions of domestic appliances in magazines and the parallel emergence of gas and electricity as sources of energy

## Short summary
The investigation aims at examining the application of computer vision tools to photos of documents and objects within historical collections. It takes as its case study the identification of domestic appliances in advertisements found within journals and magazines. To achieve this, the investigation is working in collaboration with the archives of the Institute of Engineering & Technology, which entity provided the Congruence Engine project with the digitised volume of The Electrical Age. It is also planned to assess how texts within and surrounding the advertisements can improve the identification of objects on images. 

## Aims and objectives

The initial aim of the investigation was to use computer vision tools to examine the gendered depictions of domestic appliances advertisements in historical magazines and journals. This aim was devised to 1) have a dedicated investigation within the energy strand that explores the uses of energy apart from its production and transmission, and 2) to contribute to the historical scholarship exploring the gendered depiction of advertisements.
After initial tests with the computer vision tool, it was noted that the tool was possibly not trained on historical images and low-resolution/poor quality images, given that the tool was less accurate with detection on such image types. As a result, the investigation refocused its core aim on asking what image standards and digital requirements would be needed to train a computer vision tool for specific questions. In this investigation, we are also planning on exploring how ChatGPT can assist users as a technical adviser on setting up the computer vision tool. 


## People 

**Daniel Belteki** : Conceptualization, Investigation, Data curation, Formal analysis, Methodology, Visualization 

**Kunika Kono**: Methodology, Software

**Anne Locker** : Data Curation , Resources

**Alex Butterworth** : Methodology, Investigation

**Graeme Gooday** : Investigation, Methodology

**Kylea Little**: Investigation, Methodology


## Data
The project employed the datasets below:
#### The Electrical Age 
Digitised and OCR captured version of the first two volumes of the historical magazine/journal The Electrical Age. This was provided to the Congruence Engine Project by the archives of the Institute of Engineering & Technology.

#### Images of domestic appliances from department store catalogues (archive.org)
Historical catalogues of department stores were identified on archive.org. Relevant pages and images were then downloaded from the sources.

#### Images of domestic appliances from Science Museum Group archives
The Science Museum Group archives include a large collection of trade literature produced by companies that were involved in the manufacturing of domestic appliances. The companies that frequently advertised in The Electrical Age were identified in this collection, and the relevant images of domestic appliances in these collections were photographed. 


## Method

We have been examining the usefulness of the Visual Geometry Group’s Image Classification Engine for the purposes of detecting domestic appliances in ads found in historical journal and magazines. Visual Geometry Group's (VGG) Visual Image Classification Engine (VIC Engine) is an image classification engine that trains Support Vector Machine (SVM) classifier on-the-fly, using a set of given training images, either as files or fetched online via e.g. Google images. VGG's key objective in developing VIC was a sustainable approach in the face of growing size of datasets and the data annotation needs that it implies.

The initial tests were carried out via the following method:
1a) Images of domestic appliances were identified in The Electrical Age. Two versions of these images were prepared: one where the ads were cropped out from among the text, and one where the entire page was present.
1b) Additional images of domestic appliances for comparative tests were identified in the following magazines and journals:  Life, Good Housekeeping, The Woman Engineer. Additional images were collected from the Science Museum Group online collections. 
2) Where needed, the relevant images of advertisements were cropped from the digitised full-page that they were featured on.
3) Using this dataset of images, an initial test was carried out to assess the performance of the VIC Engine without having to carry out any additional training. Two different training models were tested: rcnn resnet 2 and ssdmobilenetv2.
4) We then undertake a manual visual comparison of the identifications produced.

## Key initial findings
1)	The initial tests showed that objects were identified with higher accuracy on images featuring no texts and illustrations in colour. Objects were also identified with higher accuracy in more contemporary images. 

2)	The two different models tested also performed differently, but rather than one being more accurate than the other, they identified objects with different (though still relevant) categories and sometimes identified objects that the other model did not.

## Challenges
1)	During the data collection, the IET archives noted that they have no standard form prepared for allowing the use of their files for digital humanities tools.

2)	The IET archives also noted their concerns about the lack of data control when they share documents with short-term projects. The main concern was a lack of information about the fate of the data shared after a project ends. 

3)	The initial tests with the different models revealed that greyscale images and historical journals with a brownish/yellowish background pose challenges for the computer vision tool for the identification of objects. It appears from these results that the models were not trained on such images. Training a new model would require a collection of larger images than what has so far been acquired. 

4)	Any future training would also have to consider the quality of images upon which it is trained. This is to anticipate the type of images that would be used with the tool. For example, would the users be more likely to upload low-quality images taken with their phones in the archives, or would they be more likely to upload large batches of digitised high-quality images. 

5)	At one point it was recommended that we should take images from the trade literature collections held in the archives of the Science Museum Group. We encountered practical challenges with identifying the right material given that the trade literature collection is not yet catalogued due to its size. This issue also makes it difficult to identify whether the archival materials related to the companies actually include any items relating to domestic appliances or whether it relates to other types of products. This was a main issue with major companies such as Siemens that manufacture various different types of products. Given these complications, there were errors in communications that led to the lack of delivery of archival items for inspection.

6)	It is also important to recognise that the Congruence Engine project does not include any member of staff with high level of expertise using computer vision tools. During the last rounds of hirings of technical experts, no individual was recruited to contribute to the development of the investigation or the tool.

7)	The investigation highlighted that one of the most historically relevant and image-rich source is already digitised and available for scholars via ProQuest. However, there is no clarity in the ProQuest terms and conditions about the uses of the digitised texts and images with digital tools. In addition, the platform by ProQuest does not allow for the batch download of the digitised images. There was no contact made with ProQuest about the application of the tool to their images. This was mainly due to the slow progress made with the acquisition of images and with the testing of the tool. 

8)	In case the training of a new model has to be undertaken, there are major concerns about the hardware requirements available to the individuals. At the moment, the testing has been undertaken using the employer issued laptops, which are not necessarily equipped for the training of models. This is especially concerning in case institutions that do not meet the minimum hardware requirements would like to deploy the tool. There were also additional concerns about the installation of tools that require the authorisation of an organisation’s IT services.

9)	There have also been questions about the accessibility issues in relation to technical expertise. The installation and use of the tool (especially when used for training a model) requires relatively advanced technical knowledge. Although a documentation is available, it is not the easiest to follow these for individuals with little technical training.

10)	There are also concerns about the labels applied to the objects and individuals featured on the images. For example, this was especially noticeable through one of the model’s attempts to identify the gender of the person being depicted on the images. Although our investigation focuses on the identification of objects, rather than the individuals, it is important to note this underlying limitation of the tool. 

## Outputs
1)	The investigation has so far generated a series of screenshots showing the output of the initial tests. These have served as the basis to evaluate the usefulness of the different engines, and as the starting points for the discussions in relation to the challenges and potentials of the tool.

2)	As part of the preparation for the work, the investigation also collected a series of images from online and historical sources that depict domestic appliances. These are planned to serve as the basis for any future training work and/or for testing the engine.


## Licence 
This work is licensed under a [Creative Commons Attribution 4.0 License - CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
