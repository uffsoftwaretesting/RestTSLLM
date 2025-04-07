## Prompts (input/output) - Books API

  
    {s2}{\llm{deepseek}[\IfNoValueTF{#2}{}{#2}]}%,
    {s3}{\llm{qwen}[\IfNoValueTF{#2}{}{#2}]}%,
    {s4}{\llm{sabia}[\IfNoValueTF{#2}{}{#2}]}%,
    {s5}{\llm{llama}[\IfNoValueTF{#2}{}{#2}]}%,
    {s6}{\llm{gpt}[\IfNoValueTF{#2}{}{#2}]}%,
    {s7}{\llm{gemini}[\IfNoValueTF{#2}{}{#2}]}%,
    {s8}{\llm{mistral}[\IfNoValueTF{#2}{}{#2}]}%

| Input | Claude 3.5 Sonnet | Deepseek R1 | Qwen 2.5 32b | Sabiá 3 | LLaMA 3.2 90b | GPT 4o | Gemini 1.5 Pro | Mistral Large |
|---|---|---|---|---|---|---|---|---|
| [0_system_command.txt](prompts/0_system_command.txt)                                        | [output]() | [output]() | [output]() | [output]() | [output]() | [output]() | [output]() | [output]() | 
| [1_exemple_openapi_to_tsl.txt](prompts/1_exemple_openapi_to_tsl.txt)                        | [output]() | [output]() | [output]() | [output]() | [output]() | [output]() | [output]() | [output]() | 
| [2_exemple_tsl_to_integration_tests.txt](prompts/2_exemple_tsl_to_integration_tests.txt)    | [output]() | [output]() | [output]() | [output]() | [output]() | [output]() | [output]() | [output]() |  
| [3_convert_openapi_to_tsl.txt](prompts/3_convert_openapi_to_tsl.txt)                        | [output]() | [output]() | [output]() | [output]() | [output]() | [output]() | [output]() | [output]() |  
| [4_convert_tsl_to_integration_tests.txt](prompts/4_convert_tsl_to_integration_tests.txt)    | [output]() | [output]() | [output]() | [output]() | [output]() | [output]() | [output]() | [output]() | 
