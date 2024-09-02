# Cold Mail Generator

## Overview

The Cold Mail Generator is an end-to-end Python project designed to automate the creation of personalized cold emails for job applications or client outreach. This project utilizes the **LLaMA 3.1 7B parameters model by Meta** to generate professional and tailored emails based on job postings scraped from provided URLs. The user-friendly interface is built with **Streamlit**.

## Features

- **User-Friendly Interface**: The interface is developed using Streamlit, offering a text input pane where users can enter the URL of a job posting, along with a submit button to trigger the process.
- **Automated Web Scraping**: Upon submission, the program scrapes relevant job posting details from the provided URL.
- **Vector Storage with ChromaDB**: The scraped content is stored and processed in ChromaDB, a vector database used to efficiently handle and retrieve text data.
- **AI-Powered Cold Mail Generation**: Leveraging the LLaMA 3.1 model, the application generates a customized cold email. The email is tailored to introduce a company's capabilities, aligning them with the specific requirements of the job posting.

## How It Works

1. **Enter Job Posting URL**: The user inputs the URL of the job posting they are interested in.
2. **Web Scraping**: The program extracts relevant details such as job title, description, and qualifications from the job posting.
3. **Content Processing**: The extracted data is vectorized and stored in ChromaDB, enabling efficient querying and matching.
4. **Cold Mail Generation**: The LLaMA model is prompted with a template that generates a professional cold email, introducing the user's company and its technical expertise in relation to the job posting.

### Example Output

The generated email might look something like this:

> I came across the job description for Lead Software Engineer - ITC at NIKE Inc. and was impressed by the company's commitment to innovation and excellence. As a representative of XYZ, an AI & Software Consulting company, I am excited to introduce our team's capabilities in fulfilling your technical requirements.
>
> With our expertise in cloud environments such as AWS, Azure, and GCP, we can provide a skilled Lead Software Engineer who meets your 8-year experience requirement. Our team has hands-on experience in technical architecture design and development of demand or inventory planning products/applications, including Integrated Business Planning solutions like O9.
>
> [Portfolio Links and Further Details]

## Requirements

- Python 3.x
- Streamlit
- ChromaDB
- LLaMA 3.1 Model

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/cold-mail-generator.git
   cd cold-mail-generator
   ```
2.Install the required packages:

  ```bash
  pip install -r requirements.txt
  ```
3.Set up ChromaDB and the LLaMA model by following the instructions provided in the documentation.

## Usage

### Run the Streamlit app:

```bash
streamlit run main.py
```
1. Enter the URL of the job posting into the text pane.
2. Click the Submit button.
3. The application will scrape the job posting, process the information, and generate a customized cold email using the LLaMA model.

## Project Structure

```bash
├── app/
│   ├── main.py               # Main application script
│   ├── chains.py             # Contains the Chain class and logic
│   ├── requirements.txt      # List of dependencies
│   └── resource/
│       ├── my_portfolio.csv  # Example CSV file for portfolio data
└── README.md                 # Project README file
```
## Acknowledgement

- Meta for providing the LLaMA 3.1 model.
- Streamlit for the simple yet powerful web framework.
- ChromaDB for efficient vector storage.
