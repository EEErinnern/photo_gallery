import streamlit as st
import os

def load_photos(directory):
    photos = []
    for filename in os.listdir(directory):
        if filename.endswith(".jpg") or filename.endswith(".png"):
            photo_path = os.path.join(directory, filename)
            photos.append(photo_path)
    return photos

def main():
    st.title("My Photo Gallery")
    
    photo_directory = "path/to/your/photos"
    photos = load_photos(photo_directory)
    
    st.subheader("Gallery")
    for photo in photos:
        image_iterator = paginator("Select a sunset page", sunset_imgs)
        indices_on_page, images_on_page = map(list, zip(*image_iterator))
        st.image(photo, caption=os.path.basename(photo), use_column_width=True)

if __name__ == "__main__":
    main()
