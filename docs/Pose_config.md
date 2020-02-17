# User-defined pose-configurations in SimBA

We strongly recommend using SimBA with a [16-body-part, 2 animal, pose-configuration setting](https://github.com/sgoldenlab/simba/blob/master/docs/Tutorial_DLC.md#pose-estimation-body-part-labelling). SimBa also comes with several other other pre-generates pose-configuration settings which can be selected in the [Create Project](https://github.com/sgoldenlab/simba/blob/master/docs/Scenario1.md#step-1-generate-project-config) menu. To expand the application of SimBA, users can also define their own pose-configuration settings any number of body-parts. 



# Create a new user-defined pose-configuration

1. In the main SimBA console window, click on `File` and on `Create a new project`. The window that pops open is descibed in-depth the [Scenario 1 - Create Project](https://github.com/sgoldenlab/simba/blob/master/docs/Scenario1.md#step-1-generate-project-config) tutorial. When you are creating a new user-defined pose-configuration setting, **do not** specify a project path, project name, or any SML settings. Instead, skip these menus and click on the button in the `Animal Settings` menu next to the text `# config`. You should see the following default menu:

![alt-text-1](https://github.com/sgoldenlab/simba/blob/master/images/Create_pose_config_1.png "Pose config menu 1")

Click on `Create pose config` to begin to define a new user-defined pose configuration. 

2.  After clicking on `Create pose config`, the following menu pops open:

![alt-text-1](https://github.com/sgoldenlab/simba/blob/master/images/Pose_config_2.PNG "Pose config menu 2")

In the *first* entry box, give your pose-configuration a name. This could be, for example, BtWGaNP_pose: **avoid spaces in the pose config name**. In the *second* entry box, enter the number of animals you wish to track. This could be 1 or 2. In the *third* entry box, enter the number of body-parts the dataset contains. For example, if the dataset contains 8 tracked body-parts on two different animals, I enter the integer 16. 

Next, select an image that is representative of your tracking environment and contains a clear view of all the tracked bodyparts by clicking on `Browse File`. This image will be used to create a reference image of your pose configuration settings. After you have selected an image, click on `Confirm`.

3. After clicking confirm the following table should pop open:

![alt-text-1](https://github.com/sgoldenlab/simba/blob/master/images/Pose_config_image_3.PNG "Pose config menu 3")





