# Lung-Mechanics-Simulation-using-Lumped-Parameter-Model-Simulink-
Comparing Normal, Asthma and Emphysema Respiratory Responses



##  **1. Introduction**

This project implements a **Lumped-Parameter Respiratory Mechanics Model** in **MATLAB Simulink**.
The model describes:

* Pressures in the airway, lungs, pleural space
* Airflow driven by diaphragm pressure
* Effects of airway resistance and lung/chest-wall compliance
* Comparison of **normal, asthma, and emphysema conditions**

This simulation helps understand how **mechanical properties of lungs** affect breathing.

---

##  **2. Theory**

The respiratory system is modeled using:

* **Resistances**

  * Rc → Central airway resistance
  * Rp → Peripheral airway resistance

* **Compliances**

  * Cₗ → Lung compliance
  * Cw → Chest-wall compliance
  * Cs → Shunt compliance

A sinusoidal diaphragm pressure input generates air movement.

The lumped model considers pressures:

* Paw → Airway pressure
* PA → Alveolar pressure
* Ppi → Pleural pressure
* P₀ → Atmospheric (reference)

---

##  **3. Simulink Model Overview**

The Simulink model consists of:

* Sinusoidal **diaphragm pressure source**
* Transfer function blocks for resistances & compliances
* Summing junctions to compute lung/airway pressures
* Scopes to visualize pressure and airflow waveforms

###  Model Used

*(Based on your screenshot — simplified description here)*

```
Pdiaphragm → [Resistances & Compliances] → Paw, PA, Flow → Scope
```

---

## 📌 **4. Parameters Used**

### **Normal Condition**

| Parameter | Value |
| --------- | ----- |
| Rc        | 1     |
| Rp        | 0.5   |
| Cₗ        | 0.2   |
| Cw        | 0.2   |
| Cs        | 0.005 |

### **Asthma (Increased airway resistance)**

| Parameter | Change        |
| --------- | ------------- |
| Rc        | 2–4× increase |
| Rp        | 3–6× increase |

### **Emphysema (High compliance)**

| Parameter | Change                  |
| --------- | ----------------------- |
| Cₗ        | ↑ (0.5 – 1.0)           |
| Cw        | Slight ↑                |
| Rc / Rp   | Slight ↑ (air trapping) |

---

##  **5. How to Run the Simulation**

1. Open MATLAB
2. Load the `.slx` model file
3. Set parameters in the workspace / block masks
4. Click **Run** (▶)

---

##  **6. How to View Simulation Results**

Your model already includes **Scope blocks**.

To view output:

1. Double-click **Scope**
2. Run the model
3. Observe waveforms:

   * Lung pressure
   * Airway pressure
   * Flow
   * Chest-wall pressure

If needed, you can also log data using:

```
To Workspace → plot() in MATLAB
```

---

##  **7. Expected Output Waveforms**

The output consists of **sinusoidal-like waveforms** representing:

* Airflow
* Airway pressure (Paw)
* Alveolar pressure (PA)
* Pleural pressure (Ppi)

Normal lungs show:

* Smooth sinusoidal patterns
* Small phase differences

Asthma:

* Higher airway pressure amplitude
* Distorted airflow waveform (due to obstruction)

Emphysema:

* Larger compliance → Lower pressure swings
* Flow waveform becomes flattened
* Phase lag increases

*(Your attached scope waveform matches the expected sinusoidal outputs.)*

---

##  **8. Observations (Based on Simulation)**

### **Normal Lungs**

* Balanced pressure-volume relationship
* Smooth airflow cycles

### **Asthmatic Lungs**

* Increased Rc and Rp →

  * Reduced airflow
  * Higher airway pressure
  * Narrower waveform peaks

### **Emphysema**

* Increased lung compliance →

  * Decreased pressure swing
  * Large, delayed waveforms
  * Air trapping effect

---

##  **9. Conclusion**

The lumped-parameter Simulink model successfully simulates how **changes in compliance and resistance** affect breathing mechanics.
The results clearly differentiate:

* **Normal breathing**
* **Asthmatic restricted airflow**
* **Emphysematous high compliance**

This model is useful for biomedical engineering, respiratory mechanics studies, and clinical physiology understanding.

---

##  **10. Repository Structure**

```
├── Lung_Model.slx      # Simulink model
├── README.md           # Documentation
└── plots/              # Saved scope screenshots (optional)
```

---



