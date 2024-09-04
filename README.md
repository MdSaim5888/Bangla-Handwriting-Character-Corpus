# Bangla-Handwriting-Character-Corpus
Welcome to our project repository for developing and evaluating a multi-class corpus for Bangla handwriting recognition. We aim to advance handwriting recognition by creating a robust dataset, applying preprocessing and augmentation techniques, and evaluating recognition algorithms to achieve high accuracy and efficiency.

# Description
This diverse dataset compiles the user's perspectives for their research purposes. If the researchers want to modify their work on this platform (NLP, machine learning, deep learning, and artificial intelligence) using this dataset with the numerical vector, then it needs users' perspectives for their research purposes to identify the Unicode values, and if another section wants to use this dataset as the image that is already here. That's why we make access to this repository totally free for all further development. The productive way to use this dataset depends on the researchers or the users because of the diversity of this data, which can be used or modified however they need. We also notably understand that the availability that is demanded on the online platform is crucial. That's why this dataset contains all of the Bengali characters that exist or combine.

# Unique Feature
The dataset we have provided has a lot of unique features. The most efficient feature is Unicode values. Researchers can use this value instead of importing or modifying the image files but they first need to make understand the machine about the file that belongs to the value. This dataset contains every type of Benglai characters with their Unicode value as if combined characters or numerical characters. Another key feature is some characters that are used for sign language also have the Unicode values.

# Statistical Analysis
This expanded dataset now includes 25,900 additional samples, achieving a balanced representation across various demographics. This diversity is pivotal in developing more generalized and robust handwriting recognition models that perform well across different handwriting styles, thus enhancing the applicability of the research to a broader user base.

# Comparison with Existing Bangla Handwriting Datasets
In this section, we compare our developed dataset with prominent existing Bangla handwriting datasets to underscore the unique contributions and comprehensiveness of our work. The comparison focuses on sample size, demographic diversity, character coverage, and data accessibility. Our dataset significantly surpasses the size of other publicly available Bangla handwriting datasets. comparison of sample sizes:

- BanglaLekha-Isolated: 19,000 samples
- CMATERdb: 9,000 samples
- BN-HiLab: 12,000 samples
- Proposed Dataset: 25,900 samples

# Usage Guide
The dataset developed in this research, available on GitHub, provides a comprehensive corpus of Bangla handwriting samples intended for use in handwriting recognition tasks. It includes a diverse set of handwritten characters collected from various demographics to ensure a robust representation of Bangla script. As we mention about the free use of this repository so we conduct the license policy as nonexclusive but we want to ensure you that please use it for research purpose only, not for personal use or personal publication named yourself. Before using the dataset for model training, consider the following preprocessing steps to standardize input data:

- **Binarization**: Convert images to binary format using adaptive thresholding for consistent results.
- **Normalization**: Resize images to a fixed dimension (e.g., 32x32 pixels) and normalize pixel values to a range of 0-1 for compatibility with neural networks.
- **Augmentation**: Apply data augmentation techniques like rotation, scaling, and noise addition to increase data variability.

# Accessibility Section
The dataset is hosted on GitHub and can be accessed. Below is a sample Python script using TensorFlow and OpenCV to load and preprocess images from the dataset:

```
import cv2
import os
import numpy as np
dataset_path = 'path/to/data/train/ka/'

def load_images(path):
    images = []
    labels = []
    for filename in os.listdir(path):
        if filename.endswith('.png'):
            img = cv2.imread(os.path.join(path, filename), cv2.IMREAD_GRAYSCALE)
            img = cv2.resize(img, (32, 32))
            img = img / 255.0  # Normalize pixel values
            images.append(img)
            labels.append(filename.split('_')[0])  # Extract class label from filename
    return np.array(images), np.array(labels)
    
X, y = load_images(dataset_path)
print(f'Loaded {len(X)} images with corresponding labels.')
```

**Note**: We encourage contributions to further enhance the dataset. If you would like to contribute additional samples or report issues, please submit a pull request or open an issue on the GitHub repository.

# Suggested Remedies and Areas for Further Research
To address these challenges and enhance the accuracy of recognition models, the following remedies and areas for future research are recommended:

- Data Augmentation and Style Normalization
- Enhanced Preprocessing Techniques
- Attention Mechanisms in Recognition Models
- Character Decomposition and Segmentation Refinement
- Developing Adaptive Learning Models
- Error Analysis-Driven Model Enhancement

# Conclusion
We offer the research community to leverage this dataset to advance the field of Bangla handwriting recognition, and we welcome contributions that further enhance the corpus. By making the dataset freely accessible and providing thorough documentation, our goal is to foster a collaborative environment where insights can be shared, errors can be addressed, and continuous improvements can be made. Ultimately, this dataset not only aims to drive innovation in Bangla handwriting recognition but also serves as a foundation for future research exploring the rich and diverse characteristics of Bangla script. For any further assistance, feedback, or contributions, researchers are encouraged to contact the corresponding author, ensuring a dynamic and evolving resource that remains valuable to the community.

**THANK YOU** <br>
**Md. Abu Saim** <br>
**Email: mdabusaim.cse.ugv@gmail.com**
