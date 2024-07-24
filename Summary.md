# Summary
## U-Net
The u-net is derived from convolutional network for fast and precise segmentation of images. Image Segmentation is partitioning image to discrete group of pixels which is helpful for object detection, faster image processing.

## U-net Architecture

**Encoder:**
The primary goal of **Encoder** is to capture high level features from the input image. U-Net encoding starts with **convolutional** layer which extracts features using filters, followed by **max pooling** layer which reduces the spatial 
resolution of feature maps. Again we apply **convolutional layer** followed by **max pooling** layer, this loop repeats depending on complexity of features that we are extracting.

**Bridge:**
Bridge helps to connect Encoder and Decoder using skip connections. It consists of convolutional layers. It concatenates the feature maps from the encode and pass it to the corresponding decoder layer to preserver spatial information.

**Decoder:**
The primary goal of **Decoder** is to decode the encoded data by locating the features while maintaining the spatial resolution of the input. Decoder starts with transposed convolution layer which upsamples the feature map from the encoder,
followed by conolutional layers to refine the feature maps. This loop continues, until it produces a final segmentation map by concatenating the feature maps in each layer.

![image](https://github.com/user-attachments/assets/93834323-76c2-409e-a420-114cdd44c8c8)

[![image](https://img.youtube.com/vi/NhdzGfB1q74/0.jpg)](https://www.youtube.com/watch?v=NhdzGfB1q74)


**Example:** Medical Image Segmentation\
**Input:** An MRI scan image to identify multiple tissues.\
**Encoding:** During encoding, pixels are extracted from the image using edges, textures, shapes, and larger structures etc.\
**Decoding:** Decoding uses generated pixels from encoding and combines all the pixels to form a single segmented image by producing a map that classifies each pixel as healthy tissue, tumor, organ.\
**Output:** Output is a labelled image produced in decoding step, which is useful for medical diagnosis.




