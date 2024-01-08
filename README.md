# Modelo de Skill Alexa para integrar o ChatGPT da OpenAI
Use o ChatGPT-4 na Alexa 😊  

# Instruções
- Crie uma conta e uma chave de autenticação de API na OpenAI: https://platform.openai.com/account/api-keys
- Coloque crédito pra poder usar a API: https://platform.openai.com/account/billing/overview
> *IMPORTANTE: a API e o ChatGPT Plus são coisas diferentes, a assinatura do ChatGPT Plus não te dá acesso a API.

A API é paga por uso, ou seja por cada pergunta e resposta é cobrado alguns centavos ([veja aqui](https://openai.com/pricing)). O valor varia de acordo com o modelo selecionado.

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
- Modifique no mesmo arquivo (lambda_function.py) pro modelo de sua preferência:
  ```python
  MODEL = "gpt-4"
  ```
  Exemplos: "gpt-3.5-turbo", "gpt-4", "gpt-4-1106-preview"  
  [veja a lista completa de modelos aqui](https://platform.openai.com/docs/models)

- Salve as alterações

- Faça Build do Modelo e Deploy do Código.

- Seja feliz!