import streamlit as st
import pandas as pd
from PIL import Image

st.write("Hello World")
st.title("Bienvenue sur le site web de Qian")
liste_ville = ['', 'Pekin', 'San francisco', 'Paris', 'Greece', 'nan' ]
choice = st.selectbox("Indiquer votre arrondissement de récupération ?", liste_ville)
if choice == '':
    st.write('Fait vos choix ')
    st.image("C:\\Users\\leo12\\Documents\\Streamlit quest\\images\\choix.jpg", width=900)
elif choice == 'Pekin':
    st.write('Tu as choisis : ', 'Pekin')
    st.image("C:\\Users\\leo12\\Documents\\Streamlit quest\\images\\Pékin.jpg", width=900)
elif choice == 'San francisco':
    st.write('Tu as choisis : ', 'San francisco')
    st.image(r"C:\Users\leo12\Documents\Streamlit quest\images\San francisco.jpg")
elif choice == 'Paris':
    st.write('Tu as choisis : ', 'Paris')
    st.image(r"C:\Users\leo12\Documents\Streamlit quest\images\Paris.jpg", width=900)
elif choice == 'Greece':
    st.write('Tu as choisis : ', 'Greece')
    st.image(r"C:\Users\leo12\Documents\Streamlit quest\images\Greece.jpg", width=900)
else:
    st.write('Tu as choisis : ', 'nan')
    st.image(r"C:\Users\leo12\Documents\Streamlit quest\images\nan.jpg", width=900)
