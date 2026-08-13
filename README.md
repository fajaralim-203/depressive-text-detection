# Depressive Text Detection Trained on English Reddit Posts

### AI4ALL Ignite — Summer 2026 | Group 13D

This project explores how Natural Language Processing (NLP) and machine learning can be used to identify depression-associated language in English Reddit posts. Our team compared multiple machine learning approaches to understand how effectively they can classify text as either depression-associated or non-depressive language.

The purpose of this project is **not to diagnose depression**. Instead, the system is designed as a research tool for identifying language patterns that may be useful for further analysis.

---

## Problem Statement

Depression affects millions of people, and people sometimes express emotions and personal experiences through online platforms such as Reddit. These posts provide textual data that researchers can analyze to better understand patterns associated with mental health.

Manually reviewing large amounts of social media text would be difficult and time-consuming. Machine learning and NLP can help researchers analyze this information more efficiently.

Our research question was:

**How can we use machine learning models trained on English Reddit posts to accurately classify depressive language?**

The project also considers the responsible use of AI. A text classification model can make mistakes, contain biases from its training data, or incorrectly classify someone's language. Therefore, its predictions should not be treated as a medical diagnosis.

---

## Key Results

We trained and compared three machine learning models for classifying depression-associated language in English Reddit posts.

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 94.51% | 94.50% | 94.50% | 94.50% |
| Linear SVC | 95.16% | 95.50% | 95.00% | 95.00% |
| BERT | 98.43% | 98.50% | 98.50% | 98.50% |

### Results Interpretation

**BERT achieved the strongest overall performance**, with 98.43% accuracy and approximately 98.50% precision, recall, and F1-score.

Linear SVC performed slightly better than Logistic Regression, reaching 95.16% accuracy compared with 94.51% for Logistic Regression.

These results show that all three models performed well on our test data, while BERT produced the strongest results. However, these scores describe performance on this specific dataset and do not mean that any of the models can diagnose depression.

### Models Compared

1. **Logistic Regression**
   - Used TF-IDF features created from the Reddit text.
   - Served as an interpretable baseline model.

2. **Linear SVC**
   - Used TF-IDF features.
   - Achieved slightly stronger results than Logistic Regression.

3. **BERT**
   - Used tokenized text instead of TF-IDF features.
   - Uses contextual information to understand relationships between words.
   - Achieved the highest performance across all four evaluation metrics.
     
### Evaluation Metrics

We evaluated the models using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrices

These metrics helped us compare overall model performance and examine where incorrect classifications occurred.

---

## Methodologies

Our project followed a supervised machine learning pipeline.

1. We prepared and cleaned the English Reddit post dataset.
2. We divided the data into **80% training data and 20% testing data**.
3. Reddit text was transformed into **TF-IDF features** for Logistic Regression and Linear SVC.
4. Logistic Regression and Linear SVC were trained using the labeled training posts.
5. The text was tokenized separately for **BERT**, which was fine-tuned for binary text classification.
6. Each trained model predicted labels for previously unseen test posts.
7. We evaluated performance using accuracy, precision, recall, F1-score, and confusion matrices.
8. We compared the models to understand differences in their performance.
9. The trained system was connected to a **Streamlit application** where new text could be entered for classification.

The application returns a classification such as **"non-depressive language"** or **"depression-associated language."**

---

## Responsible AI, Bias, and Societal Impact

Because this project involves mental-health-related language, responsible AI was an important part of our work.

### Potential Positive Impacts

- Support research into mental health language patterns
- Help analyze large amounts of textual data efficiently
- Identify broader trends in online discussions
- Support mental health awareness and future research
- Analyze changes in language patterns during major events or stressful periods

### Potential Risks and Limitations

The model should **never be used as a replacement for a mental health professional or as a diagnostic tool**.

Predictions can be incorrect because language is complex and highly dependent on context. Bias can also occur if certain populations, writing styles, cultures, dialects, or types of Reddit users are underrepresented in the training dataset.

False positives may label ordinary language as depression-associated, while false negatives may fail to recognize relevant language patterns.

### Bias Mitigation

Possible mitigation strategies include:

- Evaluating more than accuracy alone
- Reviewing false positives and false negatives
- Testing performance across different data slices when demographic information is ethically available
- Using more diverse and representative datasets
- Clearly documenting limitations
- Keeping human review involved in high-impact applications
- Avoiding claims that the model can diagnose depression

---

## Limitations and Future Work

There are several ways this project could be improved in the future.

The dataset focuses on **English Reddit posts**, so the results may not generalize to other languages, social media platforms, cultures, or populations.

Future work could include:

- Testing the models on additional datasets and platforms
- Expanding the project to additional languages
- Conducting more detailed bias and fairness evaluations
- Improving contextual text preprocessing
- Performing additional hyperparameter tuning
- Analyzing why the models disagree on specific examples
- Improving the Streamlit application
- Exploring model explainability and interpretability
- Evaluating performance on more diverse language patterns

These improvements could make the project more robust while maintaining responsible and transparent use of AI.

---

## Data Sources

Our project used the Depression Reddit Cleaned dataset from Kaggle. The dataset contains cleaned English Reddit posts labeled for depressive and non-depressive language and was used to train and evaluate our text classification models.

- **Kaggle Dataset:** [Depression Reddit Cleaned](https://www.kaggle.com/datasets/infamouscoder/depression-reddit-cleaned)

---

## Technologies Used

- Python
- pandas
- Natural Language Processing (NLP)
- TF-IDF
- Logistic Regression
- Linear SVC
- BERT
- scikit-learn
- Streamlit
- GitHub
- GitHub Pages

---

## Skills Developed

Through this AI4ALL Ignite project, I gained experience with:

- Machine learning
- Natural Language Processing
- Data preprocessing
- Model training and testing
- Model evaluation
- Responsible AI
- Bias identification and mitigation
- Data visualization
- GitHub
- Collaborative AI development
- Technical presentations

---

## Author

**Fajar Alim**

AI4ALL Ignite — Summer 2026

This portfolio page presents work completed as part of a collaborative AI4ALL Ignite group project.

### Project Team

- Jimmy Zheng
- Fajar Alim
- Shreeshkumar Lillyprabhu

---

## Acknowledgments

This project was developed through the **AI4ALL Ignite** program. Thank you to our instructors, AI Project Leads, Student Coordinators, mentors, and team members for their guidance and feedback throughout the project.
