<a href="https://colab.research.google.com/github/datafyresearcher/datafy-finetuning-university/blob/main/notebooks/0_Preparing_setup_datafy_finetuning.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

# DATAFY FINETUNING: Initial Setup

<p align="center" width="100%">
    <img width="100%" height="100%" src="https://github.com/datafyresearcher/datafy-finetuning-university/blob/main/picture/2.jpg"></a>
</p>

## Pre-Requisite

1. GitHub Account: For the https://github.com/datafyresearcher/datafy-finetuning-university
2. Google Account: For Google Colab and Google Drive

## 💻 Generate API Key for LAMINI

1. Sign up on https://www.lamini.ai/
2. Go to Account and get the API key Under `Active API Tokens`
3. Under `.powerml/configure_llama.yaml`, add the key
4. `dotenv` can also be used to setup the key. Use the `env.example` to create `env` file

for more on Authentcation read `https://lamini-ai.github.io/auth/`


#### Google Colab offer free GPU therefore, running on Google Colab is prefferd method

1. To get started, you need to mount your Google Drive in Colab. You can do this by running the following command:

```bash
# Mount the Google Drive
from google.colab import drive
drive.mount('/content/drive')
```

2. Once your Drive is mounted, you can clone a repository by running the following command:

```bash
!git clone https://github.com/datafyresearcher/datafy-finetuning-university.git /content/drive/MyDrive/datafy-finetuning-university
```

```bash
!ls
```

```bash
%cd drive/MyDrive/datafy-finetuning-university
```

```bash
%pwd
```

```bash
!ls
```

#### *Upload the `.env` file to your google drive location with LAMINI_API_KEY and OPEN_API_KEY*