# Google-Summer-of-code
Layout Organization Recognition
# RenAIssance GSoC Test Task – Layout Recognition on Historical Spanish Documents

## 📌 Objective
To build a layout recognition model using a YOLOv8-based approach to detect where the main text is located in historical Spanish documents, filtering out embellishments.

##  Model
- YOLOv8 for layout detection.
- Post-processed detected text regions using `pytesseract` OCR (Spanish model).

## Dataset
- Images sourced from historical Spanish documents provided.
- Manually annotated via Roboflow in YOLO format.

## Project Structure
renai_layout_ocr_project/
├── layout_detection.ipynb            # Colab notebook with full pipeline
├── runs/
│   └── detect/
│       ├── layout_model2/            # Trained YOLOv8 model results
│       │   ├── images/               # Images with detected main text layout
│       │   └── labels/               # YOLO format labels (main text regions)
│       └── predict3/                 # YOLO predictions on test images
│           ├── images/               # Predicted layout visualizations
│           └── labels/               # Corresponding YOLO prediction labels
├── dataset/
│   ├── train/                        # Training images & labels (YOLO format)
│   └── test/                         # Test images
├── manual_crop.jpg                  # Sample manually cropped region for OCR
├── ocr_outputs/                     # Folder with OCR outputs from detected regions
├── requirements.txt                 # Python dependencies
└── README.md                        # Project summary and usage guide

## How to Run
1. Clone repo or upload to Google Colab.
2. Install dependencies:
   ```bash
   pip install ultralytics pytesseract
##Evaluation Metrics

    Intersection-over-Union (IoU) for layout bounding boxes.

    OCR text quality (visual + qualitative).

