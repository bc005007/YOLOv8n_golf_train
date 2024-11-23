
galf - v2 2023-12-05 3:44am
==============================

This dataset was exported via roboflow.com on December 4, 2023 at 10:22 PM GMT

Roboflow is an end-to-end computer vision platform that helps you
* collaborate with your team on computer vision projects
* collect & organize images
* understand and search unstructured image data
* annotate, and create datasets
* export, train, and deploy computer vision models
* use active learning to improve your dataset over time

For state of the art Computer Vision training notebooks you can use with this dataset,
visit https://github.com/roboflow/notebooks

To find over 100k other datasets and pre-trained models, visit https://universe.roboflow.com

The dataset includes 14657 images.
Galf are annotated in YOLOv8 format.

The following pre-processing was applied to each image:
* Auto-orientation of pixel data (with EXIF-orientation stripping)

The following augmentation was applied to create 2 versions of each source image:
* 50% probability of horizontal flip
* Randomly crop between 0 and 20 percent of the image
* Random rotation of between -10 and +10 degrees
* Random shear of between -7° to +7° horizontally and -8° to +8° vertically
* Random brigthness adjustment of between -25 and +25 percent
* Random exposure adjustment of between -25 and +25 percent
* Random Gaussian blur of between 0 and 2.5 pixels
* Salt and pepper noise was applied to 3 percent of pixels


