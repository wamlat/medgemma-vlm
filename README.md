## Reqs
Run in [Google Colab](https://colab.research.google.com) with a GPU enabled (I used A100, which was sufficient). You will also need a Hugging Face account and the [COVIDx CXR-4](https://www.kaggle.com/datasets/andyczhao/covidx-cxr2) dataset (for simplicity, you can upload to Google Drive as a .zip). 

## Model Info / Notes
The model is google/medgemma-4b-it, a VLM for medical tasks. It supports image+text to text via pipeline. Example output (csv) with the input text "Does this chest x-ray display signs of pneumonia?":
Image,Prediction
91cc9818-4778-4659-978c-a5a472e3c416.png,	"Based on the chest x-ray provided, there are **no obvious signs of pneumonia**.

## Running the Code
Note that in the first cell of the Inference section of the notebook, the csv output is currently limited to 20 (this can be changed). The second cell gets the output for all images, of which there are more than 70,000.
