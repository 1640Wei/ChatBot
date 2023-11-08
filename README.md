Hello, I am Wei. 💬
======

### Project Name: ChatBot-python

### Date: Nov 8, 2023

### Description:

### Technologies Used:
- **Python**:
- **Flask**:
- **jQuery**:
- **CSS**:
- **HTML**:
- **REST API**:
- **Bootstrap**:

### Project Structure:：
- `static`
  - `style.css`: Defining the appearance and style of elements on a webpage.
- `templates`
  - `chat.html`: Markup the content structure on the webpage, such as text, images, and links.
- `app.py`: It implements a conversational app based on the DialoGPT-medium model using the Flask framework and the Hugging Face transformers library.

### Example:


### Notice:
#### 1. Hugging Face - Transformers Library

1. **Load Pretrained Model**

- AutoTokenizer: This class handles the tokenization of the model, converting input into a format understandable by the model.

- AutoModelForCausalLM: This class, associated with the model, is responsible for loading and using the model.

```python
from transformers import AutoModelForCausalLM, AutoTokenizer

tokenizer = AutoTokenizer.from_pretrained("microsoft/DialoGPT-medium")
model = AutoModelForCausalLM.from_pretrained("microsoft/DialoGPT-medium")
```
2. **Process Model Input**

- Use the tokenizer to convert user input into a format the model can process. Here, the encode function is used, and the result is converted into a PyTorch tensor.

```python
new_user_input_ids = tokenizer.encode(str(text) + tokenizer.eos_token, return_tensors='pt')
```

3. **Perform Inference**

- Use the generate function for model inference, generating the model's response. Specify the maximum generation length and the end token's ID.
  
```python
chat_history_ids = model.generate(bot_input_ids, max_length=1000, pad_token_id=tokenizer.eos_token_id)
```

4. **Process Model Output**

- Use the decode function of the tokenizer to convert the model-generated tokens into human-readable text. Additionally, skip_special_tokens is used here to exclude special tokens from the generated output.

```python
tokenizer.decode(chat_history_ids[:, bot_input_ids.shape[-1]:][0], skip_special_tokens=True)
```

### Update Log:
- Version 1.0.0 (Nov 08, 2023)

***
### Thanks:

💬 I hope you enjoy this project! If you have any questions or suggestions, feel free to reach out at any time. 💬

✉️ HTY140226@gmail.com

