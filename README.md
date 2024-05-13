This repository is the Unofficial Implementation of the "DCU-Net: a dual-channel U-shaped network for image splicing forgery
detection" research paper https://doi.org/10.1007/s00521-021-06329-4

The training was done on CASIA Dataset by me but the original author trained it on CASIA and Columbia Dataset.

The proposed model is the modified version of the UNet model. It consists of two input encoder branches. One branch is adopts the structure of the VGG16 model and the other branch adopts the ResNet sturcture. The outputts of both of these branches is concatenated and then passed to the decoder that produced the desired output image. The goal of this model is to perform Image Segmentation of the tampered region in the image.

The model takes two images as input. The first one is the original tampered image and the other one is the residual image of the tampered image. The residual image is prepared by convolving the tampered image with the horizontal and vertical sobel filters.

The output image produced by the proposed model contains the segmented region for the tampered area.
