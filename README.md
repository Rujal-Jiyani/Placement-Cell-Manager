# Placement Cell Manager 🎓💼

A robust, high-performance C++ CLI application designed to automate the parsing, storage, and analysis of large-scale university placement data. 

Built entirely with core C++ and custom data structures, this engine processes multi-round, multi-year recruitment data from raw CSVs to compute branch-wise placement rates, pass percentages, and salary statistics.

## 🚀 Key Features

* **Lightning-Fast Lookups:** Implemented a custom hash table with linear probing to cut student-record retrieval times from O(n) to O(1).
* **Automated Data Pipeline:** Engineered a robust file-handling system to parse, validate, and normalize data across 30+ raw CSV and TXT files.
* **Complex OOP Architecture:** Designed a highly scalable, pointer-based nested object graph to model the real-world recruitment process.
* **Deep Analytics:** Automatically calculates and generates reports on branch-wise placement success, round-over-round drop-off rates, and salary metrics.
* **Menu-Driven CLI:** A lightweight, intuitive command-line interface for admins to query placement statistics dynamically.

## 🧠 System Architecture

The core of the application relies on a strictly defined, multi-layered nested object hierarchy. This prevents data duplication and ensures efficient memory management.

`Database` ➔ `Year` ➔ `Company` ➔ `Round` ➔ `Student`

* **Database:** The central controller managing the entire application state.
* **Year:** Segregates data by recruitment cycles (e.g., 2019, 2020).
* **Company:** Holds aggregate data and metadata for specific recruiters (e.g., Google, BlackRock, Sprinklr).
* **Round:** Tracks progression (HR, Technical R1, R2, R3, Final) to monitor pass/fail rates.
* **Student:** The leaf node containing unique identifiers, academic branches, and salary details, stored in a custom hash map for O(1) access.

## 🛠️ Tech Stack

* **Language:** C++ (Standard Template Library, core File I/O)
* **Concepts Applied:** Object-Oriented Programming (OOP), Data Structures & Algorithms (Hashing, Linear Probing), Pointers & Memory Management, String Parsing.
* **Data Format:** CSV, TXT

## 📂 Dataset Structure

The engine is built to ingest real-world, unstructured recruitment datasets. The provided mock data includes multi-round CSVs for major tech and finance firms across different academic years:
* `Company_Year_Round.csv` (e.g., `Google_2020_R1.csv`, `BlackRock_2019_Final.csv`)
* `Year.txt` (Configuration files for dynamic environment loading)

## 💻 Getting Started

### Prerequisites
* A standard C++ compiler (GCC/G++, Clang, or MSVC)

### Installation & Execution

1. Clone the repository:
   ```bash
   git clone [https://github.com/yourusername/Placement-Cell-Manager.git](https://github.com/yourusername/Placement-Cell-Manager.git)
   ```

2. Navigate to the project directory:
   ```bash
   cd Placement-Cell-Manager
   ```

3. Compile the C++ source code:
```bash
g++ 1_Main.cpp DataStructure.cpp -o PlacementManager
```

4. Run the executable:
```bash
./PlacementManager
```

🤝 Team
Originally developed as a collaborative engineering project by a 4-member team to solve real-world data normalization and algorithmic optimization challenges.
