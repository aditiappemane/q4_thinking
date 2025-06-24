# 🧠 Thinking Mode Sampler (Chain-of-Thought + Self-Consistency)

This project explores how well language models solve GRE-style arithmetic problems using **chain-of-thought reasoning** and **self-consistency voting**.

We compare two strategies:
- **Deterministic Mode**: One answer from the model (temperature=0)
- **Self-Consistency Mode**: 10 varied answers (temperature=1.1) → Majority vote

---

## 📁 Project Structure

├── self_consistency.py # Main evaluation script
├── problem.json # 10 math word problems with correct answers
├── accuracy.png # Output bar chart comparing both strategies
├── README.md # You're here!


---

## 🚀 How to Run

### 1. ✅ Install dependencies

```bash
pip install openai matplotlib

2. ✅ Get a Together.ai API key
Sign up at https://together.ai

Copy your API key

3. ✅ Set your API key
You can either:

Set an environment variable:
export TOGETHER_API_KEY=your_together_key
2. ✅ Get a Together.ai API key
Sign up at https://together.ai

Copy your API key

3. ✅ Set your API key
You can either:

Set an environment variable:
export TOGETHER_API_KEY=your_together_key
Or directly replace it in self_consistency.py:
client = OpenAI(api_key="your_together_key", base_url="https://api.together.xyz/v1")

4. ✅ Run the script
python self_consistency.py
This will:

Run both evaluation modes on problem.json

Print their accuracy scores

Generate accuracy.png

🧪 Example Output
Deterministic accuracy: 2/10
Majority vote accuracy: 2/10

📊 What It Does
Prompts the model with:

Question. Let's think step-by-step.
Extracts the final number from each completion.
For self-consistency, runs the model 10 times and majority-votes the answers.
Compares both strategies against ground truth.

🧠 Powered by
Together.ai API
Mistral/Mixtral 8x7B (via Together)
Python + OpenAI SDK v1.0+
Matplotlib for visualization

