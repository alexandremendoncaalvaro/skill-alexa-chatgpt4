# Modelo de Skill Alexa para integrar o ChatGPT da OpenAI
Use o ChatGPT-4 na Alexa 😊  

# Instruções
- Crie uma conta e uma chave de autenticação de API na OpenAI: https://platform.openai.com/account/api-keys
    - Você terá direito a um trial gratuito de 3 meses (ou limite de $18).
    - Documentação: https://platform.openai.com/docs/api-reference/authentication

- Crie uma Skill Alexa-hosted (Python) na Alexa: https://developer.amazon.com/alexa/console/ask/create-new-skill
  - Name your Skill: Escolha um nome de sua preferência (Ex: ChatGPT)
  - Choose a primary locale: Portuguese (BR)  
  - Em tipo de experiência selecione: Other > Custom > Alexa-hosted (Python)  
  - Hosting region: Pode deixar o padrão (US East (N. Virginia))
  - Templates: Clique em Import Skill
  - Insira o endereço: https://github.com/alexandremendoncaalvaro/skill-alexa-chatgpt4.git

- Vá na aba "Code"
- Insira sua chave no código: lambda > lambda_function.py:
  ```python
  openai.api_key = "substitua-por-sua-api-key-da-openai"
  ```
- Salve as alterações

- Faça Build do Modelo e Deploy do Código.

- Seja feliz!