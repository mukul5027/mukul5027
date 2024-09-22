import streamlit as st
import pandas as pd

table = pd.DataFrame({"Column 1": [1,2,3,4,5,6,7], "Column 2": [11,12,13,14,15,16,17]})

st.title("ChatWithStranger")
 
st.title("Welcome to ChatWithStranger")

st.markdown("ChatWithStranger\\ helps you connect and share with the people in your life.")

st.success("Success")
st.info("Information")
st.warning("Warning")
st.error("Error")
exp = ZeroDivisionError("Trying to divide by Zero")
st.exception(exp)

st.write("Text with write")
st.write(range(10))
st.table(table)
st.dataframe(table)
st.image("https://cdn.pixabay.com/photo/2016/11/30/18/14/chat-1873536_640.png",caption="#ChatWithStranger",width=420)

def change():
    print(st.session_state.checker)
state=st.checkbox("Checkbox",value=True, on_change=change,key="checker")
radio_btn=st.radio("In which country do you live?",options=("US","UK","Canada"))
print(radio_btn)
def btn_click():
    print("Button Clicked")
btn=st.button("login",on_click=btn_click)
select = st.selectbox("What is your favourite car?",options=("Audi","BMW","TATA"))
print(select)
