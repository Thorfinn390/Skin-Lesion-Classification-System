# Skin Cancer Classifier & Professional Reporting System

An AI-driven diagnostic assistant utilizing a fine-tuned **ResNet-18** architecture to classify skin lesions from the **HAM10000 dataset**. This tool not only predicts the lesion type butgenerates a professional-grade medical report with biopsy recommendations.

 

## Key Features
- **Multi-Class Classification:** Detects 7 types of skin lesions (Melanoma, BCC, etc.).
- **Clinical Logic Engine:** Maps AI confidence levels to biopsy recommendations and urgency levels.
- **Automated Documentation:** Generates downloadable `.docx` professional reports for clinical correlation.
- **Class Imbalance Handling:** Uses weighted Cross-Entropy loss to ensure rare malignant cases (like Melanoma) are prioritized.

## Dataset: HAM10000
The "Human Against Machine" dataset contains 10,015 dermatoscopic images. 
- **Malignant:** Melanoma, Basal Cell Carcinoma.
- **Pre-Malignant:** Actinic Keratoses.
- **Benign:** Nevi, Benign Keratosis, Dermatofibroma, Vascular Lesions.

## Technical Implementation
1. **Architecture:** ResNet-18 (Transfer Learning).
2. **Optimizer:** AdamW with `ReduceLROnPlateau` scheduler.
3. **Loss Function:** Weighted Cross-Entropy to handle the heavy distribution of 'Nevi' (moles).
4. **Augmentation:** Random flips, rotations, and color jittering to simulate various lighting/angles.



## Installation & Usage
1. Clone the repo: `git clone https://github.com/YOUR_USERNAME/Skin-Cancer-Classifier.git`
2. Install dependencies: `pip install -r requirements.txt`
3. Run the notebook or script. Ensure the HAM10000 `.zip` files are located in your data directory.

## Medical Disclaimer
This software is for **research purposes only**. It is not a diagnostic tool for clinical use. All results must be verified by a board-certified dermatologist.