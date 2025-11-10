import streamlit as st
from PIL import Image

st.title("HelloFresh Add-On Demo")
st.write("Upload a photo of your ingredients or meal to get add-on suggestions!")

# Upload image
uploaded_file = st.file_uploader("Choose an image...", type=["jpg", "jpeg", "png"])

if uploaded_file is not None:
    image = Image.open(uploaded_file)
    st.image(image, caption='Uploaded Image', use_column_width=True)
    
    # Mock detection of items
    st.write("### Detected Items in Image (simulated):")
    # For demo purposes, we pretend to detect some items
    detected_items = ["Tomato", "Cheese", "Chicken", "Lettuce"]
    st.write(", ".join(detected_items))
    
    # Example add-on suggestions based on detected items
    st.write("### Suggested Add-Ons:")
    add_ons = []
    if any(x.lower() in ['tomato', 'cheese', 'pasta'] for x in detected_items):
        add_ons.append("Extra Parmesan Cheese")
    if any(x.lower() in ['chicken', 'meat'] for x in detected_items):
        add_ons.append("Herb Marinade Pack")
    if any(x.lower() in ['lettuce', 'salad', 'veggie'] for x in detected_items):
        add_ons.append("Organic Dressing Pack")
    
    st.write(", ".join(add_ons))
