This project is focused on text classification to determine the authorship of books using machine learning techniques. Here's a summary:

Objective
- To train and evaluate machine learning models that predict the author of a book based on text features, using classification techniques. The team analyzed and compared various algorithms to find the most effective solution.

Steps Undertaken

1. Data Preparation and Preprocessing
- Data Source: Selected five fiction books by different authors from the Gutenberg Digital Books repository.
- Partitioning and Cleaning:
  - Books were divided into 200 segments, each containing 100 words.
  - Garbage characters were removed.
  - The cleaned data was saved as a CSV file for analysis.

2. Feature Engineering

The text data was transformed into numerical features using:
- Bag-of-Words (BoW):
  - Captures word frequencies in the text using CountVectorizer.
  - Considered unigrams and bigrams with a minimum frequency threshold of 3.
- TF-IDF (Term Frequency–Inverse Document Frequency):
  - Weighed words based on their importance in the text while reducing the influence of common words.
- N-gram Models:
  - Extracted contiguous word sequences (e.g., bigrams) to capture contextual information.

3. Classification Models

Each feature engineering method was paired with the following classifiers:
  - Decision Tree: Used for interpretable results but sensitive to overfitting.
  - K-Nearest Neighbor (KNN): Measures similarity between text partitions for classification.
  - Support Vector Machine (SVM): Found to perform best with TF-IDF features.

Steps for each classifier:
  - Data split into training and testing sets.
  - Performance metrics (accuracy, precision, recall, F1-score) were computed.
  - Results visualized through confusion matrices and other evaluation plots.

4. Evaluation
- Cross-Validation: 10-fold cross-validation was conducted to balance the bias-variance trade-off.

Champion Model:
- SVM with TF-IDF emerged as the top-performing model with the highest accuracy, precision, and recall.
- Kernel tuning (e.g., switching from rbf to poly) and data sample size adjustments were explored to optimize performance.

5. Error Analysis and Misclassification Review

- Some authors (e.g., Bryant and Melville) were misclassified due to thematic and stylistic similarities in their works.
- Common elements like adventure themes, vivid imagery, and distinct characterizations contributed to errors.

6. Insights
- Highlighted areas where model performance could improve, such as feature refinement or adding diverse data.

7. Key Results
- Best Model: SVM with TF-IDF features, achieving almost 100% accuracy after dataset augmentation.
- Challenges: Errors stemmed from inherent similarities in the writing styles of certain authors.
- Learnings: The project demonstrated the importance of feature selection and model tuning in text classification tasks.

8. Real-World Application
- The methodology can be extended to other text classification tasks, such as sentiment analysis, topic modeling, or plagiarism detection.
