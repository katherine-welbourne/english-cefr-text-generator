# **English CEFR Text Generator** 🎓 📖
Generating text aligned with CEFR levels to aid language learning.
---

<div align="left">
  <a href="https://github.com/katherine-welbourne/cefr-text-generator/blob/main/cefr_demo.png">
    <img src="cefr_demo.png" alt="CEFR Text Generator" width="400">
  </a>
</div>

---

## **Table of Contents** 📚
1. [Overview](#overview)
2. [Dataset](#dataset)
3. [Model](#model)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Example Output](#example-output)
7. [Future Enhancements](#future-enhancements)
8. [License](#license)

---

## **Overview** 📝
The CEFR Level Sentence Generator is a machine learning project that generates text based on the Common European Framework of Reference for Languages (CEFR). The generated sentences focus on vocabulary from a specified CEFR level while allowing the use of lower-level vocabulary for naturalness.

### Key Features:
- Input CEFR levels: A1, A2, B1, B2, C1, C2. 🛠️
- Emphasizes vocabulary from the target level. ✍️
- Utilizes Hugging Face Transformers for text generation. 🤖
- Color-coded output to indicate CEFR levels of used vocabulary. 🌈

---

## **Dataset** 📊
The dataset used is a custom CEFR vocabulary dataset:
- **Source File**: `/content/drive/MyDrive/ML/Datasets/ENGLISH_CERF_WORDS.csv`
- **Columns**:
  - `headword`: English word.
  - `CEFR`: CEFR level (A1 to C2).

---

## **Model** 🤖
The project uses Hugging Face’s pre-trained GPT-2 model:
- **Base Model**: [GPT-2](https://huggingface.co/gpt2) 🚀
- **Fine-Tuned For**: CEFR-constrained text generation.
- **Framework**: Hugging Face Transformers. 🛠️

---

## **Installation** ⚙️
To set up the project locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/katherine-welbourne/cefr-text-generator.git
   cd cefr-text-generator
   ```

2. Install dependencies:
   ```bash
   pip install transformers torch pandas
   ```

---

## **Usage** 🏋️
### Generate Text:
```python
# Example usage
level = "B2"  # Desired CEFR level
prompt = "Once upon a time"
max_length = 50
output_text = generate_text_cefr(level=level, prompt=prompt, max_length=max_length)
print(output_text)
```

### Visualize CEFR Levels:
Color-code the generated text by CEFR level:
```python
color_text_by_cefr(output_text, df)
```

---

## **Example Output** 🏆
### Input
- CEFR Level: B2
- Prompt: "The world is"

### Output
```plaintext
The world is a fascinating place where individuals often encounter unique challenges and opportunities.
```

### CEFR Distribution:
- A1: 5 words
- A2: 3 words
- B1: 4 words
- B2: 2 words
- C1: 1 word
- C2: 0 words

---

## **Future Enhancements** 🚀
- Add multilingual support for CEFR-level text generation.
- Fine-tune models for domain-specific vocabulary.
- Develop an interactive demo using Gradio or Streamlit.

---

## **License** 📜
This project is licensed under the [MIT License](LICENSE). 📖

---

