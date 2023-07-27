# Build a Retrieval-based Conversational Agent

We will employ a cutting-edge open-source LLM - Llama2

We will also make use of the repository https://github.com/PromtEngineer/localGPT that allows you to run LLMs hosted on huggingface on your Local computer 
## 1. Download the and install localGPT on your computer
- Clone the repository git clone https://github.com/PromtEngineer/localGPT.git          
This will download all the code into a folder called localGPT

cd localGPT 

- Create a conda environment for the project

conda create -n localGPT python=3.10.0

conda activate localGPT

conda install python-duckdb -c conda-forge


python -m pip install -r requirements.txt

- Open the project in VSCode
code .



## 2. Download the knowledgebase you will use
Navigate to the llms folder in the session github and download the file Essential Maternal Newborn Care Guidelines 2022 V3.pdf and add it to the source documents folder. Delete any other existing pdf file.

## 3. Process the knowledgebase file, create embeddings and store them in a vector database

Run

python ingest.py --device_type cpu
or on MAc
python ingest.py --device_type mps

