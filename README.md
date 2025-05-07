
# Student Performance SQL Analysis

In today's fast-paced and competitive educational environment, understanding the factors that influence student success is more important than ever. Just like the transport system in a bustling city like London must adapt to serve its residents, schools and educators must adapt to meet the needs of students.

This project dives deep into student performance data using SQL to identify trends, patterns, and key success drivers.

## 📊 Dataset Overview

The dataset used is named `student_performance` and contains the following columns:

| Column                   | Definition                                                  | Data Type          |
|--------------------------|-------------------------------------------------------------|--------------------|
| `attendance`             | Percentage of classes attended                              | float              |
| `extracurricular_activities` | Participation in extracurricular activities (Yes/No)    | varchar            |
| `sleep_hours`            | Average number of hours of sleep per night                  | float              |
| `tutoring_sessions`      | Number of tutoring sessions attended per month              | integer            |
| `teacher_quality`        | Quality of the teachers (Low, Medium, High)                 | varchar            |
| `exam_score`             | Final exam score                                            | float              |
| `hours_studied`          | Number of hours studied per week                            | float              |

## 📌 Project Goals

We aim to explore how various lifestyle and academic habits impact students’ academic performance, focusing on three main queries.

### 1. 📈 Study Hours + Extracurricular Impact
- **Query**: Determine if students who study more than 10 hours and participate in extracurriculars score higher.
- **Output**: `avg_exam_score_by_study_and_extracurricular`
- **Columns**: `hours_studied`, `avg_exam_score`

### 2. 🎯 Sweet Spot in Study Hours
- **Query**: Analyze score averages based on grouped study hour ranges.
- **Output**: `avg_exam_score_by_hours_studied_range`
- **Columns**: `hours_studied_range`, `avg_exam_score`
- **Groups**:
  - 1–5 hours
  - 6–10 hours
  - 11–15 hours
  - 16+ hours

### 3. 🏅 Relative Student Ranking
- **Query**: Show students’ class rank without revealing exact scores.
- **Output**: `student_exam_ranking`
- **Columns**: `attendance`, `hours_studied`, `sleep_hours`, `tutoring_sessions`, `exam_rank`
- Uses `DENSE_RANK()` to ensure shared ranks for tied scores and no skipped ranks.

## 🛠️ Technologies

- SQL (with window functions and CASE expressions)
- Python (for DataFrame handling and visualization)
- Jupyter Notebook / SQL IDE

## 📂 File Structure

```
student-performance-sql-analysis/
├── README.md                     # Project documentation
├── student_performance.sql       # SQL queries for analysis
├── notebook.ipynb                # Notebook with results and visualizations (if any)
```

## 👨‍🏫 Conclusion

This project showcases the power of SQL in education analytics. With precise queries and thoughtful logic, it provides actionable insights for teachers and students to enhance academic performance.

---

🖊️ Created by [Lukas Rozado](https://github.com/lukasrozado)
