import streamlit as st

import streamlit as stm 


stm.set_page_config(page_title="Login Page") 
 
st.title("Welcome to ChatWithStranger login page")

st.markdown("ChatWithStranger helps you connect and share with the people in your life.")
st.image("https://cdn.pixabay.com/photo/2016/11/30/18/14/chat-1873536_640.png",caption="#ChatWithStranger",width=100)
name = st.text_input("Enter username")
password = st.text_input("Enter Password",type="password")

def change():
    print(st.session_state.checker)
state=st.checkbox("T&C",value=True, on_change=change,key="checker")
if(st.button('Login',use_container_width=40)):
    result = name.title()
    st.success(result)
