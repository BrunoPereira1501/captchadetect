# captchadetect

The aim of this project was to develop a Convolutional Neural Network (CNN) capable of decoding CAPTCHAs (Completely Automated Touring test to Tell Computers and Humans Apart). Many websites use these features to prevent bot raiding, promotion spam, data scraping amongst other methods to abuse websites.

The sets of images that were provided consisted of two major groups:

    * Soft Images

![alt text](<Sem título.png>)

    * Hard Images

![alt text](<Sem título-1.png>)

The final CNN structure is depicted below:

![alt text](<captchacnn.png>)

The accuracy results were evaluated individually, i.e. each letter either correct or not; and overall accuracy which meant that all the letters from a specific CAPTCHA image needed to be correctly classified in order for that CAPTCHA be correct. As expected, the overall accuracies were lower than the individual accuracies.

The final overall CAPTCHA accuracy obtained in the soft dataset was around 80%, which is low when compared to the 95% individual character accuracy obtained in the test of the model. The resulting confusion matrix:

![alt text](<Sem título-1-1.png>)

In the hard dataset, the final overall CAPTCHA accuracy obtained was around 76%, which is also low when compared to the 95% individual character accuracy obtained in the test of the model. The resulting confusion matrix:

![alt text](<Sem título-2.png>)

The dataset is in the .rar file. The project is present at the colab file [CV]Project_2.ipynb, and also in html format, which allows for fast visualization in the browser.
