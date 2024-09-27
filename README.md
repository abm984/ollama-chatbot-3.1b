# ollama-chatbot-3.1b
For a flask base app of this same model you can check Urooj Projet which has detail work on flask base onboarding ap using the same approach 
```bash

https://github.com/urooj-akmal/Onboarding-Chatbot

```

## Complete Step-by-Step Guide: Onboarding Chatbot with Ollama

This guide walks you through setting up and running the onboarding chatbot utilizing Ollama and Flask.

**Prerequisites:**

* **Python 3.12.4:** Ensure you have Python 3.12 or later installed. Check by running `python --version` in your terminal.

**1. Install Ollama:**

- Ollama allows you to run large language models (LLMs) locally.
- It's available for Windows, macOS, and Linux.

**Download Links:**

- https://ollama.com/download

**Installation Instructions:**

   **a. Windows:**

      1. Download the Ollama executable from the link above.
      2. Double-click the downloaded file (e.g., `ollama-setup.exe`).
      3. Follow the on-screen installation instructions.

   **b. macOS:**

      1. Download the Ollama application from the link above.
      2. Unzip the downloaded file.
      3. Drag the `Ollama.app` folder to your Applications directory.

   **c. Linux:**

      1. Open your terminal.
      2. Run the following command:

         ```bash
         curl -fsSL https://ollama.com/install.sh | sh
         ```
**2. Pull the Ollama Model:**

Before starting the chatbot, download the desired LLM model using Ollama. 

- The chatbot uses the Llama 3.1:8b model (requires 4.7GB of space).
- Run the following command in your terminal:

```bash
ollama pull llama3.1:8b
```

**3. Start the Ollama Backend:**

- Start the Ollama backend server to make the language model available for the chatbot:
  - using the command line, run:

      ```bash
      ollama start
      ```

**4. Clone the Repository:**

Once Ollama is installed, clone the chatbot repository from GitHub:

```bash
git clone https://github.com/abm984/ollama-chatbot-3.1b.git
```


**5. Install Dependencies:**

Navigate to the cloned repository directory:

```bash
cd ollama-chatbot-3.1b
```

Install the necessary Python libraries using the `requirements.txt` file:

```bash
pip install -r requirements.txt
```

**6. Prepare Your Data:**

- Gather the PDF documents that you want the chatbot to be able to answer questions from.
- Ensure these PDFs are in a well-organized format within a specific directory (e.g., `data`).

![image](https://github.com/user-attachments/assets/1f50f8b7-a2ba-47de-82a7-7267a2b35463)



**7. Populate the Database:**

- Run the `POPULATE_DATABASE` script to process the PDFs and populate the Chroma database with relevant information.
     ```bash
   python populate_database.py
   ```
  
**7. Set Up Environment Variables:**

The application uses a few environment variables:

* **CHROMA_PATH:** Path to the directory where the Chroma database will be stored. 

**Here's an example of setting these variables in your terminal:**
