# p3-ml
Group Project 3: Machine learning solution using ensemble learning techniques

## Team Members
- **Liu** - Models
- **Yogitha** - Visualization
- **Rachel** - Dataset

## AI Usage Documentation
AI Assistance Disclosure and Methodological Notes

### Tools Used
- **ChatGPT**: Model and display
    - Technical troubleshooting during environment setup, including Python virtual-environment configuration, dependency installations, and Jupyter kernel selection.
    - Clarification of API behaviors for libraries such as scikit-learn, pandas, and matplotlib.
    - Generation of boilerplate code templates, which were then modified, extended, and adapted manually to meet project requirements.
    - Structured refinement of explanations and documentation, ensuring conceptual accuracy and consistency throughout the notebook and README.
- **Gemini**: Dataset loading

### Non-Delegated Human Work
- All code related to model selection, feature preparation, training/testing logic, ensemble-model implementation (Random Forest + Gradient Boosting), and performance visualization was written, tested, and validated by the project contributors. AI suggestions were evaluated critically, integrated selectively, and revised to fit the project’s methodology.
- The following tasks were performed independently and were not outsourced to AI:
    - Selection and justification of ensemble learning algorithms.
    - Determination of evaluation metrics (accuracy and F1-score) and implementation details.
    - Interpretation of model results and construction of comparison plots.
    - Validation of dataset structure, data-cleaning decisions, and preprocessing steps.
    - Git version-control operations, including commits, merges, and repository organization.
- This ensures that the intellectual work, domain reasoning, and methodological decisions remain attributable to the human contributors.
The final notebook represents an integrated effort in which AI served as a supplementary tool, while all critical design, reasoning, and programming decisions were made by the project team.

### Specific AI Assistance

- **Prompt**: "How can I load a kaggle dataset as a pandas dataframe?"
- **AI Response**: Explained installation of kagglehub, downloading an example dataset, and loading into a pandas dataframe
- **Modification**: Used a selected dataset

### Dataset choice and justification

- **Files**: `ml-dataset.ipynb`, `hotel_bookings_updated_2024.csv`
    - The hotel bookings dataset was chosen because it comes from a reputable source (Kaggle.com), has a high Usability rating (Completeness, Credibility, Compatibility as calculated by Kaggle), and contains 33 columns of data (features). These features make it ideal for a machine learning approach.
    - `ml-dataset.ipynb` downloads the latest version of this dataset and readies it for use by the models.

### Methodology
- **Models used**: Random Forest, Gradient Boosting
    - the RandomForestClassifier and GradientBoostingClassifier from the sklearn library are trained and tested on this dataset.
    - Random Forest was chosen because its random feature splitting works well with the many features of the dataset.
    - Gradient Boosting was chosen because of its focus on reducing loss, resulting in better accuracy.

### Results analysis
- **Model Performance**: Predicting the is_cancelled feature
    - Input features (X): 32 other columns describing information such as hotel name, number of adults and children, and others.
    - Output feature (Y): Prediction of the is_cancelled feature, or whether a booking will be cancelled. (True or False).
    - The data is split into 20% test, 80% train.
    - The Random Forest has high Accuracy (97.72%), but lower F1 score, or precision and recall (66%).
    - The Gradient Boosting has high Accuracy and F1 score (100%).
    - The Random Forest underperforms in recall (50%), the number of true positives over the number of true and false positives. Both have high precision, or true positives over true positives + false negatives.

### Challenges Faced and Solutions
- **Choosing a dataset**: Sklearn and Kaggle datasets
    - Problem: Sklearn datasets were initially considered for this project, but lacked variety.
    - Solution: Kaggle was chosen because of its greater variety of datasets. AI assistance was used to learn how to import the Kaggle dataset.

- **Comparing metrics**: F1 Score
    - Problem: At first glance, it was unclear what caused the dramatic difference in F1 scores between models.
    - Solution: Retrieving the precision and recall values used to calculate F1 scores illustrated the specific differences in models.
