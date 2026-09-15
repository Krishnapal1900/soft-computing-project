# soft-computing-project
Traffic Light Controller
# 🚦 Smart Traffic Light Controller

An intelligent traffic signal controller developed using **Fuzzy Logic** and **Python**. The system dynamically determines the optimal green, yellow, and red signal durations based on traffic conditions, waiting time, weather, vehicle count, lane density, and priority situations.

## 🎯 Project Objective

The objective of this project is to design a smart traffic signal system that can dynamically adjust signal timing instead of relying on fixed traffic-light durations.

The controller uses a **Fuzzy Logic Control System** to make decisions under uncertain and continuously changing traffic conditions.

## 🧠 Technologies Used

* Python
* NumPy
* Matplotlib
* Scikit-Fuzzy
* Gradio
* Google Colab

## ⚙️ Input Parameters

The system considers several factors:

### Traffic Conditions

* Traffic density
* Waiting time
* North lane traffic
* South lane traffic
* East lane traffic
* West lane traffic

### Vehicle Types

* Cars
* Buses
* Trucks
* Bikes

Different vehicle types are assigned different weights to estimate the overall traffic load.

### Environmental Conditions

* Clear weather
* Normal weather
* Bad weather

### Additional Conditions

* Emergency vehicle
* VIP/police priority
* Pedestrian crossing
* Accident detection
* Time of day

## 🔬 Fuzzy Logic

The system uses fuzzy membership functions for:

* Traffic Density

  * Low
  * Medium
  * High

* Waiting Time

  * Short
  * Medium
  * Long

* Weather

  * Clear
  * Normal
  * Bad

The output variable is:

* Green Signal Time

  * Short
  * Medium
  * Long

The fuzzy rules determine the appropriate green signal duration based on the current traffic conditions.

## 🚑 Priority Handling

The system also contains priority overrides.

### Emergency Vehicle

When an emergency vehicle is detected, the controller immediately activates a long green signal.

### VIP / Police Override

A priority green signal is activated when VIP/police override is enabled.

## 🚶 Pedestrian Handling

When a pedestrian crossing request is detected, the green signal duration is reduced while maintaining a minimum green time.

## 🚧 Accident Handling

When an accident is detected, additional green time is provided to help manage the affected traffic condition.

## 📊 Output

The system displays:

* Green signal duration
* Yellow signal duration
* Red signal duration
* Adjusted traffic density
* Current operating conditions
* Traffic signal timing graph

## 🖥️ User Interface

The project uses **Gradio** to provide an interactive web interface.

The interface contains separate sections for:

1. Main Control
2. Priority Inputs
3. Vehicle Count
4. Lane Camera Count

## ▶️ How to Run

Install the required libraries:

```bash
pip install -r requirements.txt
```

Then open the Jupyter Notebook:

```text
smart_traffic_controller.ipynb
```

Run all cells and launch the Gradio application.

## ☁️ Google Colab

The project was developed and tested using Google Colab.

## 🚀 Future Improvements

Possible future improvements include:

* Real-time vehicle detection using computer vision
* Integration with CCTV cameras
* YOLO-based vehicle detection
* Real-time traffic data
* Multiple-intersection coordination
* Reinforcement learning for adaptive signal control
* Emergency vehicle detection using computer vision
* Cloud deployment

## 👨‍💻 Author

**Krishna Pal**

---

⭐ If you find this project useful, consider giving the repository a star!
