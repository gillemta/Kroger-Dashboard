# Kroger Dashboard Web Application

This repository contains the source code for a data analytics web application developed as part of a group project assignment. The project leverages modern data engineering practices and cloud technologies (Azure) to provide interactive insights into retail customer behavior based on anonnymized 84.51°/Kroger data.

## Project Overview

The goal of the project is to explore real-world retail data and answer key questions regarding customer engagement and demographic factors. Specifically, the application helps answer:
- **How does customer engagement change over time?**
  (e.g., changes in spend, basket items, and overall engagement trends)
- **Which demographic factors (e.g., household size, presence of children, income) appear to affect customer engagement?**

Using sample household transactions and demographic data, the application process and aggregates data with [Polars](https://www.pola.rs/) and visualizes the results using interactive [Plotly](https://plotly.com/python/) charts. The application also provides an interactive data table (powered by grid.js) to browse through transaction records with features like search, sorting, and pagination.

## Features

- **Interactive Dashboard:**
  - Bar and pie charts illustrating total and average spending segmented by Age Range, Marital Status, Income Range, and Number of Children.
- **Dynamic Data Table:**
  - Display of transaction details with search, sorting and pagination.
- **User Authentication:**
  - Simple registration and login pages that allow users to create accounts and securely access the dashboard.
- **Data Processing:**  
  - Fast data aggregation and manipulation using Polars.
- **Azure Integration (Planned/Optional):**  
  - Includes code for connecting to Azure Blob Storage and PostgreSQL, supporting potential cloud-based data storage and deployment.
 
## Setup and Installation

1. **Clone the Repository:**

  ```bash
  git clone https://github.com/yourusername/kroger-dasboard.git
  cd kroger-dasboard
  ```

2. **Create a Virtual Environment & Install Dependencies:**

  ```bash
  python -m venv venv
  source venv/bin/activate  # On Windows: venv\Scripts\activate
  pip install -r requirements.txt
  ```

3. Run the Application:
  ```bash
  python app.py
  ```
  By default the application will run in debug mode on `http://0.0.0.0:5000/`

## Usage

**Registration & Logic**:
- On first visit, you'll be directed to the registration page. Create an account using your email, username, and password.
- After registration, use your credentials on the login page to access the dashboard.

**Dashboard**:
- View interactive charts showing spending and engagement metrics segmented by demographics.
- Browse the transaction data via the dynamic table. Use the search box to filter results by household number, and sort columns as needed

**Data Processing**:
- The backend aggregates and processes data from `detailed-data.csv` using Polars, providing real-time charts and statistics.
- Although the repository contains sample login data stored in CSV, the application includes code to connect to a PostgreSQL database for user management, which can be enabled with proper configuration.

## Additional Context

The project was developed based on the following assignment brief:
```
Project Abstract
Organizations today need to leverage modern data engineering as data volume and complexity grow. In retail, machine learning can analyze extensive datasets to forecast product demand and optimize pricing strategies. This project explores real-world retail data from 84.51°/Kroger to build an interactive web application on Azure, making the customer's shopping experience easier.

Key Questions:
  1. How does customer engagement change over time?
  2. Which demographic factors affect customer engagement?
```
This README summarizes the core components of the assignment and provides insight into the structure and functionality of the web application.
