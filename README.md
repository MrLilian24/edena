# 🌱 Edena

Soil analysis and plant recommendation using machine learning.

## Goal

Analyze soil conditions from images or structured data, and recommend suitable plants for a given environment.

## Project Status

> [!NOTE]
> 🚧 Phase 1: Data exploration and model prototyping

### Dataset

- **Source**: [Comprehensive Soil Classification Datasets](https://www.kaggle.com/datasets/ai4a-lab/comprehensive-soil-classification-datasets) (Kaggle)
- **Classes**: 7 soil types
- **Images**: 1,188 (original) + 5K (augmented)

| Soil Type | Images |
|-----------|--------|
| Arid | 284 |
| Black | 255 |
| Laterite | 219 |
| Mountain | 201 |
| Red | 109 |
| Yellow | 69 |
| Alluvial | 51 |

## Setup

```bash
git clone https://github.com/MrLilian24/edena.git
cd edena
conda create -n edena python=3.11 -y
conda activate edena
pip install -r requirements.txt
```

### Download dataset
```bash
kaggle datasets download -d ai4a-lab/comprehensive-soil-classification-datasets -p data/raw/
unzip data/raw/comprehensive-soil-classification-datasets.zip -d data/raw/soil-classification
```

## License

- **Code**: Apache 2.0 - see [LICENSE](LICENSE)
- **Model & Data**: CC BY-NC-SA 4.0 - see [LICENSE_MODEL](LICENSE_MODEL)