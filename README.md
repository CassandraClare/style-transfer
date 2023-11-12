# style-transfer

The model architecture is taken from research paper https://arxiv.org/abs/1603.08155 . It consists of two CNN architectures, one whose weights will be trained to change the style of the input image and the other one which is just a pretrained VGG model for extracting the image features. The weights for style and content can be changed individually and it will change the output image accordingly. 
I have used COCO dataset (just 5K images subset) to train the model. The dataset needs to be downloaded seperately and the notebook can be run easily after that. The dataset can be found at https://cocodataset.org/#download

## Potential Improvments
In this model we are manually choosing the layers the outputs of which we are using to calculate style and content loss. If that process could somehow be automated to find the best hyperparameters(layers) then the model performance can improve.
