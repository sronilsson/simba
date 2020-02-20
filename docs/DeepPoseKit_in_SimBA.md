# Using DeepPoseKit in SimBa

DeepPosekit projects can be created and managed in SimBa. DeepPosekit tracking data can be imported into SimBA and used to generate machine learning behavioral classifiers,

DeepPosekit is an extremely powerful pose-estimation tracking tool, 
 in a similar manner to DeepLabCut tracking data
The base package of DeepPoseKit is extremely powerful and does not come with a GUI and standardized folder structures 
Note: Although DeepPoseKit currently does not come with a GUI, it's commandline tools offer much extended functionality over the SimBA wrapper of DeepPoseKit. We urge users to implement the deeposekit by the command line if they have the technical skills to do so. 
Note 2: Depending on the specific version of the different pose estimation tools, the dependencies may diverge. For example, note that DPK require tensor flow 1.13 or above and CUDA 10, while some versions of DLC runs on tensorflow Less than 1.12 and CUDA 9.
