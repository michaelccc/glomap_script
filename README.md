Script is courced from https://github.com/jonstephens85/glomap_windows/tree/main


## Automated Python Scripting
In this section I walk you through how to the `run_glomap.py` which automates the manual step for running GLOWMAP. Specifically, I added modifiers to output file structure and format to use with 3DGS and Nerfstudio.

### Accessing run_glowmap.py
You can either clone this database or manually download the file. **Note: only the python script is maintained on this repository. Clone the original project for the most up to date information**

### Usage
Use run_glowmap.py by passing this command:
`python run_glowmap.py --image_path path\to\images`

**note: if the image folder is named "images" or "input" you may have some issues with the script. This will be addressed in future updates**

This will run colmap feature_extractor, colmap sequential_matcher, and glowmap mapper sequentially. The data will output in a structure and format immediately usable for the original 3DGS project.

### Modifiers
<details>
<summary><span style="font-weight: bold;">Command Line Arguments for run_glowmap.py</span></summary>

  ####  --image_path
  Path to the source directory of images.
  #### --matcher_type {sequential_matcher,exhaustive_matcher}
  Type of matcher to used by COLMAP (default: sequential_matcher).
  #### --interval {int}
  Interval of images to use in source image directory. Increase the number to use less images. For example: 2 uses every other image, 6 uses every 6th image. (default: 1)
  ####  --model_type {3dgs,nerfstudio}
  Model type to run. '3dgs' includes undistortion, 'nerfstudio' skips undistortion.

</details>
<br>
<br>
