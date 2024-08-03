# CodeGemma

CodeGemma is a collection of powerful, lightweight models that can perform a variety of coding tasks like fill-in-the-middle code completion, code generation, natural language understanding, mathematical reasoning, and instruction following.

## Advantages:

Intelligent code completion and generation: Complete lines, functions, and even generate entire blocks of code, whether you’re working locally or using Google Cloud resources.

Enhanced accuracy: Trained on 500 billion tokens of primarily English language data from web documents, mathematics, and code, CodeGemma models generate code that’s not only more syntactically correct but also semantically meaningful, reducing errors and debugging time.

Multi-language proficiency: Supports Python, JavaScript, Java, Kotlin, C++, C#, Rust, Go, and other languages.

Streamlined workflows: Integrate a CodeGemma model into your development environment to write less boilerplate and focus on interesting and differentiated code that matters, faster.

![benchmarks](benchmarks.jpg)

## Fill-in-the-middle

CodeGemma models support fill-in-the-middle (FIM), for use in autocomplete or coding assistant tooling. Below is an example using the Ollama Python library:

response = generate(
  model='codegemma:2b-code',
  prompt=f'<|fim_prefix|>{prefix}<|fim_suffix|>{suffix}<|fim_middle|>',
  options={
    'num_predict': 128,
    'temperature': 0,
    'top_p': 0.9,
    'stop': ['<|file_separator|>'],
  },
)
