# RAG Evaluation Project Documentation

## Overview
This project provides tools and scripts to evaluate Retrieval-Augmented Generation (RAG) systems using the [ragas](https://github.com/explodinggradients/ragas) library. It supports running evaluation pipelines, integrating with LLMs, and analyzing RAG performance metrics.

## Project Structure

- `main.py`: Main script for running RAG evaluation workflows.
- `evalute-with-ragas.py`: Script for evaluating RAG outputs using the ragas library.
- `pyproject.toml`: Project dependencies and configuration.
- `uv.lock`: Lock file for reproducible environments.
- `README.md`: Project overview and quick start (see also this documentation).

## Setup Instructions

### 1. Clone the Repository
```bash
git clone <repo-url>
cd rag_evaluation
```

### 2. Install Dependencies
This project uses [uv](https://github.com/astral-sh/uv) for dependency management. If you don't have `uv`, install it or use `pip` as an alternative.

#### Using uv
```bash
uv pip install -r pyproject.toml
```

#### Using pip
```bash
pip install -r requirements.txt  # If requirements.txt is available
# Or manually install dependencies:
pip install ragas langchain langchain_ollama langchain_community openai faiss-cpu numpy datasets python-dotenv pillow
```

### 3. Environment Variables
Create a `.env` file in the project root with your API keys:
```
OPENAI_API_KEY=your_openai_api_key
```

## Usage

### Evaluate with Ragas
Run the evaluation script:
```bash
uv run evalute-with-ragas.py
```
Or, if using Python directly:
```bash
python evalute-with-ragas.py
```

### Main Workflow
To run the main workflow:
```bash
uv run main.py
# or
python main.py
```

## Troubleshooting

- **ModuleNotFoundError: No module named 'PIL'**
  - Solution: Install Pillow with `pip install pillow`.
- **API Key Errors**
  - Ensure your `.env` file is present and contains valid API keys.
- **Dependency Issues**
  - Double-check that all required packages are installed. See the setup section above.
- **Script Name Typo**
  - The script is named `evalute-with-ragas.py` (note the typo). You may rename it to `evaluate-with-ragas.py` for clarity.

## References
- [ragas documentation](https://github.com/explodinggradients/ragas)
- [LangChain documentation](https://python.langchain.com/)
- [OpenAI API documentation](https://platform.openai.com/docs/)

---

