## Export Annotated Images
Annotated images can be exported either through the [Edit Media](./edit-media.md) dialog or directly from the main window.

To export images via the Edit Media dialog, select the desired images and click on the "Export Selected Images with Annotations" button.

To export an individual image, navigate to the image you wish to export and choose the `File > Export Image` option from the menu.


## Export Annotation Data
Annotations can be exported via the `File > Export Data` menu.

The exported data includes the following fields, with one entry per annotation:

| Field Name   | Description                                                                 |
|--------------|-----------------------------------------------------------------------------|
| Frame Name   | Specifies the file path of the image containing the annotation.            |
| Class        | Denotes the category of the annotation (e.g., "Sea Urchin", "Kelp").       |
| Confidence   | Represents the confidence score of the annotation, ranging from 0 to 1, (human-generated annotations have a confidence of 1). |
| X            | Indicates the X-coordinate of the annotation's top-left corner, measured in pixels. |
| Y            | Indicates the Y-coordinate of the annotation's top-left corner, measured in pixels. |
| Width        | Defines the width of the annotation's bounding box, measured in pixels.    |
| Height       | Defines the height of the annotation's bounding box, measured in pixels.   |

### Supported Export Formats:

#### CSV
CSV is the most popular export format. It is a simple, tabular format where each row represents an annotation, and each column corresponds to a field.

#### COCO
COCO, or Common Objects in Context, is a popular machine-learning dataset format. It organizes annotations into a structured JSON file, including categories, bounding boxes, and image metadata.

#### JSON
JSON is a flexible, lightweight data-interchange format. It exports annotations in a structured, hierarchical format, making it easy to integrate with custom pipelines or applications.

#### YAML
YAML is a human-readable data serialization format. It provides a clean and concise way to represent annotations, similar to JSON but with a more readable syntax.