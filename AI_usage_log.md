# AI Usage Log

## 1. Dataset Structure Review

- **Tool used:** ChatGPT
- **Purpose:** Helped me understand the COCO annotation structure used in the original dataset.
- **What I kept or changed:** I used the explanation to inspect the annotation files and understand the relationship between images, categories, bounding boxes, and segmentation polygons.

## 2. Bounding Box Analysis

- **Tool used:** ChatGPT
- **Purpose:** Helped me compare the original bounding boxes with the segmentation polygon coordinates.
- **What I kept or changed:** I decided not to rely on the original bounding boxes and recalculated new boxes from the segmentation polygons.

## 3. COCO-to-YOLO Conversion

- **Tool used:** ChatGPT
- **Purpose:** Helped review the conversion of annotations from COCO format to YOLO format.
- **What I kept or changed:** I reviewed the suggested conversion logic, tested the output, and kept the normalized YOLO label format after verifying the coordinates.

## 4. Category Mapping

- **Tool used:** ChatGPT
- **Purpose:** Helped me discuss how the original 85 food categories could be grouped into 10 broader food component classes.
- **What I kept or changed:** I made the final class decisions and kept the following categories: bread, rice, potato, egg, cheese, tomato, carrot, cucumber, salad, and fruit.

## 5. Annotation Cleaning

- **Tool used:** ChatGPT
- **Purpose:** Helped identify possible problems such as invalid coordinates, duplicate label lines, multi-polygon annotations, and image-label inconsistencies.
- **What I kept or changed:** I added validation and cleaning steps, removed selected problematic annotations, and deleted 56 duplicate label lines from 24 files.

## 6. Model Training Support

- **Tool used:** ChatGPT
- **Purpose:** Helped review the YOLO11 training setup and troubleshoot code during the training process.
- **What I kept or changed:** I used a pretrained YOLO11n model and fine-tuned it through transfer learning for 50 epochs with an image size of 640 and a batch size of 16.

## 7. Results and Error Analysis

- **Tool used:** ChatGPT
- **Purpose:** Helped me interpret precision, recall, mAP50, and mAP50-95, and discuss prediction errors.
- **What I kept or changed:** I used the metric explanations in my evaluation, but I reviewed the predictions myself and made the final conclusions about successful detections and model limitations.

## 8. Final Documentation and Repository Organization

- **Tool used:** ChatGPT
- **Purpose:** Helped organize the final notebook, README, presentation, demo notebook, and GitHub repository structure.
- **What I kept or changed:** I selected the final structure, edited the wording, reviewed all files, and made the final decisions about what to include in the repository.

## Responsibility Statement

I was responsible for selecting the project direction, choosing the dataset, defining the classes, running and reviewing the code, validating the outputs, training and testing the model, and making the final decisions about preprocessing, evaluation, documentation, and conclusions.
