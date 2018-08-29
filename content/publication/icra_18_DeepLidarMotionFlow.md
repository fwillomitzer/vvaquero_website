+++
title = "Deep Lidar CNN to Understand the Dynamics of Moving Vehicles"
date = 2018-05-21T00:00:00

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Victor Vaquero", "Alberto Sanfeliu", "Francesc Moreno-Noguer"]

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
publication = "In *International Conference on Robotics and Automation (ICRA)*."
publication_short = "In *ICRA*"

# Abstract and optional shortened version.
abstract = "Perception technologies in Autonomous Driving are experiencing their golden age due to the advances in Deep Learning. Yet, most of these systems rely on the semantically rich information of RGB images. Deep Learning solutions applied to the data of other sensors typically mounted on autonomous cars (e.g. lidars or radars) are not explored much. In this paper we propose a novel solution to understand the dynamics of moving vehicles of the scene from only lidar information. The main challenge of this problem stems from the fact that we need to disambiguate the proprio-motion of the “observer” vehicle from that of the external “observed” vehicles. For this purpose, we devise a CNN architecture which at testing time is fed with pairs of consecutive lidar scans. However, in order to properly learn the parameters of this network, during training we introduce a series of so-called pretext tasks which also leverage on image data. These tasks include semantic information about vehicleness and a novel lidar-flow feature which combines standard image-based optical flow with lidar scans. We obtain very promising results and show that including distilled image information only during training, allows improving the inference results of the network at test time, even when image data is no longer used."
abstract_short = "We propose a novel solution to understand the dynamics of moving vehicles of the scene from only lidar information. The main challenge of this problem stems from the fact that we need to disambiguate the proprio-motion of the “observer” vehicle from that of the external “observed” vehicles. For this purpose, we devise a CNN architecture which at testing time is fed with pairs of consecutive lidar scans. However, during training we introduce a series of so-called pretext tasks which also leverage on image data. These tasks include semantic information about vehicleness and a novel lidar-flow feature which combines standard image-based optical flow with lidar scans."

# Featured image thumbnail (optional)
image_preview = "icra_18_DeepLidarMotionFlow/icra_18_main.png"

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
# projects = ["deep-learning"]

# Links (optional).
url_pdf = "http://www.iri.upc.edu/files/scidoc/2018-Deep-Lidar-CNN-to-Understand-the-Dynamics-of-Moving-Vehicles.pdf"
#url_preprint = "http://eprints.soton.ac.uk/352095/1/Cushen-IMV2013.pdf"
#url_code = "#"
#url_dataset = "#"
#url_project = "#"
url_slides = "https://docs.google.com/presentation/d/1uRa97XRmTf57wvDiMR_cmLE4yKcFCh61CMz19X4Y260/present?usp=sharing"
url_video = "https://youtu.be/9jn0A_AwX_I"
url_poster = "https://drive.google.com/file/d/1DB8Q03xKdo7_XGZy4CMFIosp8WFmfyI5/view?usp=sharing"
#url_source = "#"

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
url_custom = [{name = "IRI", url = "http://www.iri.upc.edu/publications/show/2018"}]

# Does the content use math formatting?
math = true

# Does the content use source code highlighting?
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
#image = "headers/bubbles-wide.jpg"
#caption = "My caption :smile:"

+++

<!--- More detail can easily be written here using *Markdown* and $\rm \LaTeX$ math code. -->


![icra18_thumbnail](/img/thumbnails/ICRA_18_DLMF.jpg "ICRA_18_thumbnail")


<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe src="//www.youtube.com/embed/9jn0A_AwX_I" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border:0;" allowfullscreen title="YouTube Video"></iframe>
</div>

  
   
   

## **Paper Summary**


In this paper we propose a novel approach to detect the motion vector of dynamic vehicles over the ground plane by
using only lidar information. Detecting independent dynamic objects reliably from a moving platform (ego vehicle) is an
arduous task. The proprio-motion of the vehicle in which the lidar sensor is mounted needs to be disambiguated from
the actual motion of the other objects in the scene, which introduces additional difficulties.


{{< figure src="/img/icra_18_DeepLidarMotionFlow/icra_18_main.png" 
title="We present a deep learning approach that, using only lidar information, is able to estimate the ground-plane motion of the surrounding vehicles. In order to guide the learning process we introduce to our deep framework prior semantic and pixel-wise motion information, obtained from solving simpler pretext tasks, as well as odometry measurements. " >}}


We tackle this challenging problem by designing a novel
Deep Learning framework. Given two consecutive lidar scans
acquired from a moving vehicle, our approach is able to
detect the movement of the other vehicles in the scene
which have an actual motion with respect to a “ground”
fixed reference frame. During inference, our
network is only fed with lidar data, although for training
we consider a series of pretext tasks to help with solving
the problem that can potentially exploit image information.

## **Information Representation**

### Input Data 

The input of the network corresponds to a pair of lidar scans, which are
represented in 2D domains of range and reflectivity, as in our [Deep Lidar](../ecmr_17_deeplidar) paper.

![icra18_inputs](/img/icra_18_DeepLidarMotionFlow/icra_18_input_sample.png "ICRA_18_inputs")


The output we seek to learn represents the motion vectors of the
moving vehicles, colored here with the shown pattern attending to the motion angle and magnitude.

![icra18_outputs](/img/icra_18_DeepLidarMotionFlow/icra_18_output_sample.png "ICRA_18_inputs")



### Pretext tasks

We introduce a novel lidar-flow feature that
is learned by combining lidar and standard image-based
optical flow. In addition, we incorporate semantic vehicleness
information from another network trained on singe lidar
scans. Apart from these priors, we introduce knowledge
about the ego motion by providing odometry measurements
as inputs too.



{{< figure src="/img/icra_18_DeepLidarMotionFlow/icra_18_lidar_flow.png" 
caption="Lidar-flow prior, obtained by processing pairs of frames through a new learned lidar-flow net." >}}



{{< figure src="/img/icra_18_DeepLidarMotionFlow/icra_18_vehicle_segm.png" 
caption="Semantic prior, obtained by processing single frames through our vehicle lidar-detector net." >}}



### Network

Our architecture performs a concatenation
between equally sized feature maps from the contractive and
the expansive parts of the network which produce richer
representations and allows better gradient flow. In addition,
we also impose intermediate loss optimization points obtaining 
results at different resolutions which are upsampled and
concatenated to the immediate upper feature maps, guiding
the final solution from early steps and allowing the back-propagation 
of stronger and healthier gradients.

![icra18_net](/img/icra_18_DeepLidarMotionFlow/icra_18_net.png "ICRA_18_net")




### Results


We demonstrate the correct performance of our framework by
setting two different baselines, error@zero and error@mean.
The first one assumes a zero regression, so that sets all the
predictions to zero as if there were no detector. The second
baseline measures the end-point-error that a mean-motion
output would obtain.

We also measure end-point error over the real dynamic points
only. Both measurements are indicated as full and
dynamic. All the given values are calculated at test time over
the validation set only, which during the learning phase has
never been used for training neither the main network nor the
pretext tasks. Recall that during testing, the final networks
are evaluated only using lidar Data. 

{{< figure src="/img/icra_18_DeepLidarMotionFlow/icra_18_results_table.png" 
caption="Quantitative evaluation using several combination of lidar- and image-based priors. D, F , S and O respectively for models using Data, Lidar-Flow, Vehicle Segmentation and Odometry. Test is performed using only lidar inputs. Errors are measured in pixels, end-point-error. " >}}

To account for the strength of introducing optical flow as
motion knowledge for the network, we tested training with
only the lidar-flow ground truth (GT.F rows in the table) as
well as with a combination of flow ground-truth, semantics
and lidar data. Both experiments show favourable results,
being the second one the most remarkable. However, the
lidar-flow ground-truth is obtained from the optical flow
extracted using RGB images, which does not accomplish our
solo-lidar goal. We therefore perform the rest of experiments
with the learned lidar-flow (Pred.F rows in the table) as prior,
eliminating any dependence on camera images.
