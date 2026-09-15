# Smart Medical Scheduling System — Final Project

An intelligent scheduling optimization system for medical 
appointments using multiple algorithms and AI assistance.

**Course:** Industry Project | Tel Aviv University — Digital Sciences for Hi-Tech  
**Built by:** Kamelia Atwan (group project)

---

## What this project does

Given doctors' availability and patients' medical data, 
the system creates optimized appointment schedules while 
balancing medical urgency, patient preferences, and 
resource efficiency.

---

## System Architecture

**Algorithm 1 — Greedy**
Fast initial solution by sorting patients by medical 
priority and assigning the first available slot.

**Algorithm 2 — Simulated Annealing**
Improves the initial solution by exploring local changes 
and avoiding local optima.

**Algorithm 3 — Hybrid (Best performer ⭐)**
Combines Greedy + Simulated Annealing for optimal results.

**AI Layer — Gemini API**
Identifies problematic tasks and suggests targeted fixes. 
Fixes are accepted only if they improve the overall score.

---

## Objective Function

Score = 100×Scheduled + 20×Priority² + 20×InWindow 
        − 10×OutWindow − 50×DaysLate×Priority

- Scheduled: +100 per assigned patient
- Priority²: rewards urgent cases
- InWindow: +20 for preferred time slot
- OutWindow: −10 for out-of-preference slot
- DaysLate×Priority: penalty for late treatment

---

## Features

- Interactive Dashboard built with Streamlit
- Compare algorithms side-by-side
- AI-powered schedule improvement via Gemini API
- Web app for managing doctors, patients, and tasks
- CSV-based data input for flexibility

---

## Technologies

Python · Streamlit · Gemini API · pandas · 
NumPy · Matplotlib · CSV

---

## How to run

pip install streamlit pandas numpy matplotlib google-generativeai
streamlit run app.py
