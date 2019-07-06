# Grad-CAM implementation for Keras
Using mostly code from [totti0223](https://github.com/totti0223/gradcamplusplus)'s Gradcam++'s implementation.

This code is explained on [this blog article](http://blog.samuelprevost.com/neural-network/grad-cam-explaining-cnn-predictions/) and more in depth in the paper [Grad-CAM: Visual Explanations from Deep Networks via Gradient-based Localization](https://arxiv.org/abs/1610.02391).

![Applied to sunglasses image](https://raw.githubusercontent.com/sam1902/GradCAM-Keras/master/sunglasses.png)

# Usage
```
main.py [-h] --input /path/to/input/image.png
               [--output /path/to/output/graph.png] --layer
               {block1_conv1,block1_conv2,block2_conv1,block2_conv2,block3_conv1,block3_conv2,block3_conv3,block3_conv4,block4_conv1,block4_conv2,block4_conv3,block4_conv4,block5_conv1,block5_conv2,block5_conv3,block5_conv4}
               [-v] [-q]

Explains what VGG19 looks at to classify the given image.

optional arguments:
  -h, --help            show this help message and exit
  --input /path/to/input/image.png, -i /path/to/input/image.png
                        Image to run onto, can be any format.
  --output /path/to/output/graph.png, -o /path/to/output/graph.png
                        Where to generate the output visualisation.
  --layer {block1_conv1,block1_conv2,block2_conv1,block2_conv2,block3_conv1,block3_conv2,block3_conv3,block3_conv4,block4_conv1,block4_conv2,block4_conv3,block4_conv4,block5_conv1,block5_conv2,block5_conv3,block5_conv4}, -l {block1_conv1,block1_conv2,block2_conv1,block2_conv2,block3_conv1,block3_conv2,block3_conv3,block3_conv4,block4_conv1,block4_conv2,block4_conv3,block4_conv4,block5_conv1,block5_conv2,block5_conv3,block5_conv4}
                        Layer at which to "look at".
  -v, --verbose
  -q, --quiet           If set, doesn't show the plot and only saves the
                        output (if one is provided).
```