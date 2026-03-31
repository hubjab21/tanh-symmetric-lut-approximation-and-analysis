# tanh-symmetric-lut-approximation-and-analysis

## 📌 Overview

This project presents a **Look-Up Table (LUT)-based piecewise quadratic approximation** of the hyperbolic tangent function `tanh(x)`.

The implementation improves efficiency by exploiting the **odd symmetry** of the function:

[
tanh(-x) = -tanh(x)
]

Instead of computing the full range, the approximation is calculated only for the positive domain and mirrored for negative values.

---

## 🎯 Objectives

* Implement a **quadratic LUT-based approximation** of `tanh(x)`
* Compare **symmetric vs non-symmetric approaches**
* Analyze:

  * approximation accuracy (max error)
  * computation time
* Investigate the impact of:

  * number of LUT points
  * input range

---

## ⚙️ Methodology

### 1. LUT Generation

The input range is divided into segments. For each segment:

* ( Y_k ) – function value at the beginning
* ( B_k ) – linear slope
* ( A_k ) – quadratic correction (based on midpoint)

### 2. Quadratic Approximation

Each segment is approximated using:
[
y \approx Y_k + B_k x + A_k x (\Delta - x)
]

### 3. Symmetry Optimization

Only values for ( x \geq 0 ) are computed:
[
tanh(-x) = -tanh(x)
]

---

## 📊 Results

The project compares:

* **Maximum approximation error**
* **Computation time**

Key observations:

* Symmetric approach significantly reduces computation time
* Accuracy improves with more LUT points
* Larger input ranges increase approximation error

---

## 🚀 Technologies

* Python 3
* NumPy
* Matplotlib

---

## ▶️ Installation

Install required libraries:

```bash
pip install numpy matplotlib
```

> Note: `time` is part of the Python standard library and does not require installation.

---

## ▶️ How to Run

### Option 1 – Jupyter Notebook

```bash
jupyter notebook
```

Open:
`tanh-symmetric-lut-approximation-and-analysis.ipynb`

### Option 2 – HTML Version

Open the file directly in your browser:
`tanh-symmetric-lut-approximation-and-analysis.html`

---

## 📂 Project Structure

```
.
├── README.md
├── tanh-symmetric-lut-approximation-and-analysis.html
└── tanh-symmetric-lut-approximation-and-analysis.ipynb
```

---

## 📈 Visualizations

The project generates plots showing:

* Exact vs approximated `tanh(x)`
* LUT points
* Approximation error
* Performance comparison (error & time)

---

## 📌 Key Takeaways

* Using symmetry significantly reduces computation cost
* LUT-based approximation is efficient and scalable
* There is a trade-off between accuracy and LUT size

---

# 👤 Author

Hubert Jabłoński
