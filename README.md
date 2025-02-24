# Text-Driven Photo Organizer

This is a **Streamlit-based application** that allows users to upload images and search them using **natural language queries** powered by OpenAI's CLIP model.

## Features
- Upload images in **JPG, PNG, and HEIC** formats.
- Encodes images using **CLIP (Contrastive Language-Image Pretraining)**.
- Stores embeddings for faster searching.
- Search photos using text descriptions (e.g., "a photo of a sunset").
- Displays the top **3 most relevant images** based on similarity scores.
- Supports caching to **avoid redundant computations**.
- Option to **reset cache** and upload new images.

## Installation

1. Clone this repository:
   ```sh
   git clone https://github.com/your-repo/Text-Driven-Photo-Organizer.git
   cd Text-Driven-Photo-Organizer
   ```

2. Create a virtual environment (optional but recommended):
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```

## Dependencies
The project requires the following Python libraries:
- `streamlit` (for the web interface)
- `torch` (for deep learning computations)
- `transformers` (to load the CLIP model)
- `numpy` (for numerical computations)
- `pillow` (to handle image formats)
- `pillow-heif` (to support HEIC images)
- `pickle` (for caching embeddings)

You can find the full list of dependencies in **requirements.txt**.

## Running the App
### Locally
Run the following command to start the Streamlit app:
```sh
streamlit run app.py
```

### In Jupyter Notebook or Google Colab
If you want to run the app in **Jupyter Notebook** or **Google Colab**, use:
```sh
!streamlit run app.py & npx localtunnel --port 8501 --allow-invalid-certy
```

To get the password for accessing the app, run:
```sh
!curl https://loca.lt/mytunnelpassword
```

## Usage
1. **Upload Images**: Use the file uploader to add images.
2. **Search with Text**: Enter a description (e.g., "a cat on a sofa").
3. **View Results**: The top matching images will be displayed with similarity scores.
4. **Reset Cache**: Clear stored embeddings to process new images.

## Notes
- If you modify the uploaded images, you need to reset the cache to update embeddings.
- The app will automatically detect **new uploads** and re-encode them.

## License
MIT License

---
**Author:** Sheraz Ahmed

