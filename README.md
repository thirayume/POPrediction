## **Muangtai-online > Predictive Purchasing**

การพยากรณ์ยอดจัดซื้อด้วย Seasonal ARIMA

### ขั้นตอนการดำเนินงาน

1.  #### **Data Cleansing**
    

*   [ ] Prepare data จาก database (direct connection and query / export to csv)
*   [ ] Data cleaning process (ยังพบข้อมูลที่ null / NaN อยู่)

2.  #### **Data preprocess by scaling, reshaping**
    

*   [ ] ออกแบบ dataset, structure (=vector, tree, etc.) แล้วทำการ Transform data เช่น units เป็นต้น
*   [x] เลือก "Simple Model" / Linear Regression / Polynomial Regression / หรืออื่นๆ ตามสมควร?

3.  #### **Transform**
    

*   ทำ Features Selection, โดย assume ว่า data ต้นน้ำสวย
*   เลือก feature หลัก (direct features: endogenous)
*   เลือก feature รอง (hidden feature: exogenous)
*   หา Insight, Relationship

4.  #### **เลือก Model**
    

*   [x] Data preprocess by stationarity analysis, PACF, ACF
*   [x] เลือก ARIMA? / SARIMA? / SARIMAX? มาใช้ hypothesis: Seasonal
*   [x] Finding an Optimal Model with Auto-ARIMA เผื่อ PQ-d ตัวไหนที่หลุดไป, เลือกตัวที่ดีกว่ามาใช้
*   [x] 2+ approach
*   [x] Decide on model approach and KPI
    *   [x] 2+ approach เพื่อกลับมา discuss กันว่าจะใช้ตัวไหนดี?

---

ในกระบวนการ **“เลือก Model”** อาจมีการทำซ้ำหลายครั้ง เพื่อหา Simple Model ที่ดีที่สุดอย่างน้อย 2+ approch models เพื่อนำไป Optimize ต่อ

> ผลการคัดเลือกปัจจุบันจาก Modeling by
> 
> 1.  Month
> 2.  **Date**
> 
> ได้เลือก Model V.2 - Date มาดำเนินการในขั้นตอนต่อไป

---

5.  #### **ARIMA/SARIMA/SARIMAX modeling**
    

*   [ ] Optimal Model with AIC / GridSearch / Etc
*   [ ] Decide on model approach and KPI
*   [ ] Fitting Model / Finetune Model
*   [ ] Model Estimation and Diagnostics

6.  #### **Optimisation & Error minimisation**
    

*   [ ] ARIMA/SARIMA/SARIMAX Prediction
*   [ ] ARIMA/SARIMA/SARIMAX Forecast
*   [ ] Model Estimation and Diagnostics

7.  #### **Testing**
    

*   [ ] Adding Exogenous and Endogenous features

---

### **SoW**

### **Business Analysis**

*   [ ] กำหนด ARIMA Model
*   [ ] Re-Train Model ให้ Accuracy มากกว่า ± xx.xx% (TBC)
*   [ ] สร้าง Bayesian Inference Deep Network Graph
*   [ ] แก้ไข Bayesian Network ให้ตรงกับ Relationship Questioning จาก Experts
*   [ ] พัฒนา Application Programming Interface ให้ External Application เรียกใช้