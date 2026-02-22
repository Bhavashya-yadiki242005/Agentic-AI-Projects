# Multi-Agent Fraud Detection System using CrewAI

This project implements a **multi-agent fraud detection pipeline** using CrewAI.  
It analyzes financial transaction data to identify anomalies such as unusually large transfers, suspicious transaction types, and balance inconsistencies, then generates a structured fraud report.

The system uses specialized AI agents to:

- Load and profile the dataset  
- Detect suspicious patterns  
- Produce a professional fraud detection report  

This project demonstrates how agent-based AI systems can automate data analysis workflows in finance.

---

## Project Overview

Fraud detection in finance involves processing large volumes of transactions and identifying abnormal behavior.  
Instead of relying on a single model, this project uses **CrewAI** to coordinate multiple agents, each with a specific responsibility:

1. **Data Collector** – Reads and profiles the dataset.
2. **Pattern Recognizer** – Detects anomalous transactions.
3. **Fraud Reporter** – Generates a structured fraud report.

These agents work sequentially to provide a complete fraud analysis pipeline.

The dataset used is:

**Synthetic Financial Datasets For Fraud Detection (Kaggle)**  
## Dataset

Synthetic Financial Datasets for Fraud Detection (PaySim)

Download from Kaggle:
https://www.kaggle.com/datasets/ealaxi/paysim1

After downloading, place the CSV file in the project root and update the file path in:

FileReadTool(file_path='Synthetic_Financial_datasets_log.csv')

## Features

- Multi-agent architecture using CrewAI
- CSV-based transaction analysis
- Detection of:
  - High-value transactions
  - Suspicious transaction types (TRANSFER, CASH_OUT)
  - Balance inconsistencies
- Automated executive fraud report generation
- Modular agent/task design
- Extensible for real-world datasets

---

## Tech Stack

- Python 3.10+
- CrewAI
- crewai_tools
- Pandas (via FileReadTool)
- OpenAI-compatible LLM (optional, via API key)

---

## Installation

### 1. Clone or download the repository

bash
git clone <<YOUR_GITHUB_REPO_LINK>>
cd <<PROJECT_FOLDER>>

Or download the ZIP manually.

2. Install dependencies
pip install crewai
pip install crewai_tools
3. Set your OpenAI API key (if required)
import os
os.environ["OPENAI_API_KEY"] = "your-api-key-here"
Dataset

# Download the dataset from Kaggle:

<<INSERT_KAGGLE_DATASET_LINK>>

Place the CSV file in your project directory and update the file path in:

FileReadTool(file_path='Synthetic_Financial_datasets_log.csv')
Agents

1. Data Collector

Loads the CSV dataset

Profiles columns, rows, and missing values

Extracts sample records

Highlights potential anomalies

2. Pattern Recognizer

Identifies:

Very high transaction amounts

TRANSFER and CASH_OUT patterns

Balance inconsistencies

Returns row indices with explanations

3. Fraud Reporter

Produces a professional fraud detection report

Includes:

Executive summary

Key findings

Actionable recommendations

Tasks

Each agent is assigned a task:

Load Task – Dataset profiling and anomaly sampling

Detect Task – Pattern analysis and anomaly detection

Report Task – Structured fraud report generation

The Crew executes these tasks sequentially.

# Running the Project

Run the main script:

python main.py

# This will:

Load the dataset

Detect suspicious transactions

Generate a structured fraud report

Final output is printed to the console.

# Output

The system produces:

Dataset profile (row count, columns, sample records)

List of flagged transactions with explanations

Fraud detection report containing:

Executive summary

Detailed findings

Recommendations

# Example Use Cases

Financial fraud analysis prototypes

Learning multi-agent AI systems

Automated compliance checks

Risk assessment pipelines

