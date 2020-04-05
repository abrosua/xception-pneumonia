# Pneumonia X-Ray Image Classification
This is one of the machine learning project assignment of the [bangkit](https://events.withgoogle.com/bangkit/) program by Google, an exclusive machine learning academy led by Google, in collaboration with several Indonesian unicorn startups.

In this case, we're tasked to solve one problem from any public datasets. Hence, we chose an image classification problem for chest x-ray images (normal or pneumonia). The dataset is provided by [Paul Mooney](https://github.com/paultimothymooney) on [Kaggle](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia).

## Getting Started

### Methodology
Convolutional Neural Networks (CNN), is currently the best solution for handling Computer Vision problem. However, harnessing its full potential might be very resourceful. Therefore we decided to use [transfer learning](https://en.wikipedia.org/wiki/Transfer_learning) on popular CNN architecture. The model is sorted from ImageNet's image classification [leaderboard](https://paperswithcode.com/sota/image-classification-on-imagenet), since ImageNet is consisted of thousands of classes, thus might provides model with better generalization.

> Note: To simplify the problem, we used the [built-in models](https://www.tensorflow.org/api_docs/python/tf/keras/applications) that are available on TensorFlow Keras, and sorted by the ImageNet leaderboard.

Xception and VGG-16 network are chosen due to its performance and number of parameters. Since we're working on limited resources, "lighter" models are preferable.

To limit our scope of work, we decided to tune the optimizer hyperparameter only (e.g., learning rate, scheduler, etc) as it's the one that arguably impacts the performance the most.

### Model

1. Xception ([Chollet, 2017](http://openaccess.thecvf.com/content_cvpr_2017/papers/Chollet_Xception_Deep_Learning_CVPR_2017_paper.pdf))
2. VGG-16 ([Simonyan and Zisserman, 2015](https://arxiv.org/abs/1409.1556))

### Built With

* [TensorFlow 2.1.0](https://www.tensorflow.org/)
* [Google Colab](https://colab.research.google.com/)

### File Structure

 - `docs`--- supporting documentations
	 - Training report (hyperparameter tuning record).
	 - Network assessment report (TensorFlow's built-in model ranking in ImageNet current [leaderboard](https://paperswithcode.com/sota/image-classification-on-imagenet)).
	 - Presentation slides.
 - `input` --- dataset storage
	 - `xception` --- pretrained weights (for offline usage)
 - `main` --- notebooks working directory
 - `output` --- training results storage (e.g., trained weights, training history, etc)

## Authors

* **Faber Silitonga** --- [abrosua](https://github.com/abrosua)
* **Fikhri Masri** --- [fikhrimasri](https://github.com/fikhrimasri)
* **Dimas Anom Priyayi** --- [priyayidimas](https://github.com/priyayidimas)
