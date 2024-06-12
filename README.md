# 1. Prerequisite
- Basic knowledge of Python programmming
- Subscribe to [OpenAI API](https://platform.openai.com/docs/api-reference/introduction). GPT models developed by OpenAI will be used throughout the workshop.

# 2. Data source
We need Kaggle dataset ([Edmunds-Consumer Car Ratings and Reviews](https://www.kaggle.com/datasets/ankkur13/edmundsconsumer-car-ratings-and-reviews)) for the RAG demo. Make sure you have a Kaggle account and sign up for one if you are new to Kaggle.

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

# 3. OpenAI API key
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

## Local Jupyter notebook
Place the files in your working directory.

## Google Colab
Make sure that the hidden file `.env` and json file `config.json` are located on the working directory. Firstly, create the files locally as shown above and upload them to google Colab.
```
from google.colab import files

uploaded = files.upload()
```
A "choose file" button will pop out.

# 4. Dependencies
All the dependencies are documented in `requirements.txt`. Install packages with the following commands:
```
pip install -r requirements.txt
```

# 5. Clone / download github repo
## 5a Google Colab
1. Create an empty folder on your Google Drive.
2. Mount your google drive
```
from google.colab import drive
drive.mount(‘/content/gdrive’)
```
3. Change your working directory
4. Clone the github repo by following the command:
```
git clone https://github.com/Jacky-lim-data-analyst/prompt_engineering_workshop.git
```
5. Set up the OPENAI API key as mentioned on section 3.

## 5b Local Jupyter notebook (recommended)
Or download the repo in a compressed zip file and open the Jupyter notebook locally.
