# ShapeClassifierPyTorch

## Overview

This repository implements a complete pipeline for synthetic geometric shape classification using PyTorch, all contained within the `classifier.ipynb` notebook. You’ll find:

```
classifier/                 # project root
├── dataset/                # raw synthetic data output (gitignored)
├── shape_data/             # organized train/val/test folders (gitignored)
├── imgcls/                 # (optional) virtual environment folder (gitignored)
├── best_resnet18.pt        # saved model checkpoint
├── best_resnet18_RLRRheldout.pt # checkpoint from held-out test
├── classifier.ipynb        # Jupyter notebook orchestrating data gen, training & evaluation
├── requirements.txt        # Python dependencies
└── README.md               # this file
```

## Setup

1. **Create a virtual environment** (optional but recommended):

   ```bash
   cd classifier
   python3 -m venv imgcls
   source imgcls/bin/activate
   ```

2. **Install dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

## Running the Notebook

All steps—from dataset generation through model training, evaluation, and visualization—are contained in `classifier.ipynb`. To run it:

1. Launch Jupyter:

   ```bash
   jupyter notebook classifier.ipynb
   ```
2. Execute each cell in order. The notebook will:

   * Generate synthetic shape images and save metadata.
   * Compute dataset statistics (mean/std).
   * Split data into `shape_data/train`, `shape_data/val`, `shape_data/test`.
   * Define, train, and checkpoint a ResNet‑18 model.
   * Evaluate on held‑out RLRR examples and display accuracy/confusion matrix.

## Data & Notebooks

* **`classifier.ipynb`**: self‑contained pipeline; recommended workflow.
* **Data directories** (`dataset/`, `shape_data/`) are gitignored; run the notebook to recreate.
* **Checkpoints** (`.pt` files) saved automatically during training.



## Author

**Chaithra Lokasara Mahadevaswamy**  
[LinkedIn Profile](https://www.linkedin.com/in/chaithra-lokasara-mahadevaswamy-5bb076214/) 
🧠 **AI Enthusiast** | 📊 **Data Alchemist** | 🎓 **Graduate Researcher**  
🚀 **Innovation Seeker** | 🌟 **AI Tools Research Intern @ Unicorn Tutor AI**  
**_"Building Tomorrow with Intelligence Today"_**
