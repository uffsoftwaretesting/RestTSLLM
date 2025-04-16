# 🧪 Integration Test Generation Using LLMs and TSL

This repository contains the artifacts for the study **"Combining TSL and LLMs to Automate REST API Testing: A Comparative Study"**, which evaluates the use of large language models (LLMs) to generate integration tests for REST APIs based on OpenAPI specifications with an intermediate step using TSL.

## 📂 Repository Structure

```
├── general-files/
│   ├── default-prompts/           # Prompt examples used in the few-shot and decomposed prompting strategy
│   ├── examples/                  # OpenAPI, TSL and Integration Tests examples used to teach LLMs 
├── llm-processor/                 # Script for LLM interaction and execution
├── projects/
│   └── <project-name>/            # Cloned API projects with OpenAPI and results
│       └── prompt-engineering/
│           ├── prompts/           # Input - Specific prompt used in this project
│           ├── output/            # Output - Generated test cases and integration test code for each LLM in this project
├── pdfs/                          # Public evidence files (e.g., results summary)
```

## 🚀 How to use LLM Processor

Check instructions [here](llm-processor/README.md).

## 📊 Results

The study evaluated multiple LLMs (GPT 4o (OpenAI), LLaMA 3.2 90b (Meta), Claude 3.5 Sonnet (Anthropic), Gemini 1.5 Pro (Google), Deepseek R1 (Deepseek), Mistral Large (Mistral), Qwen 2.5 32b (Alibaba), and Sabiá 3 (Maritaca)) using metrics such as:
- ✅ Success Rate
- 📈 Code Coverage
- 🧬 Mutation Score
- 💰 Cost per Execution

Result can be found in:
- Output: [projects](projects/files.md).
- Metrics: [pdfs](pdfs/all_results.pdf).

## 📄 Paper

A preprint of the full paper will be made available here upon acceptance.  
In the meantime, the anonymous version used for submission is available at:

📎 [Anonymous Submission (4Open)](https://anonymous.4open.science/r/integration-test-with-llm)