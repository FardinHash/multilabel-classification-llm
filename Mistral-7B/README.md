# As the model mistralai/Mistral-7B-v0.1 is restricted. You must be authenticated to access it. You need to add HuggingFace token
1. Go to *Hugging Face* and log into your account.
2. Navigate to the Settings tab and select Access Tokens.
3. Click New Token. Assign it the necessary scopes—usually, "read" is sufficient for downloading models.
4. Save this token somewhere secure.
5. Use this token in your notebook:
   ```
   import os
   
   # Set the token as an environment variable
    os.environ["HF_TOKEN"] = "your_token_here"
6. Or you can also explicitly pass the token to the *from_pretrained* method:
   ```
   tokenizer = AutoTokenizer.from_pretrained(model_name, use_auth_token="your_token_here")
