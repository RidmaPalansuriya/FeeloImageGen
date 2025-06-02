# Feelo Cover Images Automation

This project automates the creation of promotional cover images by overlaying the Feelo logo and vendor logos onto background images using data from a CSV file. The system is implemented in Google Colab and uses Google Drive for input and output management.

📦 Features
✅ Automatically generates deal images from CSV input

✅ Supports Google Drive-hosted images (with shared links)

✅ Overlays both Feelo and Vendor logos on the background image

✅ Saves the output as PNG images in a dedicated folder

✅ Option to zip and download final images (manually or with script extension)

🧰 Requirements
Ensure these Python packages are installed:

bash
Copy
Edit
pip install pillow pandas
📂 Folder Structure
graphql
Copy
Edit
Feelo_Images_Automation/
├── dealsList.csv                  # CSV file with deal data
├── feelo_logo.png                # Transparent PNG logo for Feelo
├── output_images/                # Folder for generated images
├── feelo_cover_images.zip        # (Optional) Zip file of output images
└── Feelo_Image_Generator.ipynb   # Colab notebook or Python script
📄 CSV Format
The CSV file (dealsList.csv) should have the following columns:

Deal Title	Vendor Name	Background Image URL	Vendor Logo URL	Output File Name
Buy 1 Burger & Get 1 Free	Burger Cottage	https://drive.google.com/file/d/FILE_ID/view?usp=sharing	https://drive.google.com/file/d/FILE_ID/view?usp=sharing	burger_cottage_deal

🔗 Note: Make sure all Google Drive links are public and shared with "Anyone with the link" access.

🖼️ Image Processing Logic
For each row in the CSV:

Download and convert the background and vendor logo images from Google Drive.

Resize all images to fit a 1080x1080 square canvas.

Overlay the Feelo logo on the top-left and the vendor logo on the top-right.

Save the final composition as a PNG file in the output_images directory.

🚀 Usage (Colab)
Run the pip install and Google Drive mount cells.

Place dealsList.csv, feelo_logo.png, and required images in the correct Drive folder.

Run the main code block to generate images.

(Optional) Zip the output_images folder for download.

❗ Common Errors
Feelo logo missing — skipping image generation: Make sure feelo_logo.png exists in the base path.

Background image not accessible: Ensure the shared Google Drive image link is public.

File is not a valid image: Ensure the files are valid .png, .jpg, or .jpeg formats.

📌 To Do
 Add text overlays (e.g., deal titles)

 Support more dynamic image sizes

 UI preview option using Streamlit or Gradio

🧑‍💻 Author
Built by Ridma Palansuriya
For internal use @Feelo

