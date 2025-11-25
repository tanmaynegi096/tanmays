# Project Statement: Smart E-Commerce Price Tracker

## 1. Problem Statement
In the current e-commerce landscape, product prices on platforms like Amazon and Flipkart are highly dynamic, often fluctuating multiple times a day due to algorithmic pricing. 

For students and budget-conscious buyers, manually tracking these prices to find the best deal is efficient and error-prone. There is no easy way to know if a current price is a "good deal" without historical context, and users often miss limited-time price drops because they cannot be online 24/7.

## 2. Project Objectives
The primary objective of this project is to develop an automated software solution that:
* **Eliminates manual effort:** Automatically visits product pages to fetch live prices.
* **Provides financial benefit:** Helps users save money by alerting them exactly when a price drops.
* **Enables data-driven decisions:** Stores historical price data so users can visualize price trends over time.

## 3. Scope of the Project
This project is developed as a modular desktop application using Python.

### 3.1 In-Scope (What the project does)
* **Web Scraping:** The system will extract specific data points (Product Name, Price, Availability) from provided URLs.
* **Data Storage:** A local relational database (SQLite) will persist user preferences and price history.
* **Alert Mechanism:** The system will compare live prices against a user-defined "Target Price" and trigger a notification.
* **User Management:** Users can perform CRUD (Create, Read, Update, Delete) operations on their tracking list.

### 3.2 Out-of-Scope (What the project does not do)
* **Automatic Purchasing:** The system will not perform the actual transaction/checkout.
* **Payment Integration:** No payment gateways are involved.
* **Mobile Application:** The interface is currently a Command Line Interface (CLI), not a mobile app.

## 4. Target Users
* **Students:** Who have limited budgets and need to wait for discounts on textbooks or electronics.
* **Smart Shoppers:** Users who want to track high-value items (like Laptops or Cameras) to buy at the lowest historical price.
* **Data Enthusiasts:** Users interested in analyzing price trends and volatility of products.

## 5. High-Level Features
1.  **Dashboard/Menu:** A simple interface to view all tracked items and their last recorded prices.
2.  **Smart Scraper:** A robust scraping module that handles HTML parsing and cleans currency symbols (e.g., converting "₹1,499" to `1499.0`).
3.  **Price Comparison Logic:** An algorithm that checks `if Current_Price < Target_Price` to trigger alerts.
4.  **History Logger:** Automatically records the timestamp and price every time a check is performed.
5.  **Error Resilience:** Handles network timeouts or invalid URLs gracefully without crashing.

## 6. Technical Stack
* **Programming Language:** Python 3.8+
* **Database:** SQLite 3
* **Core Libraries:**
    * `Requests`: For HTTP connectivity.
    * `BeautifulSoup (bs4)`: For HTML parsing and data extraction.
    * `Time/Datetime`: For scheduling and timestamping.
