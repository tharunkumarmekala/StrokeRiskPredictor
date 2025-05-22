A. Data preprocessing
1.	Data Source and Feature Selection
The dataset used in this study was acquired from a publicly available online healthcare repository, specifically the Stroke Prediction Dataset[14]. It contained demographic, clinical, and lifestyle attributes pertinent to stroke occurrence. Key features extracted and utilized for the analysis included sex, age, hypertension history, previous stroke events (derived from the original heart_disease column), average glucose levels, BMI, and smoking status. These variables were selected based on their established roles as stroke risk factors, recognized in both epidemiological and clinical studies. The original dataset contained 5,110 patient records with 12 attributes.
2. Variable Transformation and Categorization
To prepare the dataset for analysis, all variables underwent transformation into standardized categorical formats. This involved encoding the variables into numerical representations suitable for machine learning algorithms. Based on specific criteria or groupings, variables were converted into integer codes, using binary values (0 or 1) or other numerical values like 0, 1, 2, or 3, depending on the variable's nature. This encoding process was applied uniformly to both the original features and the synthetically generated variables (Cholesterol, Hypertension, Atrial Fibrillation), ensuring they were also converted into these defined integer categories. The final dataset contained all features, including synthetic ones, in a numerical, integer-encoded format.
3. Handling Missing Data
Missing values, specifically 201 entries in the BMI column (3.93%), were addressed. Given the categorical nature of the processed BMI variable, mode imputation was used for the BMI column to preserve data integrity. The article, however, states that an Iterative Imputer was applied using a Random Forest Regressor for the initial, likely numerical, BMI column.
4. Dataset Balancing
The initial dataset presented a significant class imbalance, with only 4.87% positive stroke cases. To prevent bias towards the majority class, the raw dataset was rebalanced. This process created a base of 500 samples with an equal number of stroke and non-stroke cases (n=250 each). Oversampling techniques (bootstrapping) were applied to the minority class (stroke cases) if the original count was less than 250. Random undersampling was used for the majority class (non-stroke cases) to preserve comparability. This class balancing is crucial for improving recall in minority class predictions. The article discusses using Oversampling, Undersampling, and SMOTE for mitigation.
5. Synthetic Data Augmentation
To further augment the dataset and enhance generalization, an additional 1,500 synthetic samples were generated (750 for each class). This was achieved using a modified k-nearest neighbors (k-NN) based synthetic sampling method, inspired by and aligned with SMOTE. Feature scaling (Min-Max normalization) was performed before neighbor computation. Synthetic samples were rounded and clipped to match valid categorical ranges.
6. Final Dataset Structure
After rebalancing and synthetic augmentation, the final dataset comprised 2,000 observations with equal representation of stroke and non-stroke cases. Each feature was integer encoded and organized in a fixed sequence: Age, Sex, BMI, Cholesterol, Hypertension, Atrial Fibrillation, Diabetes, Smoking, Previous Stroke, and Stroke (target variable). This structured and discretized format improved interpretability and computational efficiency. The resulting dataset was clean, balanced, and well-suited for machine learning classification tasks. The feature definitions and encoding scheme are detailed in Table 1.
Table 1: Clinical and Demographic Variables with Encoding
Feature Name	Description	Type
Age	Patient's age category (1 = Young, 2 = Middle, 3 = Elderly)	Categorical
Sex	Biological sex (0 = Female, 1 = Male)	Binary
BMI	Body Mass Index (0–3 scale based on range)	Ordinal
Cholesterol	Cholesterol level (0 = Normal, 1 = High, 2 = Very High)	Ordinal
Hypertension	Hypertension stage (0 = None, 1 = Stage 1, 2 = Stage 2)	Ordinal
Atrial Fibrillation	Presence of AFib (0 = No, 1 = Yes)	Binary
Diabetes	Diabetes diagnosis (0 = No, 1 = Yes)	Binary
Smoking	Smoking status (0 = Non smoker, 1 = Smoker)	Binary
Previous Stroke	History of prior stroke (0 = No, 1 = Yes)	Binary
Stroke (Target)	Stroke outcome (0 = No, 1 = Yes)	Binary

