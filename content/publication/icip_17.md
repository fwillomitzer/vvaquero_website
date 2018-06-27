+++
title = "Joint Coarse-and-Fine Reasoning for Deep Optical Flow"
date = 2017-09-17T00:00:00

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Victor Vaquero", "German Ros","Francesc Moreno-Noguer", "Antonio M. Lopez","Alberto Sanfeliu"]

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
publication = "In *International Conference on Image Processing (ICIP)*, IEEE."
publication_short = "In *ICIP*"

# Abstract and optional shortened version.
abstract = "We propose a novel representation for dense pixel-wise estimation tasks using CNNs that boosts accuracy and reduces training time, by explicitly exploiting joint coarse-and-fine reasoning. The coarse reasoning is performed over a discrete classification space to obtain a general rough solution, while the fine details of the solution are obtained over a continuous regression space. In our approach both components are jointly estimated, which proved to be beneficial for improving estimation accuracy. Additionally, we propose a new  network architecture, which combines coarse and fine components by treating the fine estimation as a refinement built on top of the coarse solution, and therefore adding details to the general prediction. We apply our approach to the challenging problem of optical flow estimation and empirically validate it against state-of-the-art CNN-based solutions trained from scratch and tested on large optical flow datasets."

# Featured image thumbnail (optional)
image_preview= "icip_17_CaF/icip17_dummies.jpg"

# Is this a selected publication? (true/false)
selected = false

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#projects = ["example-external-project"]

# Links (optional).
url_pdf = "http://www.iri.upc.edu/files/scidoc/1902-Joint-coarse-and-fine-reasoning-for-deep-optical-flow.pdf"
url_preprint = "http://www.iri.upc.edu/files/scidoc/1902-Joint-coarse-and-fine-reasoning-for-deep-optical-flow.pdf"
#url_code = "#"
#url_dataset = "#"
#url_project = "#"
#url_slides = "#"
#url_video = "#"
url_poster = "#"
#url_source = "#"

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
url_custom = [{name = "IEEE", url = "https://ieeexplore.ieee.org/document/8296744/"},
              {name = "IRI", url = "http://www.iri.upc.edu/publications/show/1902"}]

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


# More detail can easily be written after "+++" using *Markdown* and $\rm \LaTeX$ math code.

# DOI: 10.1109/ICIP.2017.8296744

# {{ < shortcode SMkwqS8XPyM > }}

# testImage](static/img/ICIP17_content.jpg)

+++



![icip_thumbnail](/img/thumbnails/ICIP_17_CaF.jpg)


