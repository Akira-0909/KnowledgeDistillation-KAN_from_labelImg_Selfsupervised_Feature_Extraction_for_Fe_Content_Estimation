# DINOv2-KANLI: Weakly-Supervised Feature Extraction for Ferrous Content Estimation in Scrap Images

Accurate quantification of ferrous content in scrap materials is essential for optimizing recycling processes and advancing environmental sustainability. Conventional methods often depend on labor-intensive, destructive testing procedures, which limit scalability and efficiency. This project presents DINOv2-KANLI, a weakly-supervised feature extraction framework designed to estimate ferrous content from scrap images in a non-destructive and efficient manner. Leveraging the self-supervised learning capabilities of DINOv2 and the function approximation strengths of Kolmogorov-Arnold Networks (KAN), combined with sparse annotations from labelImg and Python modules, this approach captures intricate visual patterns indicative of ferrous content without requiring extensive labeled datasets. The framework integrates knowledge distillation (KD) and labelImg, allowing DINOv2-KANLI to learn nuanced representations of ferrous textures and spatial characteristics in a weakly-supervised setting. By incorporating sparse annotations, the framework enhances feature extraction precision and accuracy in ferrous content estimation. Experimental results indicate that DINOv2-KANLI consistently outperforms existing methods, providing a scalable, accurate, and non-destructive solution that aligns with industry needs for sustainable scrap recycling.

## Features

- **Self-Supervised Learning**: Utilizes DINOv2 for robust feature extraction without extensive labeled data.
- **Kolmogorov-Arnold Networks (KAN)**: Employs KAN for effective function approximation in high-dimensional image data.
- **Knowledge Distillation**: Integrates KD to transfer knowledge from teacher to student models, enhancing learning efficiency.
- **Sparse Annotations**: Incorporates minimal annotations via labelImg to improve feature extraction accuracy.
- **Non-Destructive Analysis**: Provides a scalable solution for ferrous content estimation without damaging materials.

## Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/yourusername/DINOv2-KANLI.git
   cd DINOv2-KANLI
   ```

2. **Set Up the Environment**:

   Ensure you have Python 3.8 or later installed. Create a virtual environment and activate it:

   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```

3. **Install Dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. **Prepare Your Data**:

   - Collect scrap material images for analysis.
   - Use [labelImg](https://github.com/tzutalin/labelImg) to annotate a subset of images with ferrous content information.

2. **Train the Model**:

   ```bash
   python train.py --data_path /path/to/your/data --annotations /path/to/annotations
   ```

   Adjust hyperparameters as needed in the `config.yaml` file.

3. **Evaluate the Model**:

   ```bash
   python evaluate.py --model_path /path/to/saved/model --test_data /path/to/test/data
   ```

   The evaluation script will provide metrics on the model's performance in estimating ferrous content.

## Contributing

I welcome contributions to enhance DINOv2-KANLI. 


*Keywords*: self-supervised, DINO, DINOv2, labelImg, Python, KAN, Knowledge Distillation, Kolmogorov-Arnold Networks, Ferrous Content Estimation, Feature Extraction, Ferrous Texture 
