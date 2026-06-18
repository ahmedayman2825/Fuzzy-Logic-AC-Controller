<div align="center">

<h1>🌡️ FuzzyClimate</h1>
<h3>Fuzzy Logic Air Conditioning Controller</h3>

<p>
  A fuzzy inference system that intelligently controls AC temperature and fan speed based on real-world sensor data — no rigid thresholds, just smart decisions.
</p>

<p>
  <img src="https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white" />
  <img src="https://img.shields.io/badge/scikit--fuzzy-0.4.2-4B8BBE?style=for-the-badge" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" />
</p>

<p>
  <a href="#-overview">Overview</a> •
  <a href="#-features">Features</a> •
  <a href="#-tech-stack">Tech Stack</a> •
  <a href="#-installation">Installation</a> •
  <a href="#-usage">Usage</a> •
  <a href="#-project-structure">Structure</a> •
  <a href="#-future-improvements">Roadmap</a> •
  <a href="#-contributors">Contributors</a>
</p>

</div>

---

## 📌 Overview

**FuzzyClimate** is a fuzzy logic-based controller that simulates intelligent AC management by processing real sensor readings — temperature, humidity, and occupancy — and producing smooth, human-like control decisions for compressor power and fan speed.

Unlike traditional rule-based thermostats that operate on binary on/off logic, FuzzyClimate uses **Mamdani fuzzy inference** to reason over linguistic variables (e.g., *"it's warm and fairly humid"*) and output graduated responses — the same way a person would intuitively adjust the AC.

The system was trained and validated against **5,400 rows of 3-hour interval sensor data**, with all results exported for analysis.

---

## ✨ Features

- **Fuzzy Inference Engine** — Mamdani-type FIS with fully defined input/output membership functions
- **Multi-input reasoning** — Takes temperature, humidity, and occupancy as simultaneous inputs
- **Smooth output control** — Produces continuous compressor power (%) and fan speed (%) rather than binary states
- **Real sensor data** — Validated on 5,400 real-world readings sampled at 3-hour intervals
- **Full result export** — All controller decisions saved to `fuzzy_ac_results.csv` for downstream analysis
- **Visualizations** — Membership function plots, rule activation traces, and control surface rendered inline in the notebook

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Language | Python 3.8+ |
| Fuzzy Logic Engine | `scikit-fuzzy` |
| Numerical Computing | `NumPy` |
| Data Handling | `pandas` |
| Visualization | `matplotlib` |
| Environment | Jupyter Notebook |

---

## ⚙️ Installation

**1. Clone the repository**

```bash
git clone https://github.com/ahmedayman2825/Fuzzy-Logic-AC-Controller.git
cd Fuzzy-Logic-AC-Controller
```

**2. Create a virtual environment (recommended)**

```bash
python -m venv venv
source venv/bin/activate        # Linux / macOS
venv\Scripts\activate           # Windows
```

**3. Install dependencies**

```bash
pip install scikit-fuzzy numpy pandas matplotlib notebook
```

---

## 🚀 Usage

Launch the notebook:

```bash
jupyter notebook project.ipynb
```

Then run all cells top to bottom. The notebook will:

1. Load `data_3hrs.csv` (sensor readings)
2. Define fuzzy sets and membership functions for each input/output variable
3. Build and apply the rule base
4. Run inference across all 5,400 data points
5. Export decisions to `fuzzy_ac_results.csv`
6. Render membership function plots and the 3D control surface

**Input variables:**

| Variable | Range | Linguistic Terms |
|---|---|---|
| Temperature | 0 – 50 °C | Cold, Comfortable, Warm, Hot |
| Humidity | 0 – 100 % | Low, Medium, High |
| Occupancy | 0 – 10 people | Empty, Few, Moderate, Full |

**Output variables:**

| Variable | Range | Linguistic Terms |
|---|---|---|
| Compressor Power | 0 – 100 % | Off, Low, Medium, High, Max |
| Fan Speed | 0 – 100 % | Off, Slow, Medium, Fast |

---

## 📁 Project Structure

```
Fuzzy-Logic-AC-Controller/
│
├── project.ipynb            # Main notebook — FIS definition, inference, results & plots
├── data_3hrs.csv            # Input dataset — 5,400 rows of sensor readings (3-hr intervals)
├── fuzzy_ac_results.csv     # Output dataset — controller decisions for each reading
├── .gitignore
└── README.md
```

---

## 🔭 Future Improvements

- [ ] Add a Streamlit dashboard for real-time interactive control simulation
- [ ] Expand rule base with time-of-day and outdoor temperature as additional inputs
- [ ] Benchmark FIS against a PID controller on the same dataset
- [ ] Implement Sugeno-type inference and compare output smoothness
- [ ] Package the FIS as a reusable Python module with a clean API
- [ ] Add unit tests for membership function coverage and rule completeness

---

## 👤 Contributors

 **Ahmed Ayman**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/eng-ahmed-ayman/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/ahmedayman2825)

---

<div align="center">
  <sub>Built with ❤️ by Ahmed Ayman · Alexandria University, Computer Science — AI Track</sub>
</div>
