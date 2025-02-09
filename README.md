# **Continuous Cuffless Blood Pressure Monitoring**

This repository contains the implementation of **Cuffless-BP**, a deep learning-based project aimed at providing continuous and non-invasive blood pressure monitoring, specifically tailored for space missions. The model leverages Photoplethysmogram (PPG) and Electrocardiogram (ECG) signals to estimate blood pressure with high accuracy, without the need for traditional cuffs.

## **Abstract**

Smart BP represents an innovative shift from conventional cuff-based blood pressure monitoring methods. Designed to meet the unique demands of astronauts on extended space missions, the project integrates advanced deep learning techniques for real-time cardiovascular health monitoring. Using non-invasive physiological signals (PPG and ECG), Smart BP offers uninterrupted blood pressure tracking, potentially enhancing early detection of cardiovascular issues.

## **Table of Contents**


1. [Project Overview](#project-overview)
2. [Methodology](#methodology)
3. [Dataset](#dataset)
4. [Models](#models)
5. [Usage](#usage)
6. [Results](#results)





## **Project Overview**

The main objective of this project is to develop a continuous, cuffless blood pressure monitoring system. It uses PPG and ECG signals to estimate arterial blood pressure (ABP), systolic blood pressure (SBP), and diastolic blood pressure (DBP). 

This project is particularly suited for space expeditions where real-time monitoring of cardiovascular health is essential due to the lack of immediate medical interventions. 

## **Methodology**

Smart BP uses deep learning techniques, specifically Bi-Directional Long Short-Term Memory (Bi-LSTM) networks with attention mechanisms, to process the physiological signals from PPG and ECG inputs. The architecture includes:

- **Bi-LSTM**: Captures temporal dependencies in both forward and backward directions.
- **Attention Layers**: Selectively focuses on relevant parts of the input data.
- **PPG and ECG Signals**: Used as input features for blood pressure estimation.

## **Dataset**

### Visualisation and Representations:

<table>
  <tr>
    <th>PPG Sample</th>
    <th>ECG Sample</th>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/df657c54-bd16-4e2d-8536-e0c7f68fded3" alt="PPG Sample" width="900"></td>
    <td><img src="https://github.com/user-attachments/assets/55d1d371-4183-46d7-bf5a-6e827ed0d357" alt="ECG Sample" width="900"></td>
  </tr>
  <tr>
    <th colspan="2">Distribution of ABP, SBP, and DBP</th>
  </tr>
  <tr>
    <td colspan="2" style="text-align:center;"><img src="https://github.com/user-attachments/assets/3be4fbff-e2d9-4fe3-9f03-978fd3d00d7e" alt="ABP SBP DBP Distribution" width="1000"></td>
  </tr>
</table>




## **Models**

Three models were explored in this project:
1. **Bi-LSTM with Attention Mechanisms**: Achieved the best results with an MAE of 7.2 mmHg for SBP and 2.7 mmHg for DBP.
2. **Repetitive Bi-LSTM with Additional Dense Layers**: A deeper architecture that provided slightly higher computational costs.
3. **Bi-LSTM Without Dense Layers**: A more streamlined version that focused on reducing complexity while maintaining accuracy.

## **Usage**

You can run the notebook `work.ipynb` to train and evaluate the model. Ensure the necessary datasets (PPG and ECG) are provided.

```bash
jupyter notebook work.ipynb
```

Make sure to configure the paths for datasets as needed.

## **Results**

The model was trained on data from the MIMIC III database, achieving impressive results in estimating SBP, DBP, and ABP. The model demonstrates real-time performance potential, crucial for continuous monitoring, especially in space missions.

- **Best Results**:  
  - SBP MAE: **7.2 mmHg**  
  - DBP MAE: **2.7 mmHg**

 



