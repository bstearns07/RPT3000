# 📊 RPT3000 – COBOL Sales Report Generator
![Output](assets/output.png)

## 👨‍💻 Authors

* Ben Stearns  
* Aidan Dunbar  

📅 **Date:** 03/19/2026  

🔗 **GitHub Repository:**  
https://github.com/bstearns07/RPT3000  

---

## 📌 Overview

**RPT3000** is a COBOL program that reads a customer master file and generates a professionally formatted Year-To-Date (YTD) sales report.

The report includes:

* 🧾 Customer details  
* 📈 Current year sales (YTD)  
* 📉 Previous year sales (YTD)  
* 💲 Dollar change in sales  
* 📊 Percentage change in sales  
* 🧮 Grand totals across all customers  

The output is formatted for readability, mimicking a professional business report layout with headings, alignment, and pagination.

---

## ⚙️ How It Works

### 🚀 Initialization

* Opens input and output files  
* Retrieves the current system date and time  
* Prepares report header fields  

### 🔄 Record Processing

* Reads each customer record from the input file  
* For each record:

  * Formats customer information for output  
  * Performs calculations:

    * 💲 **Change Amount** = This YTD − Last YTD  
    * 📊 **Change Percent** = (Change / Last YTD) × 100  

### ⚠️ Edge Case Handling

* If **Last YTD = 0**:

  * Percentage is set to `999.9` to avoid division errors  

### 🖨️ Output Generation

* Writes formatted customer data to the report  
* Updates running totals for:

  * 📈 This YTD sales  
  * 📉 Last YTD sales  

### 🧾 Final Totals

* Calculates grand totals  
* Computes overall percentage change  
* Writes a summary line at the end of the report  

---

## 📁 Files

| 📄 File Name     | 📌 Description                             |
|------------------|-------------------------------------------|
| `RPT3000.cbl`    | COBOL source program                      |
| `JCLRPT2.jcl`    | JCL used to compile and execute program   |
| `README.md`      | Project documentation                     |

---

## 📝 Notes

* ⚙️ Values may be hardcoded for demonstration purposes  
* 🔢 Numeric editing is used to format output fields  
* 🎓 Designed for educational use  
* 💡 Demonstrates:

  * Structured COBOL programming  
  * File handling  
  * Report formatting  
  * Business-oriented calculations  

---
