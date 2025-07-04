
#  Dynamic Pricing for Urban Parking Lots  
**Capstone Project | Summer Analytics 2025**  
*Hosted by Consulting & Analytics Club × Pathway*

##  Overview  
Urban parking is a scarce resource with demand that fluctuates throughout the day. Traditional static pricing models often result in either overutilization or inefficient empty spaces. This project solves that by designing a real-time **dynamic pricing system** that intelligently adjusts parking prices based on demand, queue length, traffic, special events, vehicle type, and nearby competition.

I developed a **streaming-based ML pipeline** using only `numpy`, `pandas`, and `Pathway`, as per the constraints. The final system makes real-time pricing decisions and simulates intelligent rerouting, ensuring optimal resource usage and improved customer experience.

---

## ⚙️ Tech Stack  

| Category             | Tools Used                     |
|----------------------|--------------------------------|
| Programming Language | Python 3.11                    |
| Libraries            | Pandas, NumPy, Pathway, Bokeh  |
| Platform             | Google Colab                   |
| Visualization        | Bokeh                          |
| Version Control      | Git & GitHub                   |
| Diagram              | Image-based Architecture Below |

---

## 🧠 Architecture Diagram  
![bokeh_plot](https://github.com/user-attachments/assets/fed79854-b7d3-4e19-867d-ace0e3a0fe56)

---

##  Project Workflow  

### 1.  Data Ingestion  
- Ingested streamed data from 14 parking lots over 73 days.
- Used Pathway to handle real-time updates.
- Enabled local file upload for dataset (`dataset.csv`).

### 2.  Preprocessing & Feature Engineering  
- Parsed timestamp from date and time columns.
- Mapped categorical fields:
  - Traffic: low/medium/high → numeric
  - Vehicle type: bike/car/truck → weighted scores
- Calculated spatial proximity using haversine distance for competitive pricing logic.

### 3.  Pricing Models  
- **Model 1: Baseline Linear**  
  - Price increases linearly with occupancy.  
- **Model 2: Demand-Based Function**  
  - Takes into account occupancy, queue length, traffic, event days, and vehicle type.
  - Normalized demand controls price changes smoothly.
- **Model 3: Competitive Pricing**  
  - Analyzes nearby lots using GPS coordinates.
  - Adjusts prices based on competition and suggests rerouting if needed.

### 4.  Visualization  
- Real-time pricing plotted using **Bokeh**.
- Created interactive line charts for each parking lot.

### 5.  Final Output  
- Fully functional Colab notebook with modular and error-free code.
- Clean, stepwise implementation:
  - Install packages
  - Upload dataset
  - Process data
  - Define pricing models
  - Run real-time simulation
  - Show live visualizations

---

##  Assumptions  
- Base price = $10 per lot.
- Price range bounded between $5 and $20.
- Competitor influence limited to 3 nearest lots.
- Demand is normalized and affects price gradually.

---

## 📁 Repository Structure  

```

📦 DynamicParkingPricing/
├── 📄 README.md
├── 📊 Dynamic\_Pricing\_Colab.ipynb
├── 📁 assets/
│   └── architecture.png  (optional static version)
├── 📄 dataset.csv         (upload only for demo, remove from final repo)
└── 📄 report.pdf          (optional, if created)

```

---

##  How to Run  

1. Clone the repository or open notebook in Google Colab  
2. Upload the dataset file (`dataset.csv`)  
3. Run the notebook sequentially to simulate real-time dynamic pricing and visualizations  

---

##  Access and Notes  

- This repository is **public**  
- All scripts are self-contained and require no API keys  
- Uses Pathway's real-time streaming simulation in Colab  
- Designed to comply with the rules of Summer Analytics 2025

---

##  Author  

> This project was built as part of **Summer Analytics 2025** organized by the **Consulting & Analytics Club, IITG** and **Pathway**.  
>  
> **Submitted by:** *Shivangi Suyash*  
> **Email:** shivangisuyash8@gmail.com  
```
