# MIT Perception and Localization Seminar

At Massachusetts Institute of Technlology, we run the Perception and Localization Seminar (PALS), which features a mix of reading groups, presentations, and seminars from authors of recent or impactful papers in perception and localization. This repository includes a list of papers that we have reviewed or hosted authors to present. 

If you have any suggestions, want to chat, or are interested in presenting, feel free to reach out!

<br>

## February 2024:
### 1. [RSS '22] Hydra: a Real-time Spatial Perception System for 3D Scene Graph Construction and Optimization
**Authors**: Nathan Hughes, Yun Chang, Luca Carlone
<details span>
<summary><b>Abstract</b></summary>
3D scene graphs have recently emerged as a powerful high-level representation of 3D environments. A 3D scene graph describes the environment as a layered graph where nodes represent spatial concepts at multiple levels of abstraction and edges represent relations between concepts. While 3D scene graphs can serve as an advanced "mental model" for robots, how to build such a rich representation in real-time is still uncharted territory. This paper describes a real-time Spatial Perception System, a suite of algorithms to build a 3D scene graph from sensor data in real-time. Our first contribution is to develop real-time algorithms to incrementally construct the layers of a scene graph as the robot explores the environment; these algorithms build a local Euclidean Signed Distance Function (ESDF) around the current robot location, extract a topological map of places from the ESDF, and then segment the places into rooms using an approach inspired by community-detection techniques. Our second contribution is to investigate loop closure detection and optimization in 3D scene graphs. We show that 3D scene graphs allow defining hierarchical descriptors for loop closure detection; our descriptors capture statistics across layers in the scene graph, ranging from low-level visual appearance to summary statistics about objects and places. We then propose the first algorithm to optimize a 3D scene graph in response to loop closures; our approach relies on embedded deformation graphs to simultaneously correct all layers of the scene graph. We implement the proposed Spatial Perception System into a architecture named Hydra, that combines fast early and mid-level perception processes with slower high-level perception. We evaluate Hydra on simulated and real data and show it is able to reconstruct 3D scene graphs with an accuracy comparable with batch offline methods despite running online.
</details>

  [📄 Paper](https://arxiv.org/abs/2201.13360) | [💻 Code](https://github.com/MIT-SPARK/Hydra) 

<br>
  
## March 2024:
### 1. [CVPR '24] SplaTAM: Splat, Track & Map 3D Gaussians for Dense RGB-D SLAM
**Authors**: Nikhil Keetha, Jay Karhade, Krishna Murthy Jatavallabhula, Gengshan Yang, Sebastian Scherer, Deva Ramanan, Jonathon Luiten
<details span>
<summary><b>Abstract</b></summary>
Dense simultaneous localization and mapping (SLAM) is crucial for robotics and augmented reality applications. However, current methods are often hampered by the non-volumetric or implicit way they represent a scene. This work introduces SplaTAM, an approach that, for the first time, leverages explicit volumetric representations, i.e., 3D Gaussians, to enable high-fidelity reconstruction from a single unposed RGB-D camera, surpassing the capabilities of existing methods. SplaTAM employs a simple online tracking and mapping system tailored to the underlying Gaussian representation. It utilizes a silhouette mask to elegantly capture the presence of scene density. This combination enables several benefits over prior representations, including fast rendering and dense optimization, quickly determining if areas have been previously mapped, and structured map expansion by adding more Gaussians. Extensive experiments show that SplaTAM achieves up to 2x superior performance in camera pose estimation, map construction, and novel-view synthesis over existing methods, paving the way for more immersive high-fidelity SLAM applications.
</details>

  [📄 Paper](https://arxiv.org/abs/2312.02126) | [🌐 Project Page](https://spla-tam.github.io/) | [💻 Code](https://github.com/spla-tam/SplaTAM) 

### 2. [ICRA '23] Asynchronous Distributed Smoothing and Mapping via On-Manifold Consensus ADMM 
**Authors**: Daniel McGann, Kyle Lassak, Michael Kaess
<details span>
<summary><b>Abstract</b></summary>
In this paper we present a fully distributed, asynchronous, and general purpose optimization algorithm for Consensus Simultaneous Localization and Mapping (CSLAM). Multi-robot teams require that agents have timely and accurate solutions to their state as well as the states of the other robots in the team. To optimize this solution we develop a CSLAM back-end based on Consensus ADMM called MESA (Manifold, Edge-based, Separable ADMM). MESA is fully distributed to tolerate failures of individual robots, asynchronous to tolerate communication delays and outages, and general purpose to handle any CSLAM problem formulation. We demonstrate that MESA exhibits superior convergence rates and accuracy compare to existing state-of-the art CSLAM back-end optimizers.
</details>

  [📄 Paper](https://ieeexplore.ieee.org/abstract/document/10611193?casa_token=zPSd_elnbaMAAAAA:IFFWJm0zPz3oaXuIO-freATm0Z3zcLfhw5DoH8VK3NnBKLncs9TDD77I1Z-3El2G4llSzK-LGA) | [💻 Code](https://github.com/rpl-cmu/mesa)

<br>

## April 2024:
### 1. [ICCV '09] Building Rome in a Day
**Authors**: y Sameer Agarwala, Yasutaka Furukawaa, Noah Snavely, Ian Simonb, Brian Curless, Steven M. Seitz, Richard Szeliski
<details span>
<summary><b>Abstract</b></summary>
We present a system that can reconstruct 3D geometry from large, unorganized collections of photographs such as those found by searching for a given city (e.g., Rome) on Internet photo-sharing sites. Our system is built on a set of new, distributed computer vision algorithms for image matching and 3D reconstruction, designed to maximize parallelism at each stage of the pipeline and to scale gracefully with both the size of the problem and the amount of available computation. Our experimental results demonstrate that it is now possible to reconstruct city-scale image collections with more than a hundred thousand images in less than a day.
</details>

[📄 Paper](https://grail.cs.washington.edu/rome/rome_paper.pdf) | [🌐 Project Page](https://grail.cs.washington.edu/rome/) | [💻 Code](https://phototour.cs.washington.edu/)


### 2. [ICRA '24] VOOM: Robust Visual Object Odometry and Mapping using Hierarchical Landmarks
**Authors**: Yutong Wang, Chaoyang Jiang, Xieyuanli Chen
<details span>
<summary><b>Abstract</b></summary>
In recent years, object-oriented simultaneous localization and mapping (SLAM) has attracted increasing attention due to its ability to provide high-level semantic information while maintaining computational efficiency. Some researchers have attempted to enhance localization accuracy by integrating the modeled object residuals into bundle adjustment. However, few have demonstrated better results than feature-based visual SLAM systems, as the generic coarse object models, such as cuboids or ellipsoids, are less accurate than feature points. In this paper, we propose a Visual Object Odometry and Mapping framework VOOM using high-level objects and low-level points as the hierarchical landmarks in a coarse-to-fine manner instead of directly using object residuals in bundle adjustment. Firstly, we introduce an improved observation model and a novel data association method for dual quadrics, employed to represent physical objects. It facilitates the creation of a 3D map that closely reflects reality. Next, we use object information to enhance the data association of feature points and consequently update the map. In the visual object odometry backend, the updated map is employed to further optimize the camera pose and the objects. Meanwhile, local bundle adjustment is performed utilizing the objects and points-based covisibility graphs in our visual object mapping process. Experiments show that VOOM outperforms both object-oriented SLAM and feature points SLAM systems such as ORB-SLAM2 in terms of localization.
</details>

[📄 Paper](https://arxiv.org/abs/2402.13609) | [💻 Code](https://github.com/yutongwangBIT/VOOM)

<br>

## May 2024:
### 1. [CVPR '23] SeqTrack: Sequence to Sequence Learning for Visual Object Tracking 
**Authors**: Xin Chen, Houwen Peng, Dong Wang, Huchuan Lu, Han Hu
<details span>
<summary><b>Abstract</b></summary>
In this paper, we present a new sequence-to-sequence learning framework for visual tracking, dubbed SeqTrack. It casts visual tracking as a sequence generation problem, which predicts object bounding boxes in an autoregressive fashion. This is different from prior Siamese trackers and transformer trackers, which rely on designing complicated head networks, such as classification and regression heads. SeqTrack only adopts a simple encoder-decoder transformer architecture. The encoder extracts visual features with a bidirectional transformer, while the decoder generates a sequence of bounding box values autoregressively with a causal transformer. The loss function is a plain cross-entropy. Such a sequence learning paradigm not only simplifies tracking framework, but also achieves competitive performance on benchmarks. For instance, SeqTrack gets 72.5% AUC on LaSOT, establishing a new state-of-the-art performance.
</details>

  [📄 Paper](https://openaccess.thecvf.com/content/CVPR2023/html/Chen_SeqTrack_Sequence_to_Sequence_Learning_for_Visual_Object_Tracking_CVPR_2023_paper.html) | [💻 Code](https://github.com/chenxin-dlut/SeqTrackv2)

<br>

## June 2024:
### 1. [RSS '14] Batch Continuous-Time Trajectory Estimation as Exactly Sparse Gaussian Process Regression 
**Authors**: Sean Anderson, Timothy D. Barfoot, Chi Hay Tong, Simo Särkkä
<details span>
<summary><b>Abstract</b></summary>
In this paper, we revisit batch state estimation
through the lens of Gaussian process (GP) regression. We consider
continuous-discrete estimation problems wherein a trajectory is
viewed as a one-dimensional GP, with time as the independent
variable. Our continuous-time prior can be defined by any linear,
time-varying stochastic differential equation driven by white
noise; this allows the possibility of smoothing our trajectory
estimates using a variety of vehicle dynamics models (e.g.,
‘constant-velocity’). We show that this class of prior results in an
inverse kernel matrix (i.e., covariance matrix between all pairs
of measurement times) that is exactly sparse (block-tridiagonal)
and that this can be exploited to carry out GP regression (and
interpolation) very efficiently. Though the prior is continuous,
we consider measurements to occur at discrete times. When the
measurement model is also linear, this GP approach is equivalent
to classical, discrete-time smoothing (at the measurement times).
When the measurement model is nonlinear, we iterate over
the whole trajectory (as is common in vision and robotics) to
maximize accuracy. We test the approach experimentally on a
simultaneous trajectory estimation and mapping problem using
a mobile robot dataset.
</details>

  [📄 Paper](https://www.roboticsproceedings.org/rss10/p01.pdf)

### 2. [ICRA '24] nvblox: GPU-Accelerated Incremental Signed Distance Field Mapping
**Authors**: Alexander Millane, Helen Oleynikova, Emilie Wirbel, Remo Steiner, Vikram Ramasamy, David Tingdahl, Roland Siegwart
<details span>
<summary><b>Abstract</b></summary>
Dense, volumetric maps are essential to enable robot navigation and interaction with the environment. To achieve low latency, dense maps are typically computed onboard the robot, often on computationally constrained hardware. Previous works leave a gap between CPU-based systems for robotic mapping which, due to computation constraints, limit map resolution or scale, and GPU-based reconstruction systems which omit features that are critical to robotic path planning, such as computation of the Euclidean Signed Distance Field (ESDF). We introduce a library, nvblox, that aims to fill this gap, by GPU-accelerating robotic volumetric mapping. Nvblox delivers a significant performance improvement over the state of the art, achieving up to a 177x speed-up in surface reconstruction, and up to a 31x improvement in distance field computation, and is available open-source.
</details>

  [📄 Paper](https://arxiv.org/abs/2311.00626) | [💻 Code](https://github.com/nvidia-isaac/nvblox)

### 3. [TRO '20] Characterizing the Uncertainty of Jointly Distributed Poses in the Lie Algebra 
**Authors**: Joshua G. Mangelson, Maani Ghaffari, Ram Vasudevan, Ryan M. Eustice
<details span>
<summary><b>Abstract</b></summary>
An accurate characterization of pose uncertainty is essential for safe autonomous navigation. Early pose uncertainty characterization methods proposed by Smith, Self, and Cheeseman (SCC), used coordinate-based first-order methods to propagate uncertainty through non-linear functions such as pose composition (head-to-tail), pose inversion, and relative pose extraction (tail-to-tail). Characterizing uncertainty in the Lie Algebra of the special Euclidean group results in better uncertainty estimates. However, existing approaches assume that individual poses are independent. Since factors in a pose graph induce correlation, this independence assumption is usually not reflected in reality. In addition, prior work has focused primarily on the pose composition operation. This paper develops a framework for modeling the uncertainty of jointly distributed poses and describes how to perform the equivalent of the SSC pose operations while characterizing uncertainty in the Lie Algebra. Evaluation on simulated and open-source datasets shows that the proposed methods result in more accurate uncertainty estimates. An accompanying C++ library implementation is also released.
</details>

  [📄 Paper](https://arxiv.org/abs/1906.07795)  

<br>

## July 2024:
### 1. [ICRA '24] Censible: A Robust and Practical Global Localization Framework for Planetary Surface Missions
**Authors**:  Wojciech Zielonka, Timur Bagautdinov, Shunsuke Saito, Michael Zollhöfer, Justus Thies, Javier Romero
<details span>
<summary><b>Abstract</b></summary>
To achieve longer driving distances, planetary
robotics missions require accurate localization to counteract
position uncertainty. Freedom and precision in driving allows
scientists to reach and study sites of interest. Typically, rover
global localization has been performed manually by humans,
which is accurate but time-consuming as data is relayed between
planets. This paper describes a global localization algorithm
that is run onboard the Perseverance Mars rover. Our approach matches rover images to orbital maps using a modified
census transform to achieve sub-meter accurate, near-human
localization performance on a real dataset of 264 Mars rover
panoramas. The proposed solution has also been successfully
executed on the Perseverance Mars Rover, demonstrating the
practicality of our approach.
</details>

  [📄 Paper](https://www-robotics.jpl.nasa.gov/media/documents/2024_Global_Localization_ICRA.pdf)

### 2. [CVPR '23] BundleSDF: Neural 6-DoF Tracking and 3D Reconstruction of Unknown Objects
**Authors**: Bowen Wen, Jonathan Tremblay, Valts Blukis, Stephen Tyree, Thomas Muller, Alex Evans, Dieter Fox, Jan Kautz, Stan Birchfield
<details span>
<summary><b>Abstract</b></summary>
We present a near real-time method for 6-DoF tracking of an unknown object from a monocular RGBD video sequence, while simultaneously performing neural 3D reconstruction of the object. Our method works for arbitrary rigid objects, even when visual texture is largely absent. The object is assumed to be segmented in the first frame only. No additional information is required, and no assumption is made about the interaction agent. Key to our method is a Neural Object Field that is learned concurrently with a pose graph optimization process in order to robustly accumulate information into a consistent 3D representation capturing both geometry and appearance. A dynamic pool of posed memory frames is automatically maintained to facilitate communication between these threads. Our approach handles challenging sequences with large pose changes, partial and full occlusion, untextured surfaces, and specular highlights. We show results on HO3D, YCBInEOAT, and BEHAVE datasets, demonstrating that our method significantly outperforms existing approaches. 
</details>

  [📄 Paper](https://arxiv.org/abs/2303.14158) |  [🌐 Project Page](https://bundlesdf.github.io/) | [💻 Code](https://github.com/NVlabs/BundleSDF)

### 3. [RAL '24] Clio: Real-time Task-Driven Open-Set 3D Scene Graphs
**Authors**: Dominic Maggio, Yun Chang, Nathan Hughes, Matthew Trang, Dan Griffith, Carlyn Dougherty, Eric Cristofalo, Lukas Schmid, Luca Carlone
<details span>
<summary><b>Abstract</b></summary>
Modern tools for class-agnostic image segmentation (e.g., SegmentAnything) and open-set semantic understanding (e.g., CLIP) provide unprecedented opportunities for robot perception and mapping. While traditional closed-set metric-semantic maps were restricted to tens or hundreds of semantic classes, we can now build maps with a plethora of objects and countless semantic variations. This leaves us with a fundamental question: what is the right granularity for the objects (and, more generally, for the semantic concepts) the robot has to include in its map representation? While related work implicitly chooses a level of granularity by tuning thresholds for object detection, we argue that such a choice is intrinsically task-dependent. The first contribution of this paper is to propose a task-driven 3D scene understanding problem, where the robot is given a list of tasks in natural language and has to select the granularity and the subset of objects and scene structure to retain in its map that is sufficient to complete the tasks. We show that this problem can be naturally formulated using the Information Bottleneck (IB), an established information-theoretic framework. The second contribution is an algorithm for task-driven 3D scene understanding based on an Agglomerative IB approach, that is able to cluster 3D primitives in the environment into task-relevant objects and regions and executes incrementally. The third contribution is to integrate our task-driven clustering algorithm into a real-time pipeline, named Clio, that constructs a hierarchical 3D scene graph of the environment online using only onboard compute, as the robot explores it. Our final contribution is an extensive experimental campaign showing that Clio not only allows real-time construction of compact open-set 3D scene graphs, but also improves the accuracy of task execution by limiting the map to relevant semantic concepts.
</details>

  [📄 Paper](https://arxiv.org/abs/2404.13696)

<br>

## August 2024:
### 1. [IJRR '17] Analytical SLAM Without Linearization
**Authors**:  Feng Tan, Winfried Lohmiller, Jean-Jacques Slotine
<details span>
<summary><b>Abstract</b></summary>
This paper solves the classical problem of simultaneous localization and mapping (SLAM) in a fashion which avoids linearized approximations altogether. Based on creating virtual synthetic measurements, the algorithm uses a linear time- varying (LTV) Kalman observer, bypassing errors and approximations brought by the linearization process in traditional extended Kalman filtering (EKF) SLAM. Convergence rates of the algorithm are established using contraction analysis. Different combinations of sensor information can be exploited, such as bearing measurements, range measurements, optical flow, or time-to-contact. As illustrated in simulations, the proposed algorithm can solve SLAM problems in both 2D and 3D scenarios with guaranteed convergence rates in a full nonlinear context.
</details>

  [📄 Paper](https://arxiv.org/abs/1512.08829)

### 2. SlideSLAM: Sparse, Lightweight, Decentralized Metric-Semantic SLAM for Multi-Robot Navigation
**Authors**: Xu Liu, Jiuzhou Lei, Ankit Prabhu, Yuezhan Tao, Igor Spasojevic, Pratik Chaudhari, Nikolay Atanasov, Vijay Kumar
<details span>
<summary><b>Abstract</b></summary>
We present a near real-time method for 6-DoF tracking of an unknown object from a monocular RGBD video sequence, while simultaneously performing neural 3D reconstruction of the object. Our method works for arbitrary rigid objects, even when visual texture is largely absent. The object is assumed to be segmented in the first frame only. No additional information is required, and no assumption is made about the interaction agent. Key to our method is a Neural Object Field that is learned concurrently with a pose graph optimization process in order to robustly accumulate information into a consistent 3D representation capturing both geometry and appearance. A dynamic pool of posed memory frames is automatically maintained to facilitate communication between these threads. Our approach handles challenging sequences with large pose changes, partial and full occlusion, untextured surfaces, and specular highlights. We show results on HO3D, YCBInEOAT, and BEHAVE datasets, demonstrating that our method significantly outperforms existing approaches. 
</details>

  [📄 Paper](https://arxiv.org/abs/2406.17249) |  [🌐 Project Page](https://xurobotics.github.io/slideslam/) | [💻 Code](https://github.com/KumarRobotics/SLIDE_SLAM)

### 3. [RAL '24] 3D Active Metric-Semantic SLAM
**Authors**: Yuezhan Tao, Xu Liu, Igor Spasojevic, Saurav Agarwal, Vijay Kumar
<details span>
<summary><b>Abstract</b></summary>
In this letter, we address the problem of exploration
and metric-semantic mapping of multi-floor GPS-denied indoor
environments using Size Weight and Power (SWaP) constrained
aerial robots.Most previous work in exploration assumes that robot
localization is solved. However, neglecting the state uncertainty
of the agent can ultimately lead to cascading errors both in the
resulting map and in the state of the agent itself. Furthermore,
actions that reduce localization errors may be at direct odds with
the exploration task.We develop a framework that balances the efficiency of exploration with actions that reduce the state uncertainty
of the agent. In particular, our algorithmic approach for active
metric-semantic SLAM is built upon sparse information abstracted
from raw problem data, to make it suitable for SWaP-constrained
robots. Furthermore, we integrate this framework within a fully
autonomous aerial robotic system that achieves autonomous exploration in cluttered, 3D environments. From extensive real-world
experiments, we showed that by including Semantic Loop Closure
(SLC), we can reduce the robot pose estimation errors by over 90%
in translation and approximately 75% in yaw, and the uncertainties
in pose estimates and semantic maps by over 70% and 65%,
respectively. Although discussed in the context of indoor multi-floor
exploration, our system can be used for various other applications,
such as infrastructure inspection and precision agriculture where
reliable GPS data may not be available.
</details>

  [📄 Paper](https://arxiv.org/pdf/2309.06950)

### 4. [ICRA '23] Active Metric-Semantic Mapping by Multiple Aerial Robots
**Authors**: Xu Liu, Ankit Prabhu, Fernando Cladera, Ian D. Miller, Lifeng Zhou, Camillo J. Taylor
<details span>
<summary><b>Abstract</b></summary>
Traditional approaches for active mapping focus on building geometric maps. For most real-world applications, however, actionable information is related to semantically meaningful objects in the environment. We propose an approach to the active metric-semantic mapping problem that enables multiple heterogeneous robots to collaboratively build a map of the environment. The robots actively explore to minimize the uncertainties in both semantic (object classification) and geometric (object modeling) information. We represent the environment using informative but sparse object models, each consisting of a basic shape and a semantic class label, and characterize uncertainties empirically using a large amount of real-world data. Given a prior map, we use this model to select actions for each robot to minimize uncertainties. The performance of our algorithm is demonstrated through multi-robot experiments in diverse real-world environments. The proposed framework is applicable to a wide range of real-world problems, such as precision agriculture, infrastructure inspection, and asset mapping in factories.
</details>

  [📄 Paper](https://ieeexplore.ieee.org/abstract/document/10161564) | [🌐 Project Page](https://www.cis.upenn.edu/~leijh/projects/gart/) | [💻 Code](https://github.com/JiahuiLei/GART) | [🎥 Short Presentation](https://www.youtube.com/watch?v=-xYNtIlW4WY)

### 5. [RAL '22] Large-Scale Autonomous Flight with Real-time Semantic SLAM under Dense Forest Canopy
**Authors**: Xu Liu, Guilherme V. Nardari, Fernando Cladera Ojeda, Yuezhan Tao, Alex Zhou, Thomas Donnelly, Chao Qu, Steven W. Chen, Roseli A. F. Romero, Camillo J. Taylor
<details span>
<summary><b>Abstract</b></summary>
Semantic maps represent the environment using a set of semantically meaningful objects. This representation is storage-efficient, less ambiguous, and more informative, thus facilitating large-scale autonomy and the acquisition of actionable information in highly unstructured, GPS-denied environments. In this letter, we propose an integrated system that can perform large-scale autonomous flights and real-time semantic mapping in challenging under-canopy environments. We detect and model tree trunks and ground planes from LiDAR data, which are associated across scans and used to constrain robot poses as well as tree trunk models. The autonomous navigation module utilizes a multi-level planning and mapping framework and computes dynamically feasible trajectories that lead the UAV to build a semantic map of the user-defined region of interest in a computationally and storage efficient manner. A drift-compensation mechanism is designed to minimize the odometry drift using semantic SLAM outputs in real time, while maintaining planner optimality and controller stability. This leads the UAV to execute its mission accurately and safely at scale.
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.17113.pdf) | [🌐 Project Page](https://perezpellitero.github.io/projects/hugs/index.html) | [🎥 Short Presentation](https://www.youtube.com/watch?v=R3CHg46SIfo)

### 6. [CVPR '21] Back to the Feature: Learning Robust Camera Localization from Pixels to Pose
**Authors**: Paul-Edouard Sarlin, Ajaykumar Unagar, Mans Larsson, Hugo Germain, Carl Toft, Viktor Larsson, Marc Pollefeys, Vincent Lepetit, Lars Hammarstrand, Fredrik Kahl, Torsten Sattler
<details span>
<summary><b>Abstract</b></summary>
Camera pose estimation in known scenes is a 3D geometry task recently tackled by multiple learning algorithms. Many regress precise geometric quantities, like poses or 3D points, from an input image. This either fails to generalize to new viewpoints or ties the model parameters to a specific scene. In this paper, we go Back to the Feature: we argue that deep networks should focus on learning robust and invariant visual features, while the geometric estimation should be left to principled algorithms. We introduce PixLoc, a scene-agnostic neural network that estimates an accurate 6-DoF pose from an image and a 3D model. Our approach is based on the direct alignment of multiscale deep features, casting camera localization as metric learning. PixLoc learns strong data priors by end-to-end training from pixels to pose and exhibits exceptional generalization to new scenes by separating model parameters and scene geometry. The system can localize in large environments given coarse pose priors but also improve the accuracy of sparse feature matching by jointly refining keypoints and poses with little overhead.
</details>

  [📄 Paper](https://openaccess.thecvf.com/content/CVPR2021/html/Sarlin_Back_to_the_Feature_Learning_Robust_Camera_Localization_From_Pixels_CVPR_2021_paper.html) | [💻 Code](https://github.com/cvg/pixloc)

<br>

## September 2024:
### 1. [RAL '24] Adaptive Global Graph Optimization for LiDAR-Inertial SLAM
**Authors**: Fengtian Lang, Ruiye Ming, Zikang Yuan, Xuemiao Xu, Kai Wu, Xin Yang

 ***Comment:***: ICRA '24

<details span>
<summary><b>Abstract</b></summary>
A complete SLAM system comprises a front-end
odometry module and a back-end optimization module. The frontend utilizes sensor data (such as from cameras or LiDAR) to
estimate the robot’s pose and construct a map of the surrounding
environment. Meanwhile, the task of the back-end is to determine
whether the robot has revisited a previously encountered location
and optimize the trajectory by incorporating loop constraints to
enhance positioning accuracy. However, existing back-end loop
detection methods typically use fixed weights when incorporating
odometry and loop closure constraints. This results in the backend optimization overlooking the varying accuracy of sensor data
across different scenarios, consequently neglecting the precision of
pose estimation and loop detection.To address this, this letter introduces a dynamic-weight estimation algorithm based on information
from the sensors and loop detection. By leveraging the reliability
of LiDAR, IMU and loop detection, this algorithm calculates the
dynamic weight of graph optimization edges. Experimental results
on two public datasets demonstrate that our SLAM system outperforms all state-of-the-art methods in accuracy. Furthermore,
the proposed dynamic-weight estimation algorithm enhances the
accuracy of back-end state optimization
</details>

[📄 Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10679917) 

### 2. [IROS '24] SOS-Match: Segmentation for Open-Set Robust Correspondence Search and Robot Localization in Unstructured Environments
**Authors**: Annika Thomas, Jouko Kinnari, Parker Lusk, Kota Kondo, Jonathan P How

 ***Comment:***: IROS '24

<details span>
<summary><b>Abstract</b></summary>
We present SOS-Match, a novel framework for detecting and matching objects in unstructured environments. Our system consists of 1) a front-end mapping pipeline using a zero-shot segmentation model to extract object masks from images and track them across frames and 2) a frame alignment pipeline that uses the geometric consistency of object relationships to efficiently localize across a variety of conditions. We evaluate SOS-Match on the Batvik seasonal dataset which includes drone flights collected over a coastal plot of southern Finland during different seasons and lighting conditions. Results show that our approach is more robust to changes in lighting and appearance than classical image feature-based approaches or global descriptor methods, and it provides more viewpoint invariance than learning-based feature detection and description approaches. SOS-Match localizes within a reference map up to 46x faster than other feature-based approaches and has a map size less than 0.5% the size of the most compact other maps. SOS-Match is a promising new approach for landmark detection and correspondence search in unstructured environments that is robust to changes in lighting and appearance and is more computationally efficient than other approaches, suggesting that the geometric arrangement of segments is a valuable localization cue in unstructured environments.
</details>

[📄 Paper](https://arxiv.org/abs/2401.04791) | [🌐 Project Page](https://acl.mit.edu/SOS-Match/) 


<br>

## October 2024:
### 1. [RAL '23] PADLoC: LiDAR-Based Deep Loop Closure Detection and Registration Using Panoptic Attention
**Authors**: José Arce, Niclas Vödisch, Daniele Cattaneo, Wolfram Burgard, Abhinav Valada

<details span>
<summary><b>Abstract</b></summary>
A key component of graph-based SLAM systems is
the ability to detect loop closures in a trajectory to reduce the
drift accumulated over time from the odometry.Most LiDAR-based
methods achieve this goal by using only the geometric information,
disregarding the semantics of the scene. In this work, we introduce
PADLoC for joint loop closure detection and registration in LiDARbased SLAM frameworks. We propose a novel transformer-based
head for point cloud matching and registration, and to leverage
panoptic information during training time. In particular, we propose a novel loss function that reframes the matching problem
as a classification task for the semantic labels and as a graph
connectivity assignment for the instance labels. During inference,
PADLoC does not require panoptic annotations, making it more
versatile than other methods. Additionally, we show that using two
shared matching and registration heads with their source and target inputs swapped increases the overall performance by enforcing
forward-backward consistency. We perform extensive evaluations
of PADLoC on multiple real-world datasets demonstrating that it
achieves state-of-the-art results.
</details>

[📄 Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10024875&tag=1) 

### 2. KISS-Matcher: Fast and Robust Point Cloud Registration Revisited
**Authors**: Hyungtae Lim, Daebeom Kim, Gunhee Shin, Jingnan Shi, Ignacio Vizzo, Hyun Myung, Jaesik Park, Luca Carlone

<details span>
<summary><b>Abstract</b></summary>
While global point cloud registration systems have advanced significantly in all aspects, many studies have focused on specific components, such as feature extraction, graph-theoretic pruning, or pose solvers. In this paper, we take a holistic view on the registration problem and develop an open-source and versatile C++ library for point cloud registration, called \textit{KISS-Matcher}. KISS-Matcher combines a novel feature detector, \textit{Faster-PFH}, that improves over the classical fast point feature histogram (FPFH). Moreover, it adopts a k-core-based graph-theoretic pruning to reduce the time complexity of rejecting outlier correspondences. Finally, it combines these modules in a complete, user-friendly, and ready-to-use pipeline. As verified by extensive experiments, KISS-Matcher has superior scalability and broad applicability, achieving a substantial speed-up compared to state-of-the-art outlier-robust registration pipelines while preserving accuracy.
</details>

[📄 Paper](https://arxiv.org/abs/2409.15615) | [💻 Code (not yet)](https://github.com/MIT-SPARK/KISS-Matcher)


### 3. [IROS '24] GSLoc: Visual Localization with 3D Gaussian Splatting
**Authors**: Kazii Botashev, Vladislav Pyatov, Gonzalo Ferre, Stamatios Lefkimmiatis

<details span>
<summary><b>Abstract</b></summary>
We present GSLoc: a new visual localization method that performs dense camera alignment using 3D Gaussian Splatting as a map representation of the scene. GSLoc backpropagates pose gradients over the rendering pipeline to align the rendered and target images, while it adopts a coarse-to-fine strategy by utilizing blurring kernels to mitigate the non-convexity of the problem and improve the convergence. The results show that our approach succeeds at visual localization in challenging conditions of relatively small overlap between initial and target frames inside textureless environments when state-of-the-art neural sparse methods provide inferior results. Using the byproduct of realistic rendering from the 3DGS map representation, we show how to enhance localization results by mixing a set of observed and virtual reference keyframes when solving the image retrieval problem. We evaluate our method both on synthetic and real-world data, discussing its advantages and application potential.
</details>

[📄 Paper](https://ieeexplore.ieee.org/abstract/document/10801919)

<br>

## November 2024
### 1. CogExplore: Contextual Exploration with Language-Encoded Environment Representations
**Authors**: Harel Biggie, Patrick Cooper, Doncey Albin, Kristen Such, Christoffer Heckman

<details span>
<summary><b>Abstract</b></summary>
Integrating language models into robotic exploration frameworks improves performance in unmapped environments by providing the ability to reason over semantic groundings, contextual cues, and temporal states. The proposed method employs large language models (GPT-3.5 and Claude Haiku) to reason over these cues and express that reasoning in terms of natural language, which can be used to inform future states. We are motivated by the context of search-and-rescue applications where efficient exploration is critical. We find that by leveraging natural language, semantics, and tracking temporal states, the proposed method greatly reduces exploration path distance and further exposes the need for environment-dependent heuristics. Moreover, the method is highly robust to a variety of environments and noisy vision detections, as shown with a 100% success rate in a series of comprehensive experiments across three different environments conducted in a custom simulation pipeline operating in Unreal Engine.
</details>

[📄 Paper](https://arxiv.org/abs/2406.17180) 

<br>

## December 2024
### 1. [RAL '24] MVINS: A Magnetism&Vision Aided Inertial Navigation System for Autonomous Underwater Vehicles
**Authors**: Bingbing Zhang, Shuo Liu, Daxiong Ji, Tao Wang, Shanmin Zhou, Zhengfei Wang, Xiaokang Qi, Wen Xu

<details span>
<summary><b>Abstract</b></summary>
We present a robust underwater navigation system
that integrates magnetic, visual, and inertial measurements
from commercial off-the-shelf sensors. Visual Inertial Navigation
Systems (VINS) face challenges when used for Autonomous
Underwater Vehicle (AUV) localization in perceptually degraded
environments. First, traditional VINS methods struggle to accurately detect sufficient loops due to several factors: feature
scarcity, environmental similarities, limited visibility, orientation
changes, and constrained computational resources. Second, the
yaw is unobservable in VINS and it may drift rapidly without
distinct features. To address these issues, we propose a novel
system that enhances loop closure by fusing magnetic signatures
from a low-cost alternating magnetic field coil with multi-scale
mapping and hierarchical place recognition. Additionally, we
utilize geomagnetic fields to align feature descriptors, improving
robustness to orientation variations. Our system also refines yaw
estimations by leveraging geomagnetic data, aligning them with
global references to mitigate drift. Experimental results validate
the improved performance of the proposed system
</details>

[📄 Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10778419&tag=1) 

## Credits

- Thanks to [Aneesa Sonawalla](https://www.linkedin.com/in/aneesa-sonawalla-827b1775/) and [Mason Peterson](https://www.linkedin.com/in/mason-burgon-peterson/) for co-organizing this seminar group with me. 
- Thanks to our presenters, [Nathan Hughes](https://www.linkedin.com/in/nathan-hughes-79abb4ab/), [Nikhil Keetha](https://www.linkedin.com/in/nik-v9/), [Dominic Maggio](https://www.linkedin.com/in/dominic-maggio-050034158/), [Xu Liu](https://www.linkedin.com/in/xu-liu-1124032b0/), [Annika Thomas](https://www.linkedin.com/in/annika-thomas/), [Hyungtae Lim](https://www.linkedin.com/in/hyungtae-lim-34b8a015a/), and [Harel Biggie](https://www.linkedin.com/in/harelb/).
- Thanks to our reading group leaders, [Aneesa Sonawalla](https://www.linkedin.com/in/aneesa-sonawalla-827b1775/), [Mason Peterson](https://www.linkedin.com/in/mason-burgon-peterson/), [Annika Thomas](https://www.linkedin.com/in/annika-thomas/), Lucas Jia, [Lorenzo Shaikewitz](https://www.linkedin.com/in/lorenzo-shaikewitz/), and [Hannah Shafferman](https://www.linkedin.com/in/hannah-shafferman-17962b18b/).
