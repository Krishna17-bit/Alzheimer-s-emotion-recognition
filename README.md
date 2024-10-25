**Emotion Recognition in Alzheimer's Patients Using Machine Learning and Blockchain**

**Overview**

This project aims to recognize emotions in Alzheimer's patients using machine learning on a combination of health, demographic, and behavioral data. The model incorporates both Alzheimer's data and emotion-labeled data, and predictions are stored securely using a blockchain-based system. This approach provides privacy-preserving emotion recognition for patients, enhancing data security and traceability.

**Project Structure**

*   data/: Directory containing raw and processed datasets.
    
    *   raw/: Raw data files, including Alzheimer's and IEMOCAP datasets.
        
    *   processed/: Data ready for modeling.
        
*   notebooks/: Jupyter Notebooks for data exploration and analysis.
    
*   src/: Source code for data processing, model training, and utility functions.
    
    *   data\_processing.py: Script for data preprocessing and feature engineering.
        
    *   modeling.py: Script for model training and evaluation.
        
    *   utils.py: Utility functions used throughout the project.
        
*   models/: Directory with trained models.
    
    *   emotion\_recognition\_with\_alzheimers.pkl: Saved model file.
        
*   README.md: Project documentation.
    
*   requirements.txt: List of required packages.
    

**Data Sources**

1.  **Alzheimer's Dataset**: Custom dataset with health and demographic information for 2,149 patients, including behavioral and cognitive assessments.
    
2.  **IEMOCAP Dataset**: Dataset used for emotion recognition, containing audio-visual data with emotion labels.
    

**Project Setup**

1.  git clone https://github.com/Krishna17-bit/Alzheimer-s-emotion-recognition.git
2.  cd emotion-recognition-alzheimers
    
3.  bashCopy codepip install -r requirements.txt
    
4.  **Download Datasets**: Place the Alzheimer's and IEMOCAP datasets in the data/raw/ directory.
    
5.  bash python src/data\_processing.py
    
6.  bash python src/modeling.py
    

**Modeling Techniques**

This project employs multiple machine learning techniques for emotion recognition, including:

*   **Random Forest** and **XGBoost** for robust classification.
    
*   **Stacking Classifier** combining Random Forest, Gradient Boosting, and XGBoost, with a Logistic Regression meta-learner for improved performance.
    
*   **Voting Classifier** to combine predictions from multiple models for final predictions.
    

The final model achieved an accuracy of 94.42% on test data.

**Blockchain Integration**

Predictions are stored on a simulated blockchain for secure and traceable access:

1.  **Mock Blockchain Class**: Simulates blockchain transactions to store and retrieve emotion predictions.
    
2.  **Storage**: Each prediction is stored as an immutable record on the blockchain.
    
3.  **Retrieval**: Predictions are retrievable by unique IDs, ensuring privacy and data integrity without a real blockchain setup.
    

**Usage**

*   import joblibmodel = joblib.load('models/emotion\_recognition\_with\_alzheimers.pkl')predictions = model.predict(X\_new)
    

**Results**

The model achieved 94.42% accuracy, with high precision and recall for identifying emotions in Alzheimer’s patients.

**Visualizations and Insights**

1.  **MMSE vs. Dominant Emotion**: Scatter plots to visualize emotional distribution by cognitive scores.
    
2.  **Emotion Distribution by Alzheimer’s Diagnosis**: Charts to compare dominant emotions between Alzheimer’s and non-Alzheimer’s patients.
    
3.  **Correlation Matrix**: Analysis of relationships between demographic, clinical, and emotional features.
    

**License**

This project is licensed under the MIT License.

**Acknowledgments**

*   Alzheimer’s Disease Research Center for providing Alzheimer's data.
    
*   IEMOCAP dataset contributors for emotion recognition data.
