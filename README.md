# Patient Management System

This repository contains a Python-based program for managing patient data. The program allows users to:
- View patient data.
- Add new patients.
- Analyze and visualize patient data.
- Save the data for future use.

## Team Member
- **Ibrahim Omar Toma**

---

## Dataset Details

### Initial Dataset
- **Filename**: `patients_data.csv`
- **Columns**:
  - `Name`: Name of the patient.
  - `Patient Number`: Unique identifier for the patient.
  - `Age`: Age of the patient.
  - `Gender`: Gender of the patient (Male/Female).
  - `Disease`: Name of the disease the patient is diagnosed with.
  - `Disease Type`: Type of disease (Genetic/Non-genetic).
  - `Diagnosis Date`: Date when the diagnosis was made.
  - `Family History`: Indicates if the disease has a family history (Yes/No).

### New Dataset
- The program creates a new dataset if `patients_data.csv` is not found.
- The new dataset will be an empty CSV file with the same columns as above.

---

## Code Explanation

### Functions and Methods

#### 1. `read_patients(file_name="patients_data.csv")`
- **Purpose**: Reads the patient data from a CSV file.
- **Input**: File name (default: `patients_data.csv`).
- **Output**: A DataFrame containing the patient data. If the file is not found, an empty DataFrame is returned.
- **Exception Handling**: Manages `FileNotFoundError` by creating a new dataset.

#### 2. `display_patients(df)`
- **Purpose**: Displays the patient data in a tabular format.
- **Input**: A DataFrame containing patient data.
- **Output**: Prints the data to the console. If the dataset is empty, a message is displayed.

#### 3. `add_patient(df)`
- **Purpose**: Adds a new patient's data to the DataFrame.
- **Inputs**:
  - `Name`: Patient's name.
  - `Patient Number`: Unique identifier for the patient.
  - `Age`: Patient's age (must be a positive integer).
  - `Gender`: Gender of the patient (Male/Female).
  - `Disease`: Name of the disease.
  - `Disease Type`: Type of the disease (Genetic/Non-genetic).
  - `Diagnosis Date`: Date of diagnosis (YYYY-MM-DD).
  - `Family History`: Indicates if the disease has a family history (Yes/No).
- **Outputs**:
  - Adds the new patient to the DataFrame.
  - Prints a success message if the patient is added successfully.
  - Handles invalid inputs (e.g., duplicate patient numbers, invalid age, etc.).

#### 4. `analyze_and_visualize(df)`
- **Purpose**: Analyzes and visualizes patient data.
- **Inputs**: A DataFrame containing patient data.
- **Outputs**:
  - Prints:
    - Average age of patients.
    - Gender distribution.
    - Disease type distribution.
  - Generates and saves bar charts for gender distribution and disease type distribution.
- **Exception Handling**:
  - Manages cases where the dataset is empty or contains invalid age data.

#### 5. `save_data(df, file_name="patients_data.csv")`
- **Purpose**: Saves the patient data to a CSV file.
- **Input**:
  - DataFrame containing patient data.
  - File name (default: `patients_data.csv`).
- **Output**: Saves the data and prints a success message.

### Main Program (`main()`)
- **Purpose**: Provides a user interface for interacting with the program.
- **Process**:
  1. Loads the dataset using `read_patients`.
  2. Displays a menu of options:
     - Display current patients.
     - Add a new patient.
     - Analyze and visualize data.
     - Save data and exit.
  3. Executes the user's choice using the appropriate functions.
  4. Loops until the user chooses to save and exit.

---

## File Outputs

### Output Charts
1. **Gender Distribution** (`gender_distribution.png`): Bar chart showing the number of male and female patients.
2. **Disease Type Distribution** (`disease_type_distribution.png`): Bar chart showing the count of genetic and non-genetic diseases.

### Saved Dataset
- **File**: `patients_data.csv`
- **Contents**: Includes all patient data added during the program's execution.

---

