# Captcha Decoder

The aim of this project was to develop a Convolutional Neural Network (CNN) capable of decoding CAPTCHAs (Completely Automated Touring test to Tell Computers and Humans Apart). Many websites use these features to prevent bot raiding, promotion spam, data scraping amongst other methods to abuse websites.

The sets of images that were provided consisted of two major groups:

    * Soft Images

![alt text](<Sem título.png>)

    * Hard Images

![alt text](<Sem título-1.png>)

## Model

The model used for character classification was composed of two parts: convolutional section and the fully-connected section.
The individual layers were as follows:
* **Conv1** - since the individual character images were binary, only 1 channel would enter the first convolution. In the output, 32 channels were generated with a kernel of size 3 and a padding of 1.
* **COnv2** - 32 channels were received fom Conv1 and 64 channels were put at the ouput. The convolution was performed again with a kernel of size 3 and a padding of 1.
* **Pool** - to reduce the dimensions of the feature maps by half, a pooling layer was used with a kernel of size 2 and a stride of 2.
* **Dropout** - a dropout with probability of 0.2 followed by 0.5 was applied, which helped prevent overfitting by randomly setting a fraction of input units to zero during training.
* **Flatten** - used to create a one dimension tensor from the 3 dimension tensor, which allows the connection to the next layer.
* **Fc1** - first fully-connected layer with an input of 64 * 16 * 16 and an output of 1024.
* **Fc2** - second fully-connected layer with an input of 1024 and an output of 512.
* **Fc3** - second and final fully-connected layer with an input of 512 and an output of 36, which is the number of labels in the classification.

The final CNN structure is depicted below:

![alt text](<captchacnn.png>)

## Results

The accuracy results were evaluated individually, i.e. each letter either correct or not; and overall accuracy which meant that all the letters from a specific CAPTCHA image needed to be correctly classified in order for that CAPTCHA be correct. As expected, the overall accuracies were lower than the individual accuracies.

The final overall CAPTCHA accuracy obtained in the soft dataset was around 80%, which is low when compared to the 95% individual character accuracy obtained in the test of the model. The resulting confusion matrix:

![alt text](<Sem título-1-1.png>)

In the hard dataset, the final overall CAPTCHA accuracy obtained was around 76%, which is also low when compared to the 95% individual character accuracy obtained in the test of the model. The resulting confusion matrix:

![alt text](<Sem título-2.png>)

## Files
The dataset is in the .rar file. The project is present at the colab file [CV]Project_2.ipynb, and also in html format, which allows for fast visualization in the browser.
