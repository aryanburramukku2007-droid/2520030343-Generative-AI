## Tokenizer Comparison
# Objective: The main objective of this experiment is to compare how different tokenizer methods split English, Telugu, and Hindi text into tokens and token IDs.

Project Folder Structure
1. requirements.txt -> Used to install the required libraries.
2. tokenizer_comparison.py -> The main Python program that loads the tokenizers and compares their output.

How it works
1. Activate the existing virtual environment.
2. Install the required libraries:

        pip install -r requirements.txt
3. The program loads three pretrained tokenizers:
   - BPE using GPT-2
   - WordPiece using Multilingual BERT
   - SentencePiece using XLM-R
4. It gives sample text in English, Telugu, and Hindi to every tokenizer.
5. Each tokenizer converts the text into tokens and token IDs.
6. The program prints the token pieces, token IDs, and total token count.

Run the program using:
 
          python tokenizer_comparison.py
Expected Output
For every language, the program shows the input text and the result from all three tokenizer methods.
- BPE -> Creates subwords by merging frequently occurring character pairs.
- WordPiece -> Splits unknown words into smaller known pieces.
- SentencePiece -> Creates subword tokens directly from raw text and does not depend only on spaces.
