# Skill – Generative AI Lab Experiments

| Folder | Topic |
|---|---|
| `Week-1/` | First LLM API call with Gemini |
| `Week-2/` | Provider-agnostic LLM client (Gemini + local Ollama) with unit test |
| `Week-3/` | LLM call monitoring: latency, tokens, cost and retries logged to MongoDB |
| `Week-4/` | Tokenizer comparison: BPE vs WordPiece vs SentencePiece (English, Telugu, Hindi) |
| `Week-5/` | Token economics: cost and context-window calculations |
| `Week-6/` | Golden question set and Release v0.1 baseline with Llama 3.2 |

## Setup
```bash
python3 -m venv .venv && source .venv/bin/activate
pip install google-genai python-dotenv requests pytest pymongo transformers sentencepiece tiktoken protobuf
```
Weeks 1-3 need a Gemini API key: copy `.env.example` to `.env` in the week folder and fill it in. **Never commit `.env`.**
Weeks 2, 3 and 6 use Ollama (`ollama pull llama3.2`, then `ollama serve`); Week 3 also needs MongoDB on port 27017.
Run each week from inside its own folder, e.g. `cd Week-6 && python main.py`.
