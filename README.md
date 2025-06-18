# 🧠 Integrated Image Captioning and Segmentation Model

This repository contains an integrated deep learning model that performs **image captioning** and **semantic segmentation** simultaneously. The model shares a CNN backbone and uses separate decoders for each task.

---

## 📁 Project Structure

- **Library Imports**: Essential packages and modules.
- **Dataset Classes**:
  - `COCODataset`: Mock/Hugging Face variant.
  - `RealCOCODataset`: Loads real COCO dataset with `pycocotools`.
- **Model Architectures**:
  - `CNNEncoder`: ResNet-based CNN feature extractor.
  - `AttentionDecoder`: (Optional) decoder for captions.
  - `CaptioningModel`: Standalone captioning model.
  - `UNet`: Standalone segmentation model.
  - `IntegratedModel`: Shared backbone with dual-task decoders.
- **Training & Evaluation**:
  - `train_integrated_model`
  - `train_model_with_logging`
  - `evaluate_model`
  - `calculate_metrics`: BLEU (captioning), IoU (segmentation)
- **Utility Functions**:
  - `VocabularyBuilder`, `create_mock_coco_data`
  - `setup_training`, `example_training_setup`
  - `create_data_loaders`, `generate_sample_results`
  - `main`: Full training and eval pipeline.

---

## ⚙️ Setup

### 🔧 Environment Setup

Install Python dependencies:

```bash
pip install torch torchvision numpy matplotlib Pillow opencv-python nltk transformers datasets pycocotools
```
### 📌 License
This project is licensed under the MIT License.

### 🤝 Contributing
Contributions are welcome! Please open issues or pull requests to improve the model, training pipeline, or documentation.
