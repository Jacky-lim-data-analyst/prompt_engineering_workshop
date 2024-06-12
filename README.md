# Prerequisite
- Basic knowledge of Python programmming
- Subscribe to [OpenAI API](https://platform.openai.com/docs/api-reference/introduction). GPT models developed by OpenAI will be used throughout the workshop.

# Data source
We need Kaggle dataset ([Edmunds-Consumer Car Ratings and Reviews](https://www.kaggle.com/datasets/ankkur13/edmundsconsumer-car-ratings-and-reviews)) for the RAG demo. Make sure you have a Kaggle account and sign up for one if you are new to Kaggle. Download the dataset and place it in your working directory.

## Jupyter notebook on local device
Download & unzip the dataset and place all the csv file on the virtual environment.

## Colab user
```
# step 1
!pip install kaggle

# step 2:
from google.colab import files
files.upload()

# step 3:
!mkdir ~/.kaggle
!cp kaggle.json ~/.kaggle

# step 4:
!chmod 600 ~/.kaggle/kaggle.json
```
Or you can refer to this [Kaggle discussion](https://www.kaggle.com/discussions/general/74235).

# OpenAI API
You can either set your OpenAI API key in `.env` file or in `config.json` file.
## .env
```
OPENAAPI_API_KEY = sk-...
```
## config.json
```
{
  "openai_api_key" = "sk-..."
}
```

# Dependencies
All the dependencies are documented in `requirements.txt`.

# Google Colab
Make sure that the hidden file `.env` and json file `config.json` are located on the working directory. Firstly, create the files locally as shown above and upload them to google Colab.
```
from google.colab import files

uploaded = files.upload()
```
A "choose file" button will pop out.
