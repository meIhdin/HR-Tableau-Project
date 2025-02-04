# Tableau Project - HR Dashboard  

This Tableau project is a step-by-step learning experience in building dashboard projects using Tableau, from requirements to a professional dashboard.  

## Project Materials  

**Download:** [Tableau-HR-Project-Materials.zip](#)  

The Zip folder contains the following:  

- **Project Data:**  
  The data used in this HR Dashboard project is generated using a combination of ChatGPT prompts and the Python Faker library. This dataset simulates employee information typically found in HR systems, including demographics, job details, salary, performance evaluations, and attrition data. The generated data mimics real-world HR data, providing a rich dataset for analysis and visualization in Tableau.  

- **Icons & Images:**  
  The icons used in the HR Dashboard are sourced from [Flaticon](https://www.flaticon.com/) and customized using Photopea to match the dashboard’s color scheme. The PDS (Photopea files) can be found in the `icon` folder of the zip file for further editing if needed.  

- **Mockups:**  
  - The initial dashboard mockup was created using the Procreate app on a tablet.  
  - The dashboard container mockups were created using [draw.io](https://app.diagrams.net/).  

- **Tableau Project File:**  
  The project file created during the course is included in the zip file. You can also download it directly from my [Tableau Public Profile](#).  

---

## ⚠️ IMPORTANT ⚠️  

If you share the Tableau project on Tableau Public or LinkedIn, I’d appreciate it if you mention my link.  
 

---

## Other Resources  

- **[FIGMA – HR Dashboard Background Design](#)**  
- **[Download Tableau Public](#)** 
- **[Tableau Public Account](#)** 
- **[Download Draw.io](https://app.diagrams.net/)**  

---

## User Story - HR Dashboard  

**As an HR manager,** I want a comprehensive dashboard to analyze human resources data, providing both summary views for high-level insights and detailed employee records for in-depth analysis.  

---

### Summary View  

The summary view is divided into three main sections: **Overview**, **Demographics**, and **Income Analysis**.  

#### **1. Overview**  
- Display the total number of hired employees, active employees, and terminated employees.  
- Visualize the total number of hired and terminated employees over the years.  
- Present a breakdown of total employees by department and job titles.  
- Compare total employees between headquarters (HQ) and branches (New York is the HQ).  
- Show the distribution of employees by city and state.  

#### **2. Demographics**  
- Present the gender ratio in the company.  
- Visualize the distribution of employees across age groups and education levels.  
- Show the total number of employees within each age group.  
- Show the total number of employees within each education level.  
- Present the correlation between employees' educational backgrounds and their performance ratings.  

#### **3. Income Analysis**  
- Compare salaries across different education levels for both genders to identify any discrepancies or patterns.  
- Present how age correlates with the salary for employees in each department.  

---

### Employee Records View  

Provide a comprehensive list of all employees with necessary information such as:  
- Name  
- Department  
- Position  
- Gender  
- Age  
- Education  
- Salary  

💡 **Filters:** Users should be able to filter the list based on any of the available columns.  

---

### Data Generation  

**Data Creation Process:**  

The employee dataset consists of **8,950 records** and was generated using Python. Below is the breakdown of the dataset creation process:  

#### **ChatGPT Prompts**  
The dataset was generated using a Python script based on the following requirements:  

1. **Employee ID:** A unique identifier for each employee.  
2. **First Name & Last Name:** Randomly generated using the Python Faker library.  
3. **Gender:** Randomly chosen with:  
   - **46% probability** for ‘Female’  
   - **54% probability** for ‘Male’  
4. **State & City:** Randomly assigned from a predefined list of states and their cities.  
5. **Hire Date:** Randomly generated with custom probabilities for each year from 2015 to 2024.  
6. **Department:** Randomly chosen from a list of departments with the following probabilities:  
   - Example: `Engineering (40%)`, `HR (20%)`, `Sales (30%)`, etc.  
7. **Job Title:** Randomly selected based on the department, with specific probabilities for each job title within the department.  
8. **Education Level:** Determined based on the job title, chosen from a predefined mapping of job titles to education levels.  
9. **Performance Rating:** Randomly selected from the following:  
   - `Excellent`  
   - `Good`  
   - `Satisfactory`  
   - `Needs Improvement`  
   ...with specified probabilities for each rating.  
10. **Overtime:** Randomly chosen with:  
    - **30% probability** for ‘Yes’  
    - **70% probability** for ‘No’  
11. **Salary:** Generated based on the department and job title, within specific ranges.  
12. **Birth Date:** Generated based on:  
    - Age group distribution  
    - Job title requirements  
    - Consistency with the hire date.  
13. **Termination Date:**  
    - Assigned to **11.2%** of employees.  
    - Ensures the termination date is at least **6 months after the hire date**.  
    - Custom probabilities for each year from 2015 to 2024.  
14. **Adjusted Salary:** Calculated based on:  
    - Gender  
    - Education level  
    - Age  
    - Specific multipliers and increments.  

---

#### **Python Script Requirements**  

The script adheres to the following guidelines:  

- Cleanly structured code with the use of functions for modularity.  
- Inclusion of **comments** to explain each step of the process.  
- Use of Python libraries such as:  
  - `Faker` for generating random names and data.  
  - `NumPy` and `Pandas` for efficient data manipulation.  
- Probabilities and logic ensure the dataset mimics **real-world HR data**.  

---  

💡 **Pro Tip:** For reproducibility, the script includes a random seed to ensure the generated dataset remains consistent.  
