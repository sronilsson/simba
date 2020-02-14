The SimBA region of intrest (ROI) interface allows users to define and draw regions of interest (ROIs) on videos. The ROI data can be used to visualize and calculate basic descriptive statistics based on animals movements and locations, and/or used to build potentially valuable additional features for random forest predictive classifiers.


# Before analyzing ROIs in SimBA
Before defining and analyzing ROI data in SimBA, the data needs to be processed through up to and including [Part 2 - Step 4](https://github.com/sgoldenlab/simba/blob/simba_JJ_branch/docs/Scenario1.md#step-4-outlier-correction) outlined in [Scenario1](https://github.com/sgoldenlab/simba/blob/simba_JJ_branch/docs/Scenario1.md). Specifically, begin by (i) [Importing your videos to the project](https://github.com/sgoldenlab/simba/blob/simba_JJ_branch/docs/Scenario1.md#step-2-import-videos-into-project-folder), (ii) [Importing the tracking data to your project](https://github.com/sgoldenlab/simba/blob/simba_JJ_branch/docs/Scenario1.md#step-3-import-dlc-tracking-data), (iii) [Set the video parameters](https://github.com/sgoldenlab/simba/blob/simba_JJ_branch/docs/Scenario1.md#step-3-set-video-parameters), and (iv) [Correct outliers](https://github.com/sgoldenlab/simba/blob/simba_JJ_branch/docs/Scenario1.md#step-4-outlier-correction). 

# Part 1. Defining ROIs in SimBA

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

6. To begin draw your shapes, click on the Draw button for the first Video in the table. Once clicked, a window will first pop up that contains instructions for how to draw your shapes. The instructions for drawing rectangles, circles, and polygons are slightly different. Any defined rectangles will be processed first. The instructions for drawing rectangles will look like this (left), and drawing rectangles should look kind of like this (right):

<img src="https://github.com/sgoldenlab/simba/blob/master/images/ROI_rectangle.JPG" width="425"/> <img src="https://github.com/sgoldenlab/simba/blob/master/images/Rectangle_draw.gif" width="425"/>

In this example, to begin to draw the rectangle named "TopLeft" on Video1, press on `Esc`. When `Esc` is pressed, the first frame of Video1 is displayed. Click and hold the left mouse button at the top left corner of rectangle "TopLeft" and drag the mouse to the bottom right corner of the rectangle

If you're unhappy with your rectangle, start to draw the rectangle again by holding the left mouse button at the top left corner of your new revised recangle. When you are happy with your rectangle, press `Esc` twice to save your rectangle and move to your next shape. Once all the rectangles have been drawn, any defined circles will be processed. The instructions for drawing circles will look like this:

<img src="https://github.com/sgoldenlab/simba/blob/master/images/ROI_circles.JPG" width="425"/> <img src="https://github.com/sgoldenlab/simba/blob/master/images/Circle_draw.gif" width="425"/>

In this example, to begin to draw the circle named "Cage" on Video1, press on `Esc`. When `Esc` is pressed, the first frame of Video1 is displayed. If you have previously drawn any rectangles, then these rectangles will also be displayed on the frame. Begin by double left clicking on the image where you would like the center of the circle to be. Next double left click on the image where you would like the outer bound of the circle to be. If you are unhappy with the center of the circle, double left mouse click on the center of the circle, and double left click again at the new circle center location. If you are unhappy with the outer bounds or the diameter of the circle, double left mouse click on outer bounds of the circle, and double left click again at the new circle outer bounds location. When you are happy with your circle, press `Esc` to save your circle and move to your next shape. Once all the circles have been drawn, any defined polygons will be processed. The instructions for drawing polygons will look like this:

<img src="https://github.com/sgoldenlab/simba/blob/master/images/ROI_polygons.JPG" width="425"/> <img src="https://github.com/sgoldenlab/simba/blob/master/images/Polygon_draw.gif" width="425"/>

In this example, to begin to draw the polygon named "Polygon1" on Video1, press on `Esc`. When `Esc` is pressed, the first frame of Video1 is displayed. If you have previously drawn any rectangles or circles, then these shapes will also be displayed on the frame. Click on at least three different locations in the image that defines the bounds of "Polygon1". SimBA does currently not allow re-definitions of the bounds locations of the polygon once they have been specified. If you are unhappy with your drawn polygon, you can however move the entire polygon in a later step (see below). When you have finished your polygon, press `Esc` to save your polygon and move to your next shape (or to finish if all the shapes have been drawn).


6. If you have finished the drawing for Video1, and you are not entirely happy with the drawings, you can either: (i) click on the `Reset` buttons next to Video1. This will delete the drawings you have made, and you can now again click on `Draw` button next to Video1 to restart Step 5. Alternatively, you can click on `Draw` again **without** first clicking on `Reset`. This will allow you to move the shapes for Video1 that you have defined.When you click on `Draw` again **without** first clicking on `Reset` after you have defined your shapes, the following instruction window will pop open:

<img src="https://github.com/sgoldenlab/simba/blob/master/images/ROI_move.JPG" width="425"/> <img src="https://github.com/sgoldenlab/simba/blob/master/images/Move_shapes.gif" width="425"/>

To start moving the shapes you have drawm, first click on the centroid circle belonging to the shape that you wish to move. This will cause the shape to disapear. Next, double left click on the new centroid location of the shape you are moving. This will display the shape in its new location. When happy, press on on `Esc` to save the new shape locations.  

7. Once all the shapes have been drawn on a single video there are two possible routes to getting them drawn on all of the videos in the project. One, and probably more time-consuming alternative, is to click on the `Draw` buttons associated with each video, and replicate **Step 5** for all of the videos in you project. Another, faster and more standardized alternative, is to replicate shapes drawn on Video1 in all of the videos of the project, and then move/nudge them in each of the videos. To replicate ROI shapes drawn for Video1 to all of the videos in the project, click on the `Apply to all` button next to Video1. Once done, click on `Draw` for Video2. This will first display the Instruction window for how to move shapes - press `Esc` to proceed. This displays the first frame for Video2. Move the shapes so that they are in the correct locations (as described in Step 6 above), and press `Esc` to save the locations of the shapes.

Repeat this step for all of the videos in the project. Once complete, close the **ROI Table** window, and navigate back to the **ROI** tab in the **Load project** window.

# Part 2. Analyzing ROI data.

This process will produce two CSV files: one file that contains the number entries into each ROI shape for each video, and a second file that contains the time spent in each zone for each video. 

1. All ROIs are now defined and the data can now be analyzed. Note: if you at any point want to look at, or modify, the defined ROI shapes for each of the videos, click on the `Load defined ROI table` button in the **ROI** tab under the `Load project` menu. If you'd like to delete all the shapes you have drawn for all of the videos and start afresh with new shapes, go back to Part 1, Step 3.

2. To analyze your ROI data, click on `Analyze ROI data` in the Analyze ROI submenu. The following menu will pop open:

![](https://github.com/sgoldenlab/simba/blob/master/images/ROI_analyze1.jpg)

Here, select the number of animals you wish to analyze the data for. First select if wish to analyze the entry and time ROI data for a single animal or two animals, and then click confirm. A second submenu will appear below named `Choose bodyparts`. This menu will contain as many dropdown menus as the number of animals selected in the  `Select number of animals` menu. Each of these drop-down menus will contain the body-parts used to track the animals. Select the body-parts you wish to use to calculate the ROI entry and time data, and click run. 

Once complete, a statement will be printed in the main SimBA terminal window noting that the process is complete. The data can be found in the `Project_folder/logs` directory. 


# Part 3. Generating features for ROI data. 

With the ROI information, we can generate several further features that might be useful for predicting behaviors, or be useful within other third-party applications. This includes features like:

* In each frame, calculate if the animal is located within or outside the ROIs
* In each frame in the video, calculate the metric distance 



