+++
title = "Real Time People Detection Combining Appearance and Depth Image Spaces using Boosted Random Ferns"
date = 2015-11-14T00:00:00

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Victor Vaquero", "Michael Villamizar","Alberto Sanfeliu"]

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
publication = "In *Robot 2015: Second Iberian Robotics Conference*."
publication_short = "In *ROBOT*"

# Abstract and optional shortened version.
abstract = "This paper presents a robust and real-time method for people detection in urban and crowed environments. Unlike other conventional methods which either focus on single features or compute multiple and independent classifiers specialized in a particular feature space, the proposed approach creates a synergic combination of appearance and depth cues in a unique classifier. The core of our method is a Boosted Random Ferns classifier that selects automatically the most discriminative local binary features for both the appearance and depth image spaces. Based on this classifier, a fast and robust people detector which maintains high detection rates in spite of environmental changes is created. The proposed method has been validated in a challenging RGB-D database of people in urban scenarios and has shown that outperforms state-of-the-art approaches in spite of the difficult environment conditions. As a result, this method is of special interest for real-time robotic applications where people detection is a key matter, such as human-robot interaction or safe navigation of mobile robots for example." 
# Featured image thumbnail (optional)
image_preview= "robot_15_RGB-D/robot_15_RGB-D.png"

# Is this a selected publication? (true/false)
selected = false

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#projects = ["example-external-project"]

# Links (optional).
url_pdf = "http://www.iri.upc.edu/files/scidoc/1720-Real-time-people-detection-combining-appearance-and-depth-image-spaces-using-boosted-random-ferns..pdf"
#url_preprint = "http://www.iri.upc.edu/files/scidoc/1902-Joint-coarse-and-fine-reasoning-for-deep-optical-flow.pdf"
#url_code = "#"
#url_dataset = "#"
url_project = "/publication/robot_15_rgbd/"
url_slides = "https://drive.google.com/file/d/1eF5NY2ktlylbNizuRByk97dM-GgT5ER7/view?usp=sharing"
url_video = "https://youtu.be/CKs2qIrk2KA"
#url_poster = "#"
#url_source = "#"

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
url_custom = [{name = "SPRINGER", url = "https://link.springer.com/chapter/10.1007/978-3-319-27149-1_45"},
              {name = "IRI", url = "http://www.iri.upc.edu/publications/show/1720"}]

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



![robot15_CargoAnts_thumbnail](/img/thumbnails/Robot_15_RGBD.jpg)


<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe src="//www.youtube.com/embed/CKs2qIrk2KA" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border:0;" allowfullscreen title="YouTube Video"></iframe>
</div>

___
      
**Acknowledgements:** 
This work has been partially funded by the EU project
CargoANTs FP7-SST-2013-605598 and the Spanish CICYT project DPI2013-
42458-P.
