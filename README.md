# 📊 Task 1: Data Cleaning and Preprocessing

## 🚀 Overview
The goal of this task was to clean and preprocess a raw job placement dataset using **Python (Pandas)**.

---

## 🗂 Dataset Description

**Filename:** `job_placement_data.csv`  
**Rows:** 699  
**Columns:** 12  

### Original Columns:
- `id`
- `name`
- `gender`
- `age`
- `degree`
- `stream`
- `college_name`
- `placement_status`
- `salary`
- `gpa`
- `years_of_experience`
- `skills`

---

## 🧹 Cleaning & Preprocessing Steps

1. **Column Renaming**
   - `college_name` → `college`
   - `years_of_experience` → `experience`

2. **Removed Duplicates**
   - Used `.drop_duplicates()` to eliminate any repeated records.

3. **Standardized Text Values**
   - Cleaned and unified `gender` values to lowercase (`male`, `female`).

4. **Column Formatting**
   - Converted all column names to lowercase and replaced spaces with underscores for consistency.

5. **Missing Value Handling**
   - Filled missing `age` values using grouped **mode** based on `experience`.
   - If mode was not available, used **group median**.
   - Final fallback used **overall median** to ensure no nulls remained.

6. **Data Type Fixes**
   - `age` and `salary` → `int`
   - `gpa` and `experience` → `float`

7. **Exported Final Dataset**
   - Cleaned data saved as `job_placement_data_cleaned.csv`

---

## 💻 Tools Used

- **Language:** Python 3.x  
- **Libraries:** Pandas  
