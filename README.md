# 🌲 Fuzzy Logic Modeling for Forest Fire Risk Assessment

Welcome to the **Forest Fire Risk Assessment** repository. This project is based on my M.Sc. thesis in Mathematics at Süleyman Demirel University (2022). It presents a deterministic decision-support mechanism that utilizes a **Mamdani Fuzzy Inference System (FIS)** to predict forest fire risk levels and optimally allocate firefighting resources based on real-world meteorological and topographical data.

---

## 📌 1. The Forest Fire Problem & The Need for Fuzzy Logic
Forest fires are devastating natural disasters that cause irreversible damage to ecosystems, wildlife, and human settlements. As global warming intensifies, fire seasons are becoming longer and more destructive. 

The rapid spread of a wildfire is heavily dependent on complex, non-linear environmental factors. Classical (crisp) logic (0 or 1) often fails to model the uncertain and chaotic nature of climate events. For instance, classifying a 30°C day strictly as "hot" and a 29°C day strictly as "warm" creates artificial boundaries that do not reflect reality. **Fuzzy Logic** allows us to mimic human reasoning, processing vague and continuous environmental variables to make rapid, intelligent decisions during an emergency.

---

## 🧠 2. Fuzzy Inference System (FIS) Architecture
To create a robust prediction model, we developed a Mamdani-type Fuzzy Inference System. The model was trained and tested using 66 historical forest fire records (Jan 2019 - Jan 2020) collected from the Isparta Regional Directorate of Forestry in Turkey.

The architecture consists of **5 Input Variables** and **2 Output Variables**:

### 📥 Inputs (Environmental & Topographical Factors)
1. **Temperature (°C):** Modeled with 3 membership functions (Low, Medium, High).
2. **Humidity (%):** Modeled with 3 membership functions (Low, Medium, High).
3. **Wind Speed (km/h):** A critical factor for fire spread, modeled with 3 membership functions.
4. **Altitude (m):** Fires are generally more frequent at lower altitudes (e.g., < 400m).
5. **Slope (%):** Fire travels exponentially faster uphill.

### 📤 Outputs (Decision Support)
1. **Fire Risk Level:** Computes the danger severity of the ongoing fire.
2. **Number of Vehicles (Fleet Size):** Determines the exact number of firefighting vehicles (e.g., 1-3 vehicles, 4-11 vehicles, or 12+ vehicles) required to suppress the fire efficiently without over-allocating resources.

*(The model utilizes a total of **243 IF-THEN rules** ($3^5$) combining Triangular and Trapezoidal membership functions to evaluate the chaotic environmental conditions).*

---
