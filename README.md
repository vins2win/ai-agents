# ai-agents
AI agents

To use the document translator, you would:

1. Save the entire Python code I provided into a file (let's call it `translator.py`)
2. Install the required dependencies:
   ```
   pip install transformers langchain python-docx openai
   ```
3. Set your OpenAI API key as an environment variable:
   ```
   export OPENAI_API_KEY=your_api_key_here  # on Linux/Mac
   # or
   set OPENAI_API_KEY=your_api_key_here  # on Windows
   ```
4. Make sure you have a Word document named 'sample.docx' in the same directory as your script
5. Run the script:
   ```
   python translator.py
   ```

The script already includes this example in the `if __name__ == "__main__":` block:

```python
# Example: Translate a document to German
result = process_user_request("Please translate the document 'sample.docx' to German and save it as a new file.")
print(result)
```

When you run the script, it will:
1. Load the document 'sample.docx'
2. Translate its content to German (the default target language)
3. Save the translated document as 'sample_de.docx' in the same directory
4. Print the result of the operation




How to Use This API-Free Translator
This simplified version only requires installing two packages:
```python
pip install transformers python-docx
```
To use it:

Save the code to a file (e.g., translator_no_api.py)
Run it with a command like:
```python
python translator_no_api.py your_document.docx --language spanish
```
This will:

Load the document
Translate it to your chosen language
Save it as a new file with the language code appended

The first time you run it, it will download the translation model from Hugging Face (this happens automatically and is free).
Important Notes

This version doesn't have the conversational agent capabilities of the original, but provides the core translation functionality
No API key or internet connection is needed after the initial model download
Translation quality may not be as high as with paid API services, but it's completely free
The models are downloaded to your local machine, so ensure you have enough disk space (~500MB per language model)

