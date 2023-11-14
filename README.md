# style-transfer

The model architecture is taken from research paper https://arxiv.org/abs/1603.08155 . It consists of two CNN architectures, one whose weights will be trained to change the style of the input image and the other one which is just a pretrained VGG model for extracting the image features. The weights for style and content can be changed individually and it will change the output image accordingly.
![image](https://github.com/CassandraClare/style-transfer/assets/84125572/47f4af7f-80a2-463e-bece-e9809c9db19a)

Once trained on a particular style, the model can be used to do real time style transfer of images. Also, it can be trained to generate images of a particular style and we need only one style image (and multiple content images) to train it.

I have used COCO dataset (just 5K images subset) to train the model. The dataset needs to be downloaded seperately and the notebook can be run easily after that. The dataset can be found at https://cocodataset.org/#download

## Results
CONTENT IMAGE

![image](https://github.com/CassandraClare/style-transfer/assets/84125572/2f850fa3-a0af-41a8-b429-b44a4aa727ea)

STYLE IMAGE

![image](https://github.com/CassandraClare/style-transfer/assets/84125572/18d32adf-4878-463d-8619-e7502f156e3b)

COMBINED IMAGE

![image](https://github.com/CassandraClare/style-transfer/assets/84125572/7d853cc5-3843-4919-a16e-ff8d815346a4)

Other results which compare the result of changes in style and content weights on the combined image are shown in the pdf file.




## Potential Improvments
In this model we are manually choosing the layers the outputs of which we are using to calculate style and content loss. If that process could somehow be automated to find the best hyperparameters(layers) then the model performance can improve.
