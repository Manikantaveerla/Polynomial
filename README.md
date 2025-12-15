#  Polynomial Constant Finder

This repository contains a solution for the "Catalog Placements Assignment". It implements a simplified version of **Shamir's Secret Sharing** algorithm to determine the constant term ($c$) of a polynomial given a set of roots provided in a JSON format.

## 📋 Project Description

The goal of this program is to find the secret constant term ($c$) of a polynomial of degree $m$. 
The input is provided in a JSON file containing $n$ roots in the format $(x, y)$.

**Key Challenges Solved:**
* **Base Decoding:** The $y$ values are encoded in different number bases (e.g., Base 10, Base 16, Base 2) and are decoded dynamically.
* **Large Number Handling:** The coordinates involved are massive (exceeding standard 64-bit integer limits), so the solution utilizes JavaScript's `BigInt` for high-precision arithmetic.
* **Lagrange Interpolation:** The constant term is calculated using the Lagrange interpolation formula to reconstruct the polynomial at $x=0$.

## 🛠️ Technology Stack

* **Language:** JavaScript (Node.js)
* **Libraries:** Native `fs` module (no external dependencies required)

## 📂 File Structure

* `solution.js`: The main script that reads the input, processes the roots, and calculates the secret.
* `input.json`: The data file containing the encoded roots (test cases).
* `README.md`: Project documentation.

## 🚀 How to Run

### Prerequisites
Ensure you have **Node.js** installed on your machine. You can verify this by running:
```bash
node -v 
