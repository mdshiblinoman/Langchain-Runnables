# LangChain Runnables Tutorial

A collection of Python scripts demonstrating different LangChain Runnable primitives for building LLM-powered chains.

## Prerequisites

- Python 3.8+
- Google Generative AI API key

## Installation

### Step 1: Clone the Repository
```bash
git clone <repository-url>
cd LangchainRunnables
```

### Step 2: Create Virtual Environment (Optional but Recommended)
```bash
python -m venv venv
source venv/bin/activate  # On Linux/Mac
# OR
venv\Scripts\activate     # On Windows
```

### Step 3: Install Dependencies
```bash
pip install langchain langchain-google-genai langchain-core python-dotenv
```

### Step 4: Configure Environment Variables
Create a `.env` file in the project root:
```
GOOGLE_API_KEY=your_google_api_key_here
```

## Runnable Types Explained

### 1. RunnableSequence (`runnable_sequence.py`)
Chains multiple components together in sequence. Each component's output becomes the next component's input.

**Example:** Generates a joke about a topic, then explains the joke.

```bash
python runnable_sequence.py
```

---

### 2. RunnableParallel (`runnable_parallel.py`)
Executes multiple chains simultaneously and returns results as a dictionary.

**Example:** Generates both a tweet and LinkedIn post about a topic in parallel.

```bash
python runnable_parallel.py
```

---

### 3. RunnablePassthrough (`runnable_passthrough.py`)
Passes data through unchanged while other parallel branches process it.

**Example:** Generates a joke and its explanation, preserving the original joke alongside the explanation.

```bash
python runnable_passthrough.py
```

---

### 4. RunnableLambda (`runnable_lambda.py`)
Wraps custom Python functions to use within chains.

**Example:** Counts words in a generated joke using a custom function.

```bash
python runnable_lambda.py
```

---

### 5. RunnableBranch (`runnable_branch.py`)
Implements conditional logic - routes to different chains based on conditions.

**Example:** Generates a report, then summarizes it only if it exceeds 300 words.

```bash
python runnable_branch.py
```

## Quick Start

1. Set up your environment (Steps 1-4 above)
2. Start with `runnable_sequence.py` to understand basic chaining
3. Progress through the files in this order:
   - `runnable_sequence.py` → Basic chaining
   - `runnable_parallel.py` → Parallel execution
   - `runnable_passthrough.py` → Data preservation
   - `runnable_lambda.py` → Custom functions
   - `runnable_branch.py` → Conditional logic

## Project Structure

```
LangchainRunnables/
├── README.md
├── .env                      # Your API keys (create this)
├── runnable_sequence.py      # Sequential chain example
├── runnable_parallel.py      # Parallel execution example
├── runnable_passthrough.py   # Passthrough example
├── runnable_lambda.py        # Custom function example
├── runnable_branch.py        # Conditional branching example
├── langchain-aam.ipynb       # Jupyter notebook examples
└── langchain-mentos.ipynb    # Jupyter notebook examples
```

## Resources

- [LangChain Documentation](https://python.langchain.com/docs/)
- [LangChain Expression Language (LCEL)](https://python.langchain.com/docs/concepts/lcel/)
- [Google Generative AI](https://ai.google.dev/)

## License

MIT License
