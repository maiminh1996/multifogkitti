## Multifog KITTI dataset: *3D Object Detection with SLS-Fusion Network in Foggy Weather Conditions*
Created by <a href="maiminh1996.github.io/" target="_blank">Nguyen Anh Minh MAI</a>, <a href="https://www.researchgate.net/profile/Pierre-Duthon" target="_blank">Pierre Duthon</a>, <a href="https://www.researchgate.net/profile/Louahdi-Khoudour" target="_blank">Louahdi Khoudour</a>, <a href="https://www.irit.fr/~Alain.Crouzil/" target="_blank">Alain Crouzil</a>, <a href="https://scholar.google.com/citations?user=FsE86kwAAAAJ&hl=en&oi=ao" target="_blank">Sergio A. Velastin</a>.

![prediction example](/docs/sensors.png)

### Introduction

This work is based on our [paper](https://doi.org/10.3390/s21206711), which is published in SENSORS. We proposed a novel synthetic dataset augmented on KITTI dataset for foggy weather conditions. You can also check our [project webpage](https://maiminh1996.github.io/multifogkitti/) for a deeper introduction.

The role of sensors such as cameras or LiDAR (Light Detection and Ranging) is crucial for the environmental awareness of self-driving cars. However, the data collected from these sensors are subject to distortions in extreme weather conditions such as fog, rain, and snow. This issue could lead to many safety problems while operating a self-driving vehicle. The purpose of this study is to analyze the effects of fog on the detection of objects in driving scenes and then to propose methods for improvement. Collecting and processing data in adverse weather conditions is often more difficult than data in good weather conditions. Hence, a synthetic dataset that can simulate bad weather conditions is a good choice to validate a method, as it is simpler and more economical, before working with a real dataset. In this paper, we apply fog synthesis on the public KITTI dataset to generate the Multifog KITTI dataset for both images and point clouds. In terms of processing tasks, we test our previous 3D object detector based on LiDAR and camera, named the Spare LiDAR Stereo Fusion Network (SLS-Fusion), to see how it is affected by foggy weather conditions. We propose to train using both the original dataset and the augmented dataset to improve performance in foggy weather conditions while keeping good performance under normal conditions. We conducted experiments on the KITTI and the proposed Multifog KITTI datasets which show that, before any improvement, performance is reduced by 42.67% in 3D object detection for Moderate objects in foggy weather conditions. By using a specific strategy of training, the results significantly improved by 26.72% and keep performing quite well on the original dataset with a drop only of 8.23%. In summary, fog often causes the failure of 3D detection on driving scenes. By additional training with the augmented dataset, we significantly improve the performance of the proposed 3D object detection algorithm for self-driving cars in foggy weather conditions.

In this repository, we release code and data for training and testing our SLS-Fusion network on stereo camera and point clouds (64 beams and 4 beams).

### Citation
If you find our work useful in your research, please consider citing:
  
    @Article{s21206711,
        AUTHOR = {Mai, Nguyen Anh Minh and Duthon, Pierre and Khoudour, Louahdi and Crouzil, Alain and Velastin, Sergio A.},
        TITLE = {3D Object Detection with SLS-Fusion Network in Foggy Weather Conditions},
        JOURNAL = {Sensors},
        VOLUME = {21},
        YEAR = {2021},
        NUMBER = {20},
        ARTICLE-NUMBER = {6711},
        URL = {https://www.mdpi.com/1424-8220/21/20/6711},
        PubMedID = {34695925},
        ISSN = {1424-8220},
        ABSTRACT = {},
        DOI = {10.3390/s21206711}
    }
   
### Download our Multifog KITTI dataset

The training and testing part of our Multifog KITTI datasets (SENSORS 2021) are organized as follows:
- Training (7481 frames): [[image_2]](https://drive.google.com/file/d/1oPuAX1-dRisN4eBcTcA-XUvdLoaO7HfX/view?usp=sharing) (4,3 GB), [image_3](https://drive.google.com/file/d/1MXJXzTz5X0HnPtrxsEsSxI8EUx13voJc/view?usp=sharing) (4,1 GB), [[velodyne_64beams]](https://drive.google.com/file/d/1-0siAOrslNqqKdOqRstJgCm9rE7sPpxF/view?usp=sharing) (10,7 GB), [[velodyne_4beams]](), [[visibility_level]](https://drive.google.com/file/d/1ggn3RWfp488b3MrRJv13MV6W-CHpYNeX/view?usp=sharing).
- Testing:  [[image_2]](), [[image_3]](), [[velodyne_64beams]](), [[velodyne_4beams]](), [[visibility_level]]().