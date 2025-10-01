## AI Academic Certificate  Authenticator
#📌 Overview

The AI Certificate Verifier is a tool designed to detect fraudulent or forged academic certificates using OCR (Optical Character Recognition), OpenCV image analysis, and machine learning models.

The system identifies signs of tampering such as:

-Font mismatches

-Inconsistent text alignment and spacing

-Editing hotspots (regions where modifications are likely)

-Signs of image manipulation from editing software

-Noise and artifact analysis

#🛠️ Features

-OCR Extraction using pytesseract

-Preprocessing with OpenCV (thresholding, denoising, contour analysis)

-Forgery Detection using handcrafted + AI-based techniques

-Noise & Artifact Analysis

-Modular Pipeline (easy to extend with new detection techniques)

#📂 Repository Structure
-src/ → Core modules (OCR, forgery detection, noise analysis, utils)
-models/ → Saved AI/ML models
-data/ → Sample documents for testing
-notebooks/ → Jupyter notebooks (prototyping & experiments)
-tests/ → Unit tests for pipeline validation
-requirements.txt → Dependencies

#🚀 Getting Started
1. Clone the repository
```
git clone https://github.com/your-username/ai-certificate-verifier.git
cd ai-certificate-verifier
```

#2. Install dependencies
```
pip install -r requirements.txt
```
#3. Run the pipeline
```
python src/main.py --input data/sample_fake.pdf
```

#📦 Dependencies

-Python 3.8+

-OpenCV

-pytesseract

-numpy, pandas

-scikit-learn / tensorflow / pytorch (if ML models are used)

-matplotlib / seaborn (for visualization)

#🧪 Example Usage
```
from src.main import run_verification

result = run_verification("data/sample_fake.pdf")
print(result)
# Output: {"status": "fraudulent", "reasons": ["Font mismatch", "Editing hotspots detected"]}
```
#📊 Results

-Sample real certificate → ✅ Verified

-Sample forged certificate → ❌ Fraud detected (font mismatch + editing artifacts)

#📌 Future Work

-Deep learning–based forgery detection

-Blockchain integration for certificate verification

-Larger dataset for improved model accuracy
