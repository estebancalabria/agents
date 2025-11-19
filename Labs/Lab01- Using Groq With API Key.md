# LAB - Using Groq With API Key

* Sacar una API key de Groq
* Crear un colab nuevo
* Ingresar el siguiente codigo

```python
  api_key = input("Ingrese su Api Key")
  prompt =  input("Ingrese su prompt")
  
  from openai import OpenAI
  import os
  client = OpenAI(
      api_key=api_key,
      base_url="https://api.groq.com/openai/v1",
  )
  
  response = client.responses.create(
      input=prompt,
      model="openai/gpt-oss-20b",
  )
  print(response.output_text)
```
