# The Chinese Antique Porcelain Shapes Classifier
-------
## Executive summary
### Chinese Antique Porcelain background
Chinese antique porcelains are one of the most popular collectibles in the art world. The fascination is not only within the Chinese, but across the globe. According to the eighth annual edition of the Global Chinese Art Auction Market Report, a partnership between Artnet and the China Association of Auctioneers (CAA), global auction sales of Chinese art and antiques reached $5.7 billion in 2019. (source)

The porcelain pieces are not appreciated only for the sophisticated yet pleasing motifs. The shapes of the porcelains also contribute to the beauty appreciation for Chinese antiques. Over the centuries from Neolithic to the Qing dynasty, the porcelains have evolved and improved into a wide variety of styles and shapes. Even now, the modern vases are inspired by the classical timeless shapes of the antique porcelains.

### Porcelain shapes
There are roughly at least 20 basic shapes. In this project, we will be looking at 5 shapes. The first will be a simple shape that help the Chinese to hold brushes. Hence. the shape is called brush pot. To increase the challenge for this project, I’ve chosen jar to be the second shape for classification as the jar shape can be quite similar to the brush pot shape. The third and fourth shapes are Tian Qiu Ping a.k.a. Globular Vase and Chang Jing Ping a.k.a. long neck vase. These two shapes look similar on screen. Newbie in antique collection will easily misclassify one for another. Lastly, I’ve included one of my favourite shapes, Meiping a.k.a plum vases, to complicate the classification model even more.

### Problem statement
Chinese antique collection is a very challenging and expensive activity. It is expensive not only for the cost of the porcelain but also for the chances of buying a fake one. To prevent overpaying for a porcelain or buying a fake one (especially through online transactions), the collector will need to know the basics. Shape of the porcelain is one of the fundamentals to evaluate the antique authenticity and value. The classifier will help new collectors to correctly identify some of the antique porcelain shapes.

## Data
The images were mainly collected from auctions houses such as Sotheby. These auction houses’ images are clean with minimal noise. Thus, the model results might be misleading since the images are ‘too clean’. Therefore, images with noisy backgrounds were also included into the dataset.

For each class, I’ve gathered at least 100 images from the web. Most of the images were cropped at a standard 256 by 256 pixels dimension. The image size was decided based on the research performed at Lund University by Olivier Rukundo. (source)

Google drive link: https://drive.google.com/drive/folders/1nT1nlHSjWSwGSsMxiOeGrRzfQapbdxhY?usp=sharing

## Modelling approach

The modelling process has three stages: Modelling without pre-trained models, Modelling with pre-trained models and Fine tuning pre-trained models.

Modelling without pre-trained model will be the baseline model. This model layers were manually added by me.
The pre-trained models used for this project are: VGG19, MobileNetV2 and ResNet50. For the second stage where modelling were done with pre-trained models, the top layer was not included and I've freeze all layers in the pre-trained model, then extra layers were added to the model. There is only one callback which is the model checkpoint to save out the weights and learning rate was fixed. For the third stage where the pre-trained models were fine tune, I've only freeze the first 10 layers of the model abd I used ReduceLROnPlateau as another callbacks to reduce the learning rate. This fine tuning approach is based on keras documentation.

## Conclusion
### Summary on model chosen
I've chosen the fine tuned VGG19 model for classifying chinese antique porcelain shapes.
Baseline Model Accuracy: 47.7%
Fine Tuned VGG19 model: 86.4%
* Jar, Meiping and Brushpot classes were predicted perfectly.
* The number of images misclassified for cjp and tqp is the same at 9.
* The learning rate was reduced to 1.6000e-06 for the best weights

### Uses for this classifier
The classifier can be used for new chinese antique collectors interested in collecting the 5 classes: Brushpot, Jar, Meiping, Chang Jing Ping and Tian Qiu Ping. By using the classifier, they can get one of the basic about the chinese antique porcelain right.

This classifier can also be used as a stepping stone for classifying chinese antiques by dynasty. This can even further evaluate the porcelain value.

### Future Work
* To collect more data for all existing classes
* Increase the number of classes to predict
* To do object detection
* Evolve to dynasty classifier for the porcelain pieces

## References
Chinese Antique Market popularity in terms of monetary value: https://cn.artnet.com/en/chinese-art-auction-market-report/

Research on the thumbrule for image size: https://www.researchgate.net/post/Which_Image_resolution_should_I_use_for_training_for_deep_neural_network

Keras documantation on Conv2d: https://keras.io/api/layers/convolution_layers/convolution2d/

Using ADAM as optimizer: https://machinelearningmastery.com/adam-optimization-algorithm-for-deep-learning/

Fine tuning approach based on keras documentation: https://keras.io/guides/transfer_learning/
