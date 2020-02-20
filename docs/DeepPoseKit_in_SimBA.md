# Using DeepPoseKit in SimBa

DeepPoseKit projects can be created and managed in SimBa, and DeepPosekit tracking data can be imported into SimBA to [generate machine learning behavioral classifiers](https://github.com/sgoldenlab/simba/blob/master/docs/Scenario1.md).

[DeepPosekit](https://github.com/jgraving/DeepPoseKit) is an *extremely* powerful and flexible pose-estimation tracking tool that has a wide-range of features that enables user to create robust tracking models. [DeepLabCut](https://github.com/AlexEMG/DeepLabCut) and [LEAP](https://github.com/talmo/leap) based models can also be generated within the DeepPoseKit pipeline which allow swift model comparisons - please read the excellent [DeepPoseKit paper in ELife](https://elifesciences.org/articles/47994). The base DeepPoseKit package does not come with a GUI and standardized folder structures which users of other animal pose-estimation tools might have gotten used to. However, such folder structures are created when DeepPoseKit projects are managed through SimBA.  

**IMPORTANT**: Although DeepPoseKit currently does not come with a GUI, it's commandline tools offer much extended functionality over the SimBA wrapper of DeepPoseKit. We *urge* users to use DeepPoseKit though the [command line and notebooks](https://github.com/jgraving/DeepPoseKit#using-deepposekit-is-a-4-step-process) if possible to get the full experience. 

>*Note*: Depending on the specific version of the different pose estimation tools the dependencies may diverge. For example, note that DeepPoseKit require tensorflow >=1.13 and CUDA 10, while versions of DeepLabCut run on earlier CUDA/tensorflow version. 

# Creating a DeepPoseKit project in SimBA

To begin using DeepPoseKit in SimBA, begin by creating a SimBA project by clicking on 




