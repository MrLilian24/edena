# 🌱 Edena

**Soil classification from images using deep learning**

A machine learning project for analyzing soil types from smartphone photos using transfer learning with [EfficientNet-B0](https://huggingface.co/google/efficientnet-b0).

---

## 🎯 Project Overview

Edena classifies soil images into 7 different soil types using a Convolutional Neural Network (CNN). This project is part of the larger **GeoGarden** system, which combines soil detection with plants recommendations for gardening applications.

### Key Features

- 🏞️ **7 soil types** classification (Arid, Black, Laterite, Mountain, Red, Yellow, Alluvial)
- 🧠 **Transfer learning** with EfficientNet-B0 pre-trained on ImageNet
- 📊 **82.58% validation accuracy** achieved

---

## 📊 Dataset

**Source**: [Comprehensive Soil Classification Datasets](https://www.kaggle.com/datasets/ai4a-lab/comprehensive-soil-classification-datasets) (Kaggle)

**Total images**: 1,188 (original dataset)

| Soil Type | Images | Percentage |
| --------- | ------ | ---------- |
| Arid      | 284    | 23.9%      |
| Black     | 255    | 21.5%      |
| Laterite  | 219    | 18.4%      |
| Mountain  | 201    | 16.9%      |
| Red       | 109    | 9.2%       |
| Yellow    | 69     | 5.8%       |
| Alluvial  | 51     | 4.3%       |

**Data split**:

- Training: 70% (~832 images)
- Validation: 15% (~178 images)
- Test: 15% (~178 images)

---

## 📈 Results

### Performance Metrics

| Metric                  | Score  |
| ----------------------- | ------ |
| **Validation Accuracy** | 82.58% |
| **Test Accuracy**       | 88.27% |

### Training Curves

![Training Curves](outputs/training_curves.png)

### Confusion Matrix

![Confusion Matrix](outputs/confusion_matrix.png)

---

## 🚀 Quick Start

### Prerequisites

- Python 3.11+
- Conda (recommended) or venv
- Kaggle account (for dataset download)

### Installation

```bash
# Clone the repository
git clone https://github.com/MrLilian24/edena.git
cd edena

# Create conda environment
conda create -n edena python=3.11 -y
conda activate edena

# Install dependencies
pip install -r requirements.txt
```

### Download Dataset

```bash
# Make sure you have Kaggle API credentials configured (~/.kaggle/kaggle.json)
kaggle datasets download -d ai4a-lab/comprehensive-soil-classification-datasets -p data/raw/
unzip data/raw/comprehensive-soil-classification-datasets.zip -d data/raw/soil-classification
```

### Run the Notebooks

```bash
# Start Jupyter
jupyter notebook

# Then run notebooks in order:
# 1. notebooks/01_data_exploration.ipynb
# 2. notebooks/02_data_preparation.ipynb
# 3. notebooks/03_model_training.ipynb
# 4. notebooks/04_model_evaluation.ipynb
```

---

## Deployment

### Planned Deployment

- **Platform**: HuggingFace Hub
- **API**: HuggingFace Inference API
- **Integration**: GeoGarden mobile application

### Future Work

- Fine-tune additional layers for better accuracy
- Collect more data for a larger dataset
- Experiment with other architectures (EfficientNet-B3, ResNet)
- Deploy as REST API endpoint

---

## 📄 License

This project uses a dual-license structure:

- **Code** (src/, notebooks/, scripts/): [Apache 2.0](LICENSE)
- **Model & Data** (trained weights, datasets): [CC BY-NC-SA 4.0](LICENSE_MODEL)

---

## Acknowledgments

Thanks to the following resources and their respective authors:

- Dataset: [AI4A Lab](https://www.kaggle.com/datasets/ai4a-lab/comprehensive-soil-classification-datasets) on Kaggle
- Pre-trained model: [EfficientNet](https://arxiv.org/abs/1905.11946) by Google Research
- Framework: [PyTorch](https://pytorch.org/)

---

## 👤 Author

**Rémi LAVERGNE** - [MrLilian24](https://github.com/MrLilian24)

---

## 📧 Contact

For questions or collaboration:

- GitHub Issues: [edena/issues](https://github.com/MrLilian24/edena/issues)
- Email (only for professional inquiries): contact@remi-lvg.com

---

> [!NOTE]
>
> **Status**: 🚧 Active Development
>
> **Current phase**: Model evaluation and HuggingFace deployment...
