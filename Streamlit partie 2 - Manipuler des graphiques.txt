import streamlit as st
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.express as px
import pandas as pd

# read dataset of flight :
flight_data = pd.read_csv("https://raw.githubusercontent.com/mwaskom/seaborn-data/master/flights.csv")
datasets = ['Flight', '']

# title
st.title('Manipulation de données et création de graphiques')

# afficher le dataframe in the streamlit
choice = st.selectbox('Quel dataset veux-tu', datasets)
if choice == 'Flight':
    st.table(flight_data.head(10))

# afficher the graphiques en fonction du temps et nbr de passagers
flitre_flight = ['year', 'month', 'passengers']
x = st.selectbox('Choisissez la colonne X', flitre_flight)
y = st.selectbox('Choisissez la colonne y', flitre_flight)

# choix de graphiques 
graph = ['scatter_chart', 'line_chart', 'bar_chart']
graphiques = st.selectbox('Quel graphique veux-tu utiliser ?', graph)
plt.figure(figsize=(10, 6))
if graphiques == 'scatter_chart':
    sns.scatterplot(data=flight_data, x=x, y=y)
    st.pyplot(plt.gcf())
elif graphiques == 'line_chart':
    sns.lineplot(data=flight_data, x=x, y=y)
    st.pyplot(plt.gcf())
elif graphiques == 'bar_chart':
    sns.barplot(data=flight_data, x=x, y=y)
    st.pyplot(plt.gcf())

# afficher le checkbox :
check = st.checkbox('Afficher la matrice de corrélation')
st.subheader('Ma matrice de corrélation')
if check:
    correlation_matrix = flight_data[['year', 'passengers']].corr()
    sns.heatmap(correlation_matrix, annot=True)
    st.pyplot(plt.gcf())
