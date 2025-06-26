# 🧩 Integration Test Generation Using LLMs and TSL

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

## 🧪 How to reproduce the experiment

1. Into `llm-processor/config` dir, make a copy from `.env.sample` to `.env` and add your API keys to each LLM provider. You can add only a few API keys if you only want to test a few LLMs.
2. From root, run the follow command to process LLMs for each project that you want to reproduce. If you only want to reproduce the results for just one or few projects, feel free to run the command for whatever project you want (change `<project>` for the available projects `todo-api`, `hotels-api`, `restaurants-api`, `books-api`, `supermarket-api`, and/or `shortener-api`). You can run all LLMs if you have added all API keys or, just change the parameter `--llms=<model>` to point to a specific model (`claude`, `qwen`, `mistral`, `gpt`, `sabia`, `deepseek`, `llama`, or `gemini`)
```
cd llm-processor
python3 -m pip install -r ./requirements.txt
python3 main.py --prompts-dir="../projects/<project>/prompt-engineering/prompts" \
                --system-command-file="../projects/<project>/prompt-engineering/prompts/0_system_command.txt" \
                --output-dir="../projects/<project>/prompt-engineering/output" \
                --llms=all
```
3. After it, you can open a project into Visual Studio (from `projects/<project>/<project>-llm-<model>`) and copy results (from `projects/<project>/prompt-engineering/output`) and paste into existing test project.
4. You can run tests from IDE to verify the results from coverage and to collect mutation score you only need to run the follow command `dotnet stryker --output llm-test-generation-files`, but, some projects have some dependencies and you need to provide executing docker for example. The dependecies and full CLI commands for each project you can find in `dependencies-and-commands.yml`.

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

## 📚 Citation
[![Cite this paper](https://img.shields.io/badge/Cite%20this%20paper-SBES%202025-blue)](#citation)

If you use **RestTSLLM** in your research or project, please cite:

```bibtex

@inproceedings{barradas2025tsl,
  author    = {Thiago Barradas and Aline Paes and Vânia de Oliveira Neves},
  title     = {Combining TSL and LLM to Automate REST API Testing: A Comparative Study},
  booktitle = {Proceedings of the XXXIX Brazilian Symposium on Software Engineering (SBES)},
  year      = {2025},
  note      = {To appear}
} 

```

**Text citation format:**

```
Barradas, T., Paes, A., & Neves, V. O. (2025). Combining TSL and LLM to Automate REST API Testing: A Comparative Study. In: Proceedings of the XXXIX Brazilian Symposium on Software Engineering (SBES). To appear.

```

