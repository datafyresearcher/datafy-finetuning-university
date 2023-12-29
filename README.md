<h1 align="center">
📖 DATAFY FINETUNING COURSE
</h1>

<p align="center" width="100%">
    <img width="100%" height="100%" src="https://github.com/datafyresearcher/datafy-finetuning-university/blob/main/picture/1.png"></a>
</p>

A collection of notebooks for DATAFY FINETUNING COURSE


## Learning Objectives

- Learn the fundamentals of finetuning a large language model (LLM).
- Data Preparation for Finetuning with help of Human Efforts
- Understand how finetuning differs from prompt engineering, and when to use both.
- Get practical experience with real data sets, and how to use techniques for your own projects.

## 🔧 Features

- Collection of Notebooks
- Google Colab
- Docker Support with Optimisation Cache etc
- Run the Notebook Server with Docker

This repo contains an `notebooks` flocation contains the ntebooks

## 💻 Generate API Key for LAMINI

1. Sign up on https://www.lamini.ai/
2. Go to Account and get the API key Under `Active API Tokens`
3. Under `.powerml/configure_llama.yaml`, add the key
4. `dotenv` can also be used to setup the key. Use the `env.example` to create `env` file

for more on Authentcation read `https://lamini-ai.github.io/auth/`

## 💻 Fork the Course Repositry

Fork the Course GitHub Repository and Start working. Got Below Link and Click Fork 

```bash
https://github.com/datafyresearcher/datafy-finetuning-university
```
<datafyresearcher>, Change to your Own Username for below commands 

## 💻 Running on Google Colab

Google Colab offer free GPU therefore, running on Google Colab is prefferd method

1. To get started, you need to mount your Google Drive in Colab. You can do this by running the following command:
```bash
from google.colab import drive
drive.mount('/content/drive')
```

2. Once your Drive is mounted, you can clone a repository by running the following command:
```bash
!git clone https://github.com/datafyresearcher/datafy-finetuning-university.git /content/drive/MyDrive/datafy-finetuning-university
```

This will clone the repository to your Colab instance, and you can work on it just as you would on your local machine. When you want to push your changes back to the repository, you can use the usual Git commands, such as:

```bash
!git add .
!git commit -m "Commit message"
!git push origin <branch>
```

## 💻 Running Locally

1. Clone the repository📂

```bash
git clone https://github.com/datafyresearcher/datafy-finetuning-university.git
```

2. Install dependencies with [Poetry](https://python-poetry.org/) and activate virtual environment🔨

```bash
poetry install
poetry shell
```

3. Copy and Modify `env.example` to `.env`

Generate the HF API Key to be able to hosted models for inference and set the variables accordingly.

4. Run the JupyterLab server🚀

```bash
jupyter lab
```


Run Notebooks using Docker
--------------------------
This project includes `Dockerfile` to run the app in Docker container. In order to optimise the Docker Image
size and building time with cache techniques, I have follow tricks in below Article 
https://medium.com/@albertazzir/blazing-fast-python-docker-builds-with-poetry-a78a66f5aed0

Build the docker container

```bash
docker  build . -t datafy-finetuning-course:latest 
```

To generate Image with `DOCKER_BUILDKIT`, follow below command

```bash
DOCKER_BUILDKIT=1 docker build --target=runtime . -t datafy-finetuning-course:latest
```

1. Run the docker container directly 

```bash
docker run -d --name datafy-finetuning-course -p 8888:8888 datafy-finetuning-course:latest 
```

2. Run the docker container using docker-compose (Recommended)

```bash
docker-compose up
```

> Make sure to include the `.env` SECRETS file when running with `docker-compose` with your own Keys.


## Report Feedbacks

As `dlai-hf-course:latest` is a template project with minimal example. Report issues if you face any. 

## DISCLAIMER & CREDITS

We have collected the Notebooks from original course and edited for few lines/functions to make them run locally. 