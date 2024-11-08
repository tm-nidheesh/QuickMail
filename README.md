# 📧 Cold Mail Generator
Cold email generator for services company using groq, langchain and streamlit. It allows users to input the URL of a company's careers page. The tool then extracts job listings from that page and generates personalized cold emails. These emails include relevant portfolio links sourced from a vector database, based on the specific job descriptions. 

## Project Overview
This project automates the process of generating personalized job application responses for specific roles by leveraging Large Language Models (LLM), particularly Llama 3.2, along with ChromaDB for efficient data storage and retrieval. The workflow consists of extracting job description data from a career page, parsing it to identify essential skills and requirements, and generating tailored cover letters or application responses.

## Architecture Diagram

<img width="703" alt="project overview" src="https://github.com/user-attachments/assets/0bb1b498-9efb-403b-808f-453678d177ae">

![architecture](https://github.com/user-attachments/assets/029c71e4-2b46-4573-bc8a-8e7d8d7e9291)


## Prerequisites
* Python 3.x
* API access to Llama 3.1 (or a similar LLM model)
* ChromaDB setup and configuration

## Technologies Used
* LLM (Llama 3.2): For natural language processing to parse job descriptions and generate customized application responses.
* ChromaDB: A database solution to store and retrieve portfolio links and metadata associated with job descriptions.
* Python: For scripting and automating the process.

## Workflow
* Extract Text from Career Page:<br
The system extracts text from a job listing, pulling key details like required skills, years of experience, and role responsibilities.<br>
The extracted job description is parsed into a JSON format. <br>

* Data Processing with LLM (Llama 3.1):<br>
The extracted job details are processed by LLM (Llama 3.1) to generate a personalized cover letter or application response.<br>
The model takes the job description as input, analyzes the requirements, and creates a tailored response, highlighting relevant skills, experiences, and links to the applicant's portfolio.<br>

* Portfolio Links Storage with ChromaDB:<br>
Links to relevant portfolio projects or experiences are stored in ChromaDB.<br>
The LLM uses this database to pull specific portfolio links that best match the job description, enhancing the personalization of each application.<br>

## Set-up
1. To get started we first need to get an API_KEY from here: https://console.groq.com/keys. Inside `app/.env` update the value of `GROQ_API_KEY` with the API_KEY you created. 


2. To get started, first install the dependencies using:
    ```commandline
     pip install -r requirements.txt
    ```
   
3. Run the streamlit app:
   ```commandline
   streamlit run app/main.py
   ```
   


