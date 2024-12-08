# **NoSQL MongoDB Challenge: Eat Safe, Love**

![MongoDB Logo](https://www.mongodb.com/assets/images/global/leaf.png)

---

## **📜 Project Overview**
This project involves working with a dataset of food establishments across the United Kingdom. Using **MongoDB**, we analyze food hygiene ratings to provide valuable insights for the editors of a food magazine, *Eat Safe, Love*. The challenge includes tasks such as database setup, data cleaning, updates, and exploratory analysis.

The key goals of this challenge:
1. Import a dataset into MongoDB and set up the database and collection.
2. Perform data updates and modifications to meet specific requirements.
3. Conduct exploratory analysis to answer meaningful questions about the dataset.

---

## **📁 Directory Structure**
```
nosql-challenge/
│
├── Starter_Code/
│   ├── NoSQL_setup_starter.ipynb   # Notebook for database setup and data updates
│   ├── NoSQL_analysis_starter.ipynb # Notebook for exploratory analysis
│   ├── Resources/
│   │   └── establishments.json      # Dataset in JSON format
│
├── README.md                        # This README file
└── .gitignore                       # Git ignore file
```

---

## **⚡ Getting Started**

### **🔧 Prerequisites**
- **Python 3.x**
- **MongoDB Community Server**
- **Libraries**:
  - `pymongo`
  - `pandas`
  - `pprint`
  - `dnspython` (optional for advanced MongoDB connections)

### **📥 Installation**
1. Install MongoDB from the [official website](https://www.mongodb.com/try/download/community).
2. Install required Python libraries:
   ```bash
   pip install pymongo pandas
   ```

3. Clone this repository to your local machine:
   ```bash
   git clone <repository-url>
   cd nosql-challenge
   ```

---

## **🚀 Step-by-Step Instructions**

### **1️⃣ Database Setup**
- Open **`NoSQL_setup_starter.ipynb`** in Jupyter Notebook or VS Code.
- Follow these steps:
  1. Import the dataset (`establishments.json`) into MongoDB using the `mongoimport` command:
     ```bash
     mongoimport --db uk_food --collection establishments --drop --file Starter_Code/Resources/establishments.json --jsonArray
     ```
  2. Use `pymongo` to connect to the MongoDB instance, confirm the collection setup, and explore the data.

### **2️⃣ Update the Database**
- Add a new restaurant, **Penang Flavours**, to the database.
- Update specific fields (e.g., assign `BusinessTypeID`).
- Remove irrelevant data (e.g., establishments in Dover).
- Convert data types (e.g., `latitude`, `longitude`, and `RatingValue`).

### **3️⃣ Exploratory Analysis**
- Use **`NoSQL_analysis_starter.ipynb`** for analysis.
- Answer the following key questions:
  1. **Which establishments have a hygiene score of 20?**
  2. **How many establishments in London have a `RatingValue` ≥ 4?**
  3. **What are the top 5 establishments near "Penang Flavours" with `RatingValue` = 5, sorted by hygiene score?**
  4. **Which Local Authorities have the most establishments with a hygiene score of 0?**

---

## **🛠 Features**
1. **Database Setup**:
   - Fully documented setup steps with code snippets.
2. **Data Cleaning**:
   - Handles invalid or non-standard data.
   - Ensures data types are accurate.
3. **Exploratory Analysis**:
   - Queries are optimized for efficiency.
   - Results are converted into readable Pandas DataFrames.

---

## **📊 Sample Insights**
### **Top 5 Establishments Near "Penang Flavours"**
| Establishment Name | Hygiene Score | Latitude    | Longitude   |
|--------------------|---------------|-------------|-------------|
| Example 1          | 0             | 51.490010   | 0.083850    |
| Example 2          | 1             | 51.490100   | 0.083800    |

### **Top 10 Local Authorities with Hygiene Score 0**
| Local Authority Name | Count |
|----------------------|-------|
| Thanet               | 1130  |
| Greenwich            | 882   |
| Swale                | 713   |

---

## **🛡 Challenges Faced**
1. **Data Cleaning**:
   - Converting non-numeric values (e.g., `"Pass"`) into nulls or integers.
2. **Aggregation Pipelines**:
   - Grouping and sorting data effectively using MongoDB's `aggregate()` method.

---

## **🤝 Contributions**
Contributions are welcome! Feel free to fork this repository, create a new branch, and submit a pull request.

---

## **📄 License**
This project is licensed under the MIT License. See `LICENSE` for more information.

---

## **👩‍💻 Author**
**[Jonas]**

For any inquiries or suggestions, reach out via [your email].

---

### **✨ Happy Coding!**
