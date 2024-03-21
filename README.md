# AIPI590-Project1
This project is to try to improve the performance of a LLM on a specific property ("focal property"). We mainly focus on the law professional knowledge and try to fine tuning a Law-QA model.

We fine-tuned Meta's LLM: Llama 2 thru Hugging Face Api: meta-llama/Llama-2-7b-chat-hf

Models are separatly fine-tuned on two dataset:
- joey234/mmlu-professional_law, link: https://huggingface.co/datasets/joey234/mmlu-professional_law
- joey234/mmlu-professional_law-neg, link: https://huggingface.co/datasets/joey234/mmlu-professional_law-neg

Models are trained using Colab pro A100 GPU.

Results:
| Model                           | Dataset                               | Accuracy | Response Time/question (s) |
|---------------------------------|---------------------------------------|----------|---------------------------|
| Pot-1/llama-7b-lawbot-true      | joey234/mmlu-professional law         | 0.4      | ~40                       |
| Pot-1/llama-7b-lawbot      | joey234/mmlu-professional law-neg     | 0.35     | ~40                       |
| Llama-2-7b-chat-hf              | joey234/mmlu-professional law         | 0.3      | ~120                      |
| Llama-2-7b-chat-hf              | joey234/mmlu-professional law-neg     | 0.1      | ~120                      |


