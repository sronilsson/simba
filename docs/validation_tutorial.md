# Validate model on single video

1. Click on `File` --> `Load project`, and the following window will pop up.

![](/images/loadprojectini.PNG)

2. Click `Browse File` and select the *project_config.ini* file and click `Load Project`.

3. Under **[Run machine model]** tab --> **validate Model on Single Video**, select your features file (.csv). It should be located in `project_folder/csv/features_extracted`.

![](/images/validatemodel_graph.PNG)

4. Select a model file (.sav).

5. Click on `Run Model`.

6. Once, it is completed, it should print *"Predictions generated."*, now you can click on `Generate plot`. A graph window and a frame window will pop up.

- `Graph window`: model prediction probability versus frame numbers will be plot. The graph is interactive, click on the graph and the frame window will display the selected frames.

- `Frame window`: Frames of the chosen video with controls.

![](/images/validategraph1.PNG)

7. Click on the points on the graph and picture displayed on the other window will jump to the corresponding frame. There will be a red line to show the points that you have clicked.

![](/images/validategraph2.PNG)

8. Once it jumps to the desired frame, you can navigate through the frames to determine if the behavior is present. This step is to find the optimal threshold to validate your model.

![](/images/validategraph.gif)

9. Once the threshold is determined, enter the threshold into the `Discrimination threshold` entry box and the desire minimum behavior bouth length into the `Minimum behavior bout lenght(ms)` entrybox.

- `Discrimination threshold`:

- `Minimum behavior bout length (ms)`:

10. Click `Validate` to validate your model. **Note that this step will take a long time as it will generate a lot of frames.**
