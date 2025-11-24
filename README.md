# Smart Price Tracker Project 🛒

This is my Python project for the **VITyarthi Build Your Own Project** course. 

## 🎯 Problem Statement
I noticed that prices on e-commerce websites fluctuate frequently. It is difficult to manually check the website every day to see if a product I want has become cheaper. 

**My Solution:**
I built a Python script that automates this process. It takes a product link, scrapes the current price, and saves it to a database. If the price goes below my budget, it alerts me.

## ⚙️ How it Works (Architecture)
The system is modular and has 3 main parts:
1.  **User Input (Main Module):** I enter the URL and my target price.
2.  **Scraper Module:** Uses `BeautifulSoup` to download the webpage and extract the price tag.
3.  **Database Module:** Uses `SQLite` to store the product details and a history of price changes.

## 🛠️ Tech Stack Used
* **Language:** Python 3
* **Libraries:** `requests`, `bs4` (BeautifulSoup)
* **Database:** SQLite (built-in)

## 🚀 How to Run
1.  Install the requirements:
    ```
    pip install -r requirements.txt
    ```
2.  Run the main file:
    ```
    python main.py
    ```
