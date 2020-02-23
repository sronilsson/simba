# Using DeepPoseKit in SimBa

DeepPoseKit projects can be created and managed in SimBa, and DeepPosekit tracking data can be imported into SimBA to [generate machine learning behavioral classifiers](https://github.com/sgoldenlab/simba/blob/master/docs/Scenario1.md).

[DeepPosekit](https://github.com/jgraving/DeepPoseKit) is an *extremely* powerful and flexible pose-estimation tracking tool that has a wide-range of features that enables user to create robust tracking models. [DeepLabCut](https://github.com/AlexEMG/DeepLabCut) and [LEAP](https://github.com/talmo/leap) based models can also be generated within the DeepPoseKit pipeline which can allow model comparisons - please read the excellent [DeepPoseKit paper in ELife](https://elifesciences.org/articles/47994). The base DeepPoseKit package does not come with a GUI or standardized project folder structures which users of other animal pose-estimation tools might have gotten used to. However, such folder structures are created when DeepPoseKit projects are managed through SimBA.  

**IMPORTANT I**: Although DeepPoseKit currently does not come with a GUI, it's commandline tools offer much extended functionality over the SimBA wrapper of DeepPoseKit. We strongly *urge* users to use DeepPoseKit though the available [notebooks](https://github.com/jgraving/DeepPoseKit#using-deepposekit-is-a-4-step-process) where possible to get the full tour-de-force DeepPoseKit experience. 

**IMPORTANT II**: For extensive details on the DeepPoseKit workflow, please see the documentation on the [DeepPoseKit Github page](https://github.com/jgraving/DeepPoseKit).

>*Note*: Depending on the specific version of the different pose estimation tools the dependencies may diverge. For example, note that DeepPoseKit require tensorflow >=1.13 and CUDA 10, while some versions of DeepLabCut run on earlier CUDA/tensorflow releases. 

# Part 1: Creating a DeepPoseKit project in SimBA

To start using DeepPoseKit in SimBA, begin by creating a SimBA project as decribed in-depth in [Part 1 - Create a new project](https://github.com/sgoldenlab/simba/blob/master/docs/Scenario1.md#part-1-create-a-new-project-1) of the Scenario 1 Tutorial. 

Next, close the Project Configuration window. In the main SimBA console window, click on Tracking. In the dropdown, chose DeepPoseKit, and click on Create DeepPoseKit project.

![](https://github.com/sgoldenlab/simba/blob/master/images/DPK1.png "dir_info")

Once clicked, the following window should pop open: 

![](https://github.com/sgoldenlab/simba/blob/master/images/DPK2.png "dir_info")

Next to the SimBA project.in file, click on browse and select your SimBA project_config.ini file. Next to project Name, give your DeepPoseKit project a name (*Note:* avoid using spaces in the name. Instead, use underscore if needed). Click on Generate project to create your DeepPoseKit project folder structure. 

You DeepPoseKit project will be generated within the chosen SimBA project. If you navigate to you SimBA project, and look within the `project_folder\logs\measures\dpk` folder, you should see a folder named after your chosen `Project Name`. The inside if this folder will contain several subfolders reminiscent of the sub-folders created by other packages:
![](https://github.com/sgoldenlab/simba/blob/master/images/DPK_2.png "dir_info")

Go ahead and close the `Create DeepPoseKit project` window.  

# Part 2: Loading a DeepPoseKit project in SimBA

In the main SimBA console window, click on Tracking. In the dropdown, chose DeepPoseKit, and click on Load DeepPoseKit project and the following window pops up:

![](https://github.com/sgoldenlab/simba/blob/master/images/DPK_3.png "DPK_3")

When DeepPoseKit projects are created in SimBA, they each come with their own *.ini* file that stores your project settings chosen in the SimBA GUI. This is **not** the same *project_config.ini* that stores your main SimBA project settings, but a separate *.ini* file, exclusive to your DeepPoseKit project. Go ahead and click on `browse File` and navigate to your DeepPoseKit *.ini* file located in your DeepPosekitProject (in the `project_folder\logs\measures\dpk` directory). Once done, click on `Load Project`.

# Part 3: Working with DeepPoseKit projects in SimBA

## Step 2: Using the DeepPoseKit Annotator in SimBA 

In the DeepPoseKit window, click on the `Annotator` tab and you should see the following window:

![](https://github.com/sgoldenlab/simba/blob/master/images/DPK_4.png "DPK_4")

Click on `Browse File` and select your annotation *.h5* file located in the `annotation_sets` directory. Click on `Run` and the following windows should pop open, with instructions displayed on the right: 

![](https://github.com/sgoldenlab/simba/blob/master/images/DPK_annotator.PNG "DPK_4")

After the annotations are complete, press `Esc` to save your annotations. 

## Step 3: Training DeepPoseKit models in SimBA

Click on the `Train model` tab and ou should see the following window.

![](https://github.com/sgoldenlab/simba/blob/master/images/DPK_5.png "DPK_5")

For documentation on the different parameters and network architectures available, see Jake Garvings' [DeepPosekit](https://github.com/jgraving/DeepPoseKit) documentation. In SimBA, most of the entry boxes and user-defined settings defaults to the DeepPoseKit suggested defults. To chooose the neural network archictecture, click on the `NN_architecture` drop-down menu and you should see the networks available in DeepPoseKit:

![](https://github.com/sgoldenlab/simba/blob/master/images/DPK_6.png "DPK_6")

To access architecture-specific settings, click on the `Model Settings` button. Depending on the chosen archiceture, you should see one of the three possible menus:

<img src="https://github.com/sgoldenlab/simba/blob/master/images/DPK_7.png" width="200"/> <img src="https://github.com/sgoldenlab/simba/blob/master/images/DPK_8.png" width="200"/> <img src="https://github.com/sgoldenlab/simba/blob/master/images/DPK_9.png" width="200"/>

Again, see Jake Garvings' [DeepPosekit](https://github.com/jgraving/DeepPoseKit) documentation for the model-specific setting in the [DeepLabCut](http://jakegraving.com/DeepPoseKit/html/deepposekit/models/DeepLabCut.html#references), [StackedDenseNet](http://jakegraving.com/DeepPoseKit/html/deepposekit/models/StackedDenseNet.html#references), [StackedHourglass](http://jakegraving.com/DeepPoseKit/html/deepposekit/models/StackedHourglass.html#references), and [LEAP](http://jakegraving.com/DeepPoseKit/html/deepposekit/models/LEAP.html#references). 

## Step 4: Track body-part coordinates using DeepPoseKit in SimBA


## Step 5: Visualize tracking using DeepPoseKit in SimBA



























