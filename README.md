# Time Series Analysis for Human Activity Recognition

## Project Overview
This project focuses on performing time series analysis to extract meaningful features from accelerometer data for various human activities. The data was collected from 15 subjects performing activities such as walking, running, climbing up, and climbing down. The goal is to analyze and identify patterns to forecast fall events, particularly in elderly individuals.

### Key Objectives:
- Analyze time-series accelerometer data across multiple body parts.
- Extract features using Natural Visibility Graphs (NVG) and Horizontal Visibility Graphs (HVG).
- Visualize network topology metrics such as average degree, network diameter, and average path length.
- Compute Permutation Entropy and Complexity for detailed time-series characterization.

---

## Dataset
The dataset consists of accelerometer readings collected from 15 subjects. Each subject performed four distinct activities:
1. **Walking**
2. **Running**
3. **Climbing Up**
4. **Climbing Down**

For each activity, data was collected from accelerometers placed on different body parts:
- **Chest**
- **Forearm**
- **Head**
- **Shin**
- **Thigh**
- **Upper Arm**
- **Waist**

### Data Characteristics:
- **File Format**: CSV
- **File Naming Convention**: `acc_<activity>_<body_part>.csv` (e.g., `acc_climbingdown_chest.csv`)
- **Columns**:
  - **Time**: Timestamp of the data point.
  - **ID**: Unique identifier for the data sample.
  - **X, Y, Z**: Accelerometer readings along the three axes (oscillation of movement).

---

## Methodology
### Feature Extraction
1. **Visibility Graphs**:
   - **Natural Visibility Graph (NVG)** and **Horizontal Visibility Graph (HVG)** are used to convert time-series data into graph structures.
   - Extracted metrics include:
     - **Average Degree**: Measure of node connectivity.
     - **Network Diameter**: Longest shortest path in the graph.
     - **Average Path Length**: Average number of steps between nodes.

2. **Permutation Entropy and Complexity**:
   - These measures provide insights into the randomness and structural complexity of the time series.
   - Parameters explored include embedding dimension, delay, and signal length.

### Visualization
Scatter plots were generated to explore relationships between features such as Permutation Entropy, Complexity, Average Degree, and Network Diameter across activities and body parts.

---

## Tools and Technologies
- **Python Libraries**:
  - `ts2vg`: For generating NVG and HVG.
  - `igraph`: For network analysis.
  - `ordpy`: For calculating Permutation Entropy and Complexity.
  - `seaborn`: For data visualization.
  - `pandas`: For data manipulation.
- **Google Colab**: Used for computation and visualizations.

---

## Results
- **Topological Metrics**: NVG and HVG metrics revealed distinct patterns for each activity and body part.
- **Entropy & Complexity**: Variation in Permutation Entropy and Complexity helped differentiate activities.
- **Insights**: The analysis successfully identified unique patterns that could forecast potential fall events in elderly individuals.

---

## How to Use
1. **Install Required Libraries**:
   ```bash
   pip install ts2vg igraph ordpy
   ```
2. **Run Analysis**:
   - Upload the dataset to your working directory.
   - Use the provided Python scripts to generate visualizations and metrics.
3. **Explore Results**:
   - The computed metrics and visualizations will help identify patterns and insights in the data.

---

## Future Scope
- Integrate additional features like velocity and orientation data.
- Extend analysis to real-time streaming data.
- Develop predictive models for early detection of fall events.

 

 
