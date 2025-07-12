# CodeMMLU Challenge

The CodeMMLU benchmark tests LLMs on their understanding of code and software engineering principles through nearly 3,000 multiple-choice questions.

Challenge link: https://www.kaggle.com/competitions/fpt-ai-residency-batch-6-entry-test/overview

 My work focuses on evaluating and fine-tuning two competitive open-source models:

- **Meta-LLaMA-3.3-70B Instruct**
- **Qwen3-32B**

## Methodology

### 1. Base Model Selection
Five models were initially evaluated in Zero-shot and Chain-of-Thought (CoT) settings. GPT-4o, Meta-LLaMA variants, and Qwen3 were compared, with Meta-LLaMA-3.3 and Qwen3-32B selected for fine-tuning based on strong baseline performance.

### 2. Dataset Construction for Fine-tuning
Since the original training set contains only questions and correct answers, I used GPT-4o with CoT prompting to generate detailed reasoning responses. Responses were included in the dataset only if they were correct or could be corrected with further prompting.

### 3. Fine-tuning and Submission
- **Meta-LLaMA-3.3-70B Instruct** was fine-tuned using **LoRA** and deployed via **Together AI**.
- **Qwen3-32B** was fine-tuned on **Google Colab** using the **Unsloth** library.

Model performance was evaluated via private leaderboard submissions.


## Tools & Libraries
- Huggingface
- Unsloth
- Together AI
- OpenAI API