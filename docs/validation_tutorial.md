# Validate model on single video

1. Click on `File` --> `Load project`, and the following window will pop up.

2. Click `Browse File` and select the *project_config.ini* file and click `Load Project`.

3. Under **[Run machine model]** tab --> **validate Model on Single Video**, select your features file (.csv). It should be located in `project_folder/csv/features_extracted`.

4. Select a model file (.sav).

5. Click on `Run Model`.

6. Once, it is completed, it should print *Predictions generated.*, now you can click on `Generate plot`. A graph window and a frame window will pop up.

- `Graph window`: model prediction probability versus frame numbers will be plot. The graph is interactive, click on the graph and the frame window will display the selected frames.

- `Frame window`: Frames of the chosen video with controls.

