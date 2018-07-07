+++
title = "Low Resolution Lidar-Based Multi-Object Tracking for Driving Applications"
date = 2017-11-15T00:00:00

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Iván del Pino", "Victor Vaquero", "Beatrice Masini", "Joan Solà", "Francesc Moreno-Noguer", "Alberto Sanfeliu", " Juan Andrade-Cetto"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference proceedings
# 2 = Journal
# 3 = Work in progress
# 4 = Technical report
# 5 = Book
# 6 = Book chapter
publication_types = ["1"]

# Publication name and optional abbreviated version.
publication = "In *Robot 2017: Third Iberian Robotics Conference*."
publication_short = "In *ROBOT*"

# Abstract and optional shortened version.
abstract="Vehicle detection and tracking in real scenarios are key components to develop assisted and autonomous driving systems. Lidar sensors are specially suitable for this task, as they bring robustness to harsh weather conditions while providing accurate spatial information. However, the resolution provided by point cloud data is very scarce in comparison to camera images. In this work we explore the possibilities of Deep Learning (DL) methodologies applied to low resolution 3D lidar sensors such as the Velodyne VLP-16 (PUCK), in the context of vehicle detection and tracking. For this purpose we developed a lidar-based system that uses a Convolutional Neural Network (CNN), to perform point-wise vehicle detection using PUCK data, and Multi-Hypothesis Extended Kalman Filters (MH-EKF), to estimate the actual position and velocities of the detected vehicles. Comparative studies between the proposed lower resolution (VLP-16) tracking system and a high-end system, using Velodyne HDL-64, were carried out on the Kitti Tracking Benchmark dataset. Moreover, to analyze the influence of the CNN-based vehicle detection approach, comparisons were also performed with respect to the geometric-only detector. The results demonstrate that the proposed low resolution Deep Learning architecture is able to successfully accomplish the vehicle detection task, outperforming the geometric baseline approach. Moreover, it has been observed that our system achieves a similar tracking performance to the high-end HDL-64 sensor at close range. On the other hand, at long range, detection is limited to half the distance of the higher-end sensor."

# Featured image thumbnail (optional)
image_preview= "robot_17_DeepLidarPuck/robot17.png"

# Is this a selected publication? (true/false)
selected = false

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#projects = ["example-external-project"]

# Links (optional).
url_pdf = "http://www.iri.upc.edu/files/scidoc/1924-Low-resolution-lidar-based-multi-object-tracking-for-driving-applications.pdf"
#url_preprint = "http://www.iri.upc.edu/files/scidoc/1902-Joint-coarse-and-fine-reasoning-for-deep-optical-flow.pdf"
#url_code = "#"
#url_dataset = "#"
#url_project = "#"
url_slides = "#"
url_video = "#"
#url_poster = "#"
#url_source = "#"

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
url_custom = [{name = "SPRINGER", url = "https://link.springer.com/chapter/10.1007/978-3-319-70833-1_24"},
              {name = "IRI", url = "http://www.iri.upc.edu/publications/show/1924"}]

# Does the content use math formatting?
math = true

# Does the content use source code highlighting?
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
#image = "GeneralFig_FULL.jpg"
#image = "ICIP17_vvaquero.pdf.jpg"
# caption = "We approach dense per-pixel regression problems with a joint coarse-and-fine manner. We apply our method to the challenging optical flow problem explicitly combining a coarse result from pixel-wise horizontal and vertical classification problems with a fine one from regression predictions."
#caption = "We define a joint coarse-and-fine approach for standard per-pixel regression problems. We apply our method to the challenging optical flow problem explicitly combining a coarse result from pixel-wise horizontal and vertical classification problems with a fine one from regression predictions."



+++



![robot15_CargoAnts_thumbnail](/img/thumbnails/ROBOT_17_DeepLidarPuck.jpg)


