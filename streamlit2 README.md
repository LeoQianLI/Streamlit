# Streamlit App: Manipulation de Données et Création de Graphiques

This project demonstrates data manipulation and visualization using **Streamlit**, **Seaborn**, and **Matplotlib**. 
The app allows users to explore a dataset of flight statistics and create various types of visualizations interactively.

---

## Features
- **Data Display**: View the first 10 rows of the flight dataset.
- **Graph Customization**:
  - Choose the x and y axes for visualizations.
  - Select the type of graph: scatter plot, line chart, or bar chart.
- **Correlation Matrix**: Visualize the correlation matrix between selected columns.

---

## Dataset
The dataset is sourced from the Seaborn library:
- URL: [flights.csv](https://raw.githubusercontent.com/mwaskom/seaborn-data/master/flights.csv)
- Columns:
  - `year`: The year of the record.
  - `month`: The month of the record.
  - `passengers`: The number of passengers.


### Technologies Used
Streamlit: Interactive web app framework.
Pandas: Data manipulation.
Seaborn: Visualization library.
Matplotlib: Additional visualization support.

### Future Improvements
Add support for multiple datasets.
Allow users to upload their own datasets.
Add more visualization types (e.g., histograms, box plots).