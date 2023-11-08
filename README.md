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

1.Load Pretrained Model

- AutoTokenizer: This class handles the tokenization of the model, converting input into a format understandable by the model.

- AutoModelForCausalLM: This class, associated with the model, is responsible for loading and using the model.

```python
from transformers import AutoModelForCausalLM, AutoTokenizer

tokenizer = AutoTokenizer.from_pretrained("microsoft/DialoGPT-medium")
model = AutoModelForCausalLM.from_pretrained("microsoft/DialoGPT-medium")
```


### Update Log:
- Version 1.0.0 (Nov 08, 2023)

***
### Thanks:

💬 I hope you enjoy this project! If you have any questions or suggestions, feel free to reach out at any time. 💬

✉️ HTY140226@gmail.com

