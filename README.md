#  Student Performance Analysis - ML Project

This project aims to analyze student performance data and prepare it for training Machine Learning models. The process involves data ingestion, preprocessing, exploratory data analysis, and visualization, followed by model training and evaluation.

---

##  Project Structure

mlproject1/
│
├── notebook/
│ └── data/
│ └── stud.csv # Raw student performance dataset
│
├── src/
│ └── components/
│ └── data_ingestion.py # Contains the DataIngestion class
│
├── logs/
│ └── *.log # Auto-generated log files
│
├── artifacts/
│ ├── raw.csv # Saved raw data
│ ├── train.csv # Training data
│ └── test.csv # Test data
│
├── requirements.txt
└── README.md



---

##  Key Components

### `DataIngestion` Class
Handles:
- Reading CSV data from disk.
- Saving the raw data.
- Splitting it into train and test datasets.
- Creating folders automatically if they don't exist.
- Logging the entire process.

```python
from src.components.data_ingestion import DataIngestion

ingestor = DataIngestion()
train_path, test_path = ingestor.initiate_data_ingestion()


Input Dataset
File: stud.csv
Location: notebook/data/stud.csv

This CSV contains student information such as:

Gender

Math score

Reading score

Writing score

Test preparation course, etc.

 How It Works
Read the raw dataset.

Create the output directory (if it doesn't exist).

Save the original raw dataset.

Split it into train and test sets (80:20).

Save those sets into the artifacts/ directory.

Log every step for debugging and tracking.


Requirements
Install dependencies with:

pip install -r requirements.txt

 Logging
All steps of data ingestion are logged to a file inside the logs/ directory. Log filenames are time-stamped like 05_30_2025_55_12.log.

Sample Output
After running the ingestion script, the following files are created:

artifacts/raw.csv

artifacts/train.csv

artifacts/test.csv

You can now use these files for further preprocessing, EDA, or ML model training.


 Future Enhancements
Add data validation before splitting.

Automatically detect and handle missing values.

Integrate preprocessing, EDA, and model training in a complete pipeline.

Author
Bilal
AI/ML Enthusiast | Data Science Projects
#MadeWithPython 


