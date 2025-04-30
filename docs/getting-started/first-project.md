# Creating Your First Project

A project serves as a container for managing a collection of images, annotations, and models. It provides a structured environment to streamline the process of detection, annotation, and model training.

```mermaid
graph TD
    A[Create a New Project] --> B[Add Media]
    B --> C[Run Detections]
    C --> D[Annotate Media]
    D --> E[Train Models]
    E --> B
    D --> F[Export Annotations]
```


## Configuring Your Project

Configuring a project involves defining the following settings. You will be prompted to do so on creation of new projects.

| Setting                              | Description                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------|
| **Load model**                       | Select what model will be used for detections.                              |
| **Specify detections**               | Select which objects the model should write detections for.                 |
| **Model confidence**                 | How certain the model should be in the object in order to write the detection. |
| **Select video slice interval**      | In the case of videos, how far apart should the frames be captured?          |
| **Automatically filter dead video**  | Select whether the video should save frames that do not include a written detection. |

!!! info
    These settings may be changed at any time after initial configuration by navigating to the "settings" tab while in a project.


!!! tip
    Remember to press "Apply" when you are done!

## Adding media

After configuration, you can begin to add media. Currently, we support the following formats:

- `.MP4`
- `.MOV`
- `.PNG`
- `.JPG`

!!! info
    Media will be screened on upload, before being loaded into the project. Detection may be re-run on a per-frame basis with a custom confidence via the **"detect"** button, in the event that experimenting with confidence is desired.
!!! warning
    Running **"detect"** on a single frame will overwrite existing detections.


## Annotating media

Annotations represent instances of a particular object within some image. These may be created by either users or, eventually by a model -- once the user has a trained model, that is. 

Since we may expect some degree of errors in model detections, users may wish to correct the result of a model's work. That is to say: they may wish to add, remove or edit annotations. This functionality is available within currently active projects, either by selecting the **+ New Annotation** option or using the shortcut: **N**. Annotation creation is by drag-and-drop, and the object category ("class") may be selected either by rotating through options via the **space bar**, or manually selecting the type of object in the top-left dropdown **Class** selection.

If you are unhappy with a particular annotation, you may delete it with the **delete** or **backspace** keys.


!!! warning
    Additional object types may not be added after project creation.

## Model Training

## 