# InfraNet
InfraNet: Accurate Forehead Temperature Measurement Framework for People in the Wild with Monocular Thermal Infrared Camera


Abstract:During an epidemic, accurate human temperature screening based on neural networks for disease
surveillance is important and challenging. Existing distant human forehead temperature measuring
device usually adopts a dual-camera system using paired RGB and thermal infrared images to conduct
face detection and temperature measurement. Since the facial RGB image may undermine people’s
privacy, we designed a monocular thermal system and proposed an effective framework called the
InfraNet to measure and calibrate forehead temperature of people in the wild. To address the challenge
of temperature floating, the InfraNet calibrates the subject’s temperature with one’s physical depth
and horizontal offset predicted by a single infrared image. Our InfraNet framework mainly consists
of three parts: face detection subnet, depth and horizontal offset estimation subnet and temperature
calibration subnet. The temperature calibration performance can be improved with the help of spatial
regularization term concentrating on predicting precise depth and horizontal offset of people. Besides,
we collected a large-scale infrared image dataset in the both lab and wild scenarios, including 8,215
thermal infrared images. Experiments on our wild dataset demonstrated that the InfraNet achieved
91.6% high accuracy of distant multi-subject temperature measurement on average under the standard
temperature threshold of strict 0.3◦C.

Non-linear temperature attenuation (floating) calibration(The captured temperature
map by the thermal infrared camera presents non-linear attenuation, especially in the distant region.):
![2](https://github.com/aaalds/InfraNet/assets/92625242/c5b6f4e9-38af-40d4-a6fa-016ffc2c7287)
This is an example as shown demonstrates the nonlinear temperature decay of the 37◦C blackbody in a large area (12 metres vertical
depth and 3 metres horizontal width). It can be seen that its temperature is closest to the true temperature at a vertical depth of 4 -
5 metres and a horizontal offset of 0m, while all other areas show
irregular decay. The figure shows that our goal is to calibrate all
temperatures in the region to the interior of the upper and lower
planes, which shows how difficult this goal is.


Our proposed InfraNet:
![1](https://github.com/aaalds/InfraNet/assets/92625242/964a0785-c0a2-44d9-8c7e-824802e5ec01)
InfraNet extracts the features from monocular thermal infrared images for remote face location and temperature calibration. It
consists of three subnets, including the face detection subnet, depth and horizontal offset estimation subnet, and temperature calibration
subnet. InfraNet innovatively uses single-frame thermal infrared image for depth estimation and horizontal offset estimation, and utilizes
this information to calibrate the raw facial forehead temperature.

 Datasets:
![3](https://github.com/aaalds/InfraNet/assets/92625242/7b7dde25-df6e-4f7a-a0e5-65db4bdddfd0)
General description of L-TMII Dataset and W-TMII Dataset. We collected data according to different human characteristics, such
as whether existing glasses, masks, forehead occlusions or different facial orientations, etc.
The data collection and annotation process required substantial human and material resources. Due to its significant value for future research on human temperature estimation, we will organize the dataset for publication after the paper is released.

