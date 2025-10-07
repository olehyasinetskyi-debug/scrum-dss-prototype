# Decision Support System for Scrum Projects

[![Live Demo](https://img.shields.io/badge/demo-live-success)](https://[your-username].github.io/scrum-dss-prototype)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

## 📊 Overview

A web-based Decision Support System (DSS) for predicting sprint delay risks in Scrum projects based on statistical analysis of team velocity data.

**Features:**
- 📈 Three types of forecasts (current pace, historical, mixed)
- 📊 95% prediction interval calculation
- 🚦 Automated risk assessment (Low/Medium/High)
- 💡 Context-aware management recommendations
- 🌐 Platform-independent (runs in any modern browser)
- 📱 Responsive design for desktop and mobile

## 🚀 Live Demo

**Try it now:** [https://[your-username].github.io/scrum-dss-prototype](https://[your-username].github.io/scrum-dss-prototype)

## 📖 How to Use

1. **Input Tab**: Enter current sprint parameters (duration, current day, planned/completed Story Points)
2. **History Tab**: Add historical velocity data from previous sprints
3. **Calculate**: Click "Calculate Forecast" to generate predictions
4. **Results Tab**: View statistical analysis, three forecast types, and risk indicators
5. **Recommendations Tab**: Get actionable management guidance based on risk level

## 🧮 Model Formulas

The DSS uses the following statistical approach:

**Historical Statistics:**
V_avg = Σ V_i / n
s = √[Σ(V_i - V_avg)² / (n-1)]

**Current Performance:**
V_day = CompletedSP / CurrentDay

**Forecasts:**
ForecastSP_current = V_day × SprintLength
ForecastSP_hist = V_avg
ForecastSP_mixed = w × ForecastSP_current + (1-w) × ForecastSP_hist
where w = CurrentDay / SprintLength

**Prediction Interval (95%):**
PI = V_avg ± t(0.975, n-1) × s × √(1 + 1/n)

**Risk Classification:**
- Deviation > 10 SP → 🔴 High Risk
- 5 SP ≤ Deviation ≤ 10 SP → 🟡 Medium Risk
- 0 SP ≤ Deviation < 5 SP → 🟢 Low Risk
- Deviation < 0 → 🟢 Ahead of Schedule

## 📄 Academic Publication

This tool is part of academic research on risk management in Scrum projects.

**Authors:** Oleh Yasinetskyi, Tetiana Fesenko  
**Affiliation:** Kharkiv National University of Radio Electronics

**Citation:**

Yasinetskyi, O., Fesenko, T. (2025). Decision Support System for Predicting
Delay Risks in Scrum Projects Based on Velocity Statistical Analysis.
[Journal/Conference Name]. DOI: [to be assigned]

## 🛠️ Technical Details

- **Technology Stack**: Pure HTML5, CSS3, JavaScript (ES6+)
- **Dependencies**: None (no external libraries required)
- **Browser Support**: All modern browsers (Chrome, Firefox, Safari, Edge)
- **Responsive**: Works on desktop, tablet, and mobile devices

## 📦 Installation

### Option 1: Use Online (Recommended)
Simply visit the [live demo](https://[your-username].github.io/scrum-dss-prototype)

### Option 2: Run Locally
1. Clone this repository:
```bash
   git clone https://github.com/[your-username]/scrum-dss-prototype.git
