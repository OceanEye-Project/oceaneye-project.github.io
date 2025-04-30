OceanEye uses the [ONNX](https://onnx.ai/) (Open Neural Network Exchange) format, which is a popular cross-platform format for sharing AI models.

It is reccomended to use a [CUDA-capable GPU](https://developer.nvidia.com/cuda-gpus). CUDA can be downloaded [here](https://developer.nvidia.com/cuda-downloads). While training on a CPU is supported, it may result in significantly longer training times.

Model training requires additional dependencies, which are automatically installed during the initial training process with OceanEye.

It is recommended to have at least 200 annotations per class before initiating training. For optimal results, having over 1,000 annotations per class is strongly encouraged.

## Model Training Settings

| Setting                  | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| Model Save Location      | Filepath to the outputted model                                             |


### Advanced Settings

| Setting                  | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| Base Model               | Specifies the filename of a [supported Ultralytics model](https://docs.ultralytics.com/models/#featured-models) to be used as the starting point for training. |
| Training Time            | Defines the maximum allowable duration for training. Set to 0 for unlimited training time. |
| Max Epochs               | Indicates the total number of epochs for training, where each epoch represents a complete iteration over the dataset. |
| Patience                 | Determines the number of consecutive epochs without improvement in validation metrics before terminating the training process early. |


Model training requires Python. An isolated Python environment is automatically created within the `.oceaneye` directory located in your home folder. Approximately 5 GB of additional dependencies will be installed during this process. Depending on your system's performance, training may take several hours or even multiple days. It is recommended to allow the process to run uninterrupted.