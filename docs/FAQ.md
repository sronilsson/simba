## Friendly Asked Questions (FAQ)

- **I get 'TypeError: cannot convert the series to <class 'int'>' or 'TypeError: cannot convert the series to <class 'float'>' when trying to extract features, generate movies/frames, or when extracting outliers**

>This error comes up when SimBA can't find the resolution and/or pixels per millimeter of your video. This data is stored in the `project_folder/logs/video_info.csv` file. If open this CSV file, make sure that the left-most column named `Video` contains the names of your video files, do not contain any duplicate rows (where video names appear in more than one row), and that the resolution columns and pixels/mm column contains values. 

- **I get a `QHull` (e..g., QH6154 or 6013) error when extracting the features** 

>This error typically happens when a video tracked with DLC/DPK does not contain an animal (or one animal is missing from the video when you are tracking two animals). Because no animal is present in the video, DeepLabCut places all body-parts at the same co-ordinate with a low probability. SimBA tries to use these co-ordinates to calculate metrics from teh hull of the animal, but bacause the coordinates are in 1D rather than 2D, it produces the`QHull` error. To fix it, use the video pre-processing tools in SimBA to trim the videos and discard the portions where no animals are present:

[Tutorial: Batch pre-process videos in SimBA](https://github.com/sgoldenlab/simba/blob/master/docs/tutorial_process_videos.md)

[Tutorial: Video pre-processing tools in SimBA](https://github.com/sgoldenlab/simba/blob/master/docs/Tutorial_tools.md)

- **The frames folder is empty after clicking to extract frames, or my videos have not been generated appropriately**

>Make sure that: 

1. You have installed FFmpeg: [INSTALLATION INSTRUCTIONS](https://m.wikihow.com/Install-FFmpeg-on-Windows)

2. You are running Python 3.6.0 (or python 3.6.10 in conda). 

- **SimBA won't launch - there's an error, some complaint about Shapely**

Check out these issue threads for potential fixes:

https://github.com/sgoldenlab/simba/issues/12

https://github.com/sgoldenlab/simba/issues/11#issuecomment-596805732

> ** SimBA won't start, and there is GPU related errors such as "ImportError: Could not find 'cudart64_100.dll'


