<h1>RAG with Ollama Locally</h1>

<h3>1. Create a virtual environment</h3>

```
python -m venv venv
```

<h3>2. Activate the virtual environment</h3>

```
venv\Scripts\Activate
(or on Mac): source venv/bin/activate
```

<h3>3. Install libraries</h3>

```
pip install -r requirements.txt
```

<h3>4. Add Bright Data API Key</h3>
<ul>
<li>Rename the .env.example file to .env</li>
<li>Add your Bright Data API key</li>
<li><i>If you want to use ChatGPT or Anthropic models, add an API key (not required for Ollama)</i></li>
</ul>

<h2>Executing the scripts</h2>

- Open a terminal in VS Code

- Execute the following command:

```
python run 1_scraping_wikipedia.py
python run 2_chunking_embedding_ingestion.py
streamlit run 3_chatbot.py
```
