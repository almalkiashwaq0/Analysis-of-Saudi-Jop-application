# 🇸🇦 Saudi Job Market Analysis (Jadarat) — EDA

This project performs **Exploratory Data Analysis (EDA)** on job postings from the **Jadarat** platform to better understand the Saudi labor market—roles in demand, locations, sectors, experience/education requirements, and posting activity over time.

- **Source:** Jadarat (public job postings)
- **Dataset size:** **1470 rows × 18 columns**

---

## 🎯 Project Purpose
- **Profile data quality** and **understand feature distributions/relationships**.  
- Explore job demand by **city, region, sector/industry, and employment type**.  
- Analyze **experience & education requirements**, and (where available) **salary ranges**.  
- Surface insights that can guide **job seekers, universities, and workforce planning**.

---

## 📂 Dataset Description
**Shape:** 1470 rows × 18 columns  
**Unit of analysis:** one row = one job posting on Jadarat.

**Typical fields in this dataset (18 columns):**
1. `job_post_id` — Unique posting identifier  
2. `job_title` — Role title  
3. `employer_name` — Hiring organization  
4. `sector` — Public / Private (or similar)  
5. `industry` — Industry/category  
6. `city` — City of the role  
7. `region` — Province/region (e.g., Riyadh, Makkah, Eastern)  
8. `employment_type` — Full-time / Part-time / Contract / Internship  
9. `work_model` — Onsite / Hybrid / Remote  
10. `experience_level` — Entry / Mid / Senior, or years  
11. `education_level` — Required degree/qualification  
12. `salary_min` — Lower bound (if provided)  
13. `salary_max` — Upper bound (if provided)  
14. `posted_date` — Date listed  
15. `closing_date` — Application deadline (if provided)  
16. `skills` — Key/required skills (string or list)  
17. `applicants_count` — Number of applicants (if available)  
18. `job_description` — Text summary of duties/requirements

---

## 🧹 Data Quality & Preparation

### 2️⃣ Data Quality Checks
- **Reliability** → **yes**  
- **Timeliness** → **yes**  
- **Consistency** → **yes**  
- **Relevance** → **yes**  
- **Uniqueness** → Removed duplicate entries using **`job_post_id`**  
- **Completeness** → Filled null values via **imputation with constant values**  
- **Accuracy** → **fixed** (cleaned and standardized during preprocessing)

---

## 📊 Key Insights

1️⃣ **Gender Requirements**  
   - We found a close gender requirement gap, where job postings open to both genders achieved the highest share at 39.9%, followed by male-only roles at 32.7%, and female-only roles at 27.4%, as shown in the chart below.
     ![Gender Chart](images/Gender.png)


2️⃣ **Salary Insights**  
   - The **average salary** across all postings is around **5,285 SAR**, with some roles offering up to **35,000 SAR**.
   - For **fresh graduates**, the **average salary** drops to around **4,712 SAR**.
   - Jobs specifically targeted **for women only** tend to **offer lower salaries** compared to roles requiring **men only** or **open to both genders** *(as shown in the chart)*.
     ![Salary Chart](images/Salary.png)

3️⃣ **Regional Demand**  
   - **44.8%** of all job postings are concentrated in the **Riyadh** region.  
   - **Makkah** follows as the **second-highest** region, with **28.3%** of postings.
   - *(as shown in the chart)*.
     ![Region Chart](images/Region.png)

4️⃣ **Most Demanded Role**  
   - As shown in the figure, the **most posted job** was **“Seller”**, appearing **98 times** across listings.
     ![Jobs Chart](images/Jobs.png)

---

🌐 Explore the storytelling dashboard on Streamlit: [Click Here](https://usecase5jadarat.streamlit.app/)

