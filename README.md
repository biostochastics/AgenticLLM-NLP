# LLM-NLP

# LLM-based Topic and Sentiment Analysis of Chinese Sentences

## Overview

This Google Colab notebook provides a framework for performing topic and sentiment analysis on a set of Chinese sentences using Large Language Models (LLMs). It leverages the OpenRouter API to access various LLMs, including GPT-4, Claude, Qwen, Gemini, and Llama. The analysis is conducted in two stages:

1. **Topic Identification:** Determining the main theme or topic of each sentence.
2. **Multi-Dimensional Analysis:** Analyzing sentiment, emotions, implied likelihood, realism, temporal orientation, and other noteworthy dimensions.

## Requirements

- **OpenRouter API Key:** You need an API key from OpenRouter to access the LLMs. You can obtain one by signing up on their website. 
- **Python Libraries:** The following libraries are required:
    - `transformers`
    - `openai`
    - `openrouter`
    - `aiohttp`
    - `nest_asyncio`
    - `pandas`
    - `backoff`
    - `re`

## Data

The notebook assumes that the input data is stored in a TSV file (`data_chinese.txt`). Each line in the file should contain a single Chinese sentence. The notebook includes functionality to anonymize the data by removing Personally Identifiable Information (PII) using the `PIIRemover` class.

## Usage

1. **Setup Environment:** Install the necessary libraries using the provided `pip install` commands.
2. **Load Data and Anonymize:** Load the data from the TSV file and apply the `PIIRemover` to anonymize it if needed.
3. **Analysis:**
    - **Prompt Engineering:** The notebook includes pre-defined prompts for the LLMs. You can modify or create your own prompts as needed.
    - **LLM Selection:** Choose the desired LLMs for the analysis from the available options.
    - **Execution:** Run the analysis functions, which will send the sentences and prompts to the selected LLMs via the OpenRouter API.
    - **Output:** The results of the analysis are stored in a dictionary and can be saved to a JSON file for further processing.
4. **Synthesis:** The notebook uses the `o1-preview` model to synthesize the categories identified by the different LLMs. This provides a comprehensive overview of the topics, dimensions, patterns, and trends discovered in the sentences.
5. **Rubrics:** The notebook includes a rubric for scoring, translated into English, Chinese, and Russian, for ease of use and comprehensive analysis.
6. **Template:** The notebook defines a structured template for model responses, ensuring consistency and suitability for downstream analysis.

## Limitations

- **Accuracy:** The accuracy of the analysis depends on the quality of the prompts and the capabilities of the selected LLMs.
- **Bias:** LLMs can be prone to biases, which might influence the analysis results.
- **Cost:** Using the OpenRouter API might incur costs depending on your usage.

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## License

This project is licensed under the MIT License.

## Disclaimer

This notebook is for research and educational purposes only. Use it responsibly and be aware of the limitations of LLMs.
