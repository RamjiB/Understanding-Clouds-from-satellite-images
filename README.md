# Understanding-Clouds-from-satellite-images
Climate change has been at the top of our minds and on the forefront of important political decision-making for many years. We hope you can use this competition’s dataset to help demystify an important climatic variable. Scientists, like those at Max Planck Institute for Meteorology, are leading the charge with new research on the world’s ever-changing atmosphere and they need your help to better understand the clouds.

Shallow clouds play a huge role in determining the Earth's climate. They’re also difficult to understand and to represent in climate models. By classifying different types of cloud organization, researchers at Max Planck hope to improve our physical understanding of these clouds, which in turn will help us build better climate models.

There are many ways in which clouds can organize, but the boundaries between different forms of organization are murky. This makes it challenging to build traditional rule-based algorithms to separate cloud features. The human eye, however, is really good at detecting features—such as clouds that resemble flowers.

In this challenge, you will build a model to classify cloud organization patterns from satellite images. If successful, you’ll help scientists to better understand how clouds will shape our future climate. This research will guide the development of next-generation models which could reduce uncertainties in climate projections.

# Data

In this competition you will be identifying regions in satellite images that contain certain cloud formations, with label names: Fish, Flower, Gravel, Sugar. For each image in the test set, you must segment the regions of each cloud formation label. Each image has at least one cloud formation, and can possibly contain up to all all four.

The images were downloaded from NASA Worldview. Three regions, spanning 21 degrees longitude and 14 degrees latitude, were chosen. The true-color images were taken from two polar-orbiting satellites, TERRA and AQUA, each of which pass a specific region once a day. Due to the small footprint of the imager (MODIS) on board these satellites, an image might be stitched together from two orbits. The remaining area, which has not been covered by two succeeding orbits, is marked black.

The labels were created in a crowd-sourcing activity at the Max-Planck-Institite for Meteorology in Hamburg, Germany, and the Laboratoire de météorologie dynamique in Paris, France. A team of 68 scientists identified areas of cloud patterns in each image, and each images was labeled by approximately 3 different scientists. Ground truth was determined by the union of the areas marked by all labelers for that image, after removing any black band area from the areas.

The segment for each cloud formation label for an image is encoded into a single row, even if there are several non-contiguous areas of the same formation in an image. If there is no area of a certain cloud type for an image, the corresponding EncodedPixels prediction should be left blank. You can read more about the encoding standard on the Evaluation page.

# Models and corresponding private score:
- UNET with resnet50 (0.01836)
- UNET with resnet34 (0.19767)
- UNET with densenet169 (0.22112)
- UNET with VGG19 (0.40394)
- UNET with VGG16 (0.36422)
- UNET with Efficientnetb0 (0.22206)
- UNET with Efficientnetb1 (0.21096)

# Competition link
https://www.kaggle.com/c/understanding_cloud_organization
