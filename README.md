# 🛒 E-Commerce Price Tracker

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Database](https://img.shields.io/badge/SQLite-LightBlue?style=for-the-badge&logo=sqlite&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

> **A robust, automated Python tool designed to track product prices across e-commerce platforms and trigger email notifications when prices drop.**

---

## 📑 Table of Contents
1. [Project Overview](#-project-overview)
2. [System Architecture](#-system-architecture)
3. [Key Features](#-key-features)
4. [Folder Structure](#-folder-structure)
5. [Installation & Usage](#-installation--usage)
6. [Future Scope](#-future-roadmap)

---

## 📖 Project Overview
This project addresses the problem of manual price monitoring. By leveraging web scraping and task scheduling, it allows users to track products on Amazon/eBay without human intervention. It fulfills the academic requirement of **Data Input** (Scraping), **Processing** (Logic), and **Reporting** (Alerts).

**Target Audience:** Smart shoppers and data enthusiasts who want to save money.

---

## 🏗 System Architecture
The system follows a modular data flow. When uploaded to GitHub, the diagram below represents the logic:

```mermaid
graph LR
    A[User Input: URL] --> B(Scheduler)
    B --> C{Scraper Engine}
    C -->|Request| D[E-Commerce Site]
    D -->|HTML Data| C
    C -->|Clean Data| E[(SQLite Database)]
    E --> F{Price Analyzer}
    F -->|Price Drop!| G[Email Notification]
    F -->|No Change| H[Log Data]
