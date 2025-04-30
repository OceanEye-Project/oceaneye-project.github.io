To add media, click the **Add Media** button located in the main project view. A file dialog will appear, allowing you to select one or more images or videos for import.

Currently, we support the following formats:

- `.MP4`
- `.MOV`
- `.PNG`
- `.JPG`

### Behavior of Imported Media

#### Images
When importing images, OceanEye creates a reference link to the original files on your local filesystem.

!!! warning
    If the images are moved or renamed after being imported, OceanEye will no longer be able to locate them. 

#### Videos
When importing videos, OceanEye processes them by slicing the video into individual frames. These frames are extracted based on the slice interval specified in the application settings and are saved directly to the project folder.

### Automatic Detection and Filtering

- **Detection on Import:** If a detection model is loaded, OceanEye will automatically run detections on all imported images.
- **Automatic Filtering:** If the **Automatically Filter Dead Video** option is enabled in the settings, any frames or images without detections will be excluded from the project.