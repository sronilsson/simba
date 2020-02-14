The SimBA region of intrest (ROI) interface allows users to define and draw regions of interest (ROIs) on videos. The ROI data can be used to visualize and calculate basic descriptive statistics based on animals movements and locations, and/or used to build potentially valuable additional features for random forest predictive classifiers.


# Before analyzing ROIs in SimBA
Before defining and analyzing ROI data in SimBA, the data needs to be processed through up to and including [Part 2 - Step 4](https://github.com/sgoldenlab/simba/blob/simba_JJ_branch/docs/Scenario1.md#step-4-outlier-correction) outlined in [Scenario1](https://github.com/sgoldenlab/simba/blob/simba_JJ_branch/docs/Scenario1.md). Specifically, begin by (i) [Importing your videos to the project](https://github.com/sgoldenlab/simba/blob/simba_JJ_branch/docs/Scenario1.md#step-2-import-videos-into-project-folder), (ii) [Importing the tracking data to your project](https://github.com/sgoldenlab/simba/blob/simba_JJ_branch/docs/Scenario1.md#step-3-import-dlc-tracking-data), (iii) [Set the video parameters](https://github.com/sgoldenlab/simba/blob/simba_JJ_branch/docs/Scenario1.md#step-3-set-video-parameters), and (iv) [Correct outliers](https://github.com/sgoldenlab/simba/blob/simba_JJ_branch/docs/Scenario1.md#step-4-outlier-correction). 

# Step 1. Defining ROIs in SimBA

1. In the main SimBA console window, begin by loading you project by clicking on `File` and `Load project`. In the **[Load Project]** tab, click on `Browse File` and select the `project_config.ini` file belonging to your project. 

2. Navigate to the **ROI** tab, which should look like this:

![](/images/roi_main.PNG)

3. Begin at the left hand side of the **ROI** tab, which lets you define **the number of rectangles, circles, and polygons** you which to draw on the videos in the project. All videos in the project needs to contain the same number of shapes. In the three entry boxes associated with each shape, enter the number of shapes you wish to draw. If you do *not* want to draw a specific shape, leave the entry box blank or enter the number 0. 

4. Once this infomation is entered, click on `Show Shape Definitions Table` and the following table will pop up.

![](/images/roidef1.PNG)

In this table, enter a name for each of your shapes in the Rectangle Name, Circle Name, and Polygon Name entry boxes. Once the names have been entered, click on the `Set Shape Definitions` button which is located at the bottom of the Shape definitions table. 

5. After clicking on the `Set Shape Definitions` button, the following table will pop up.


Each video in the project has three buttons associated with it: **Draw, Reset, and apply to all**. The functions of each button will be outlined below. In brief, the *Draw* button allows you to start to draw your defined shapes on the specific video. The *Reset* button delets any drawing made on the specific video and allows you to restart the drawing from scratch on the specific video by next clicking on the *Draw* button. The *Apply to all* buttons takes the drawing made on the specific video and replicates it on all other videos in the project. 

>*Note*: If a drawing has been made on a specific video, or applied to all videos by clicking on the *Apply to all* button, then the drawn shapes for a specific video can be moved by clicking on the *Draw* button.

6. To begin draw your shapes, click on the Draw button for the first Video in the table. Once clicked, a window will first pop up that contains instructions for how to draw your shapes. The instructions for drawing rectangles, circles, and polygons are slightly different. Any defined rectangles will be processed first. The instructions for drawing rectangles will look like this:

![](/images/ROI_rectangle.JPG)



















Select Shape --> Define Shape --> Draw Shape --> Analyze ROI --> Visualize ROI

## Step 1: Select Shape for ROI

1. Load your `project_config.ini` under the **[Load Project]** tab.

2. Navigate to the **[ROI]** tab --> `Define ROI`, enter the number of shapes for the region of interest in your video.





4. Enter the name for the shapes. You can set a fixed width and height for your rectangle in the given entry boxes. If it was left to be 0, rectangle can be drawn by free hand. This is the same case for circle.

![](/images/roidef.PNG)

5. Once all the information is filled, click on `Set Shape Definitions`, and the **ROI Table** will pop up.

## Step 2: Draw Shape

1. The **ROI Table** will be populated based on the number of videos in your project folder.

2. In this case, I have one video in my project folder and the **ROI Table** will look like this.

![](/images/roitable.PNG)

3. Click on `Draw` to start drawing ROI. Read the instructions carefully and follow through the steps.

![](/images/roigif.gif)

4. If you want to apply the ROI to all the video in your project, click `Apply to all` from the same row of the video that you just clicked `Draw`.

5. If you want to redraw the ROI, click `Reset`, and that will reset the ROI you drew. Click on `Draw` again to redraw your ROI.

## Step 3: Load ROI (Optional)

1. Load your `project_config.ini` under the **[Load Project]** tab.

2. Under **[ROI]** tab --> **Load ROI**, click on `Load defined ROI table`.

## Step 4: Analyze ROI

1. Once the ROI has been defined in every video, click on `Analyze ROI data`.



## Step 5: Visualize ROI



