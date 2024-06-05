# Data source
We need Kaggle dataset ([Edmunds-Consumer Car Ratings and Reviews](https://www.kaggle.com/datasets/ankkur13/edmundsconsumer-car-ratings-and-reviews)) for the RAG demo.

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
