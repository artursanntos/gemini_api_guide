# 🚀 Gemini API Passo-a-Passo – Rocket Lab

Notebook interativo com os conceitos essenciais para consumir a **API do Gemini**. Material de apoio do **Rocket Lab**.

## 📘 O que você vai encontrar

- 📌 Como obter e configurar sua chave de API
- 📌 Primeira chamada e anatomia da resposta (incluindo custo em tokens)
- 📌 Roles, System Instruction e parâmetros de geração
- 📌 **A API é stateless** — como montar o histórico de uma conversa
- 📌 Janela de contexto e boas práticas de prompt
- 📌 Output estruturado com Pydantic
- 📌 Function Calling (Google Search e ferramentas customizadas), com o ciclo completo
- 📌 Inputs multimodais (apêndice)

---

## 🧰 Pré-requisitos

```bash
pip install google-genai
```

E uma chave de API do Google AI Studio — **gratuita e sem cartão de crédito**:

👉 https://aistudio.google.com/apikey

Guarde a chave num arquivo `.env` e coloque o `.env` no `.gitignore`. Nunca commite uma chave.

## ▶️ Como usar

**No Google Colab (recomendado para a aula):** abra o notebook por aqui e clique em *Open in Colab*. Cadastre a chave em 🔑 → *Adicionar novo secret*, com o nome `GOOGLE_API_KEY`, e ative *Acesso ao notebook*.

**Localmente:**

```bash
git clone https://github.com/artursanntos/gemini_api_guide.git
cd gemini_api_guide
export GOOGLE_API_KEY="sua-chave"
jupyter notebook "Criação_de_Comunicação_com_LLM.ipynb"
```

## 🤖 Modelo usado

O notebook roda em **`gemini-3.1-flash-lite`**: é o modelo mais barato com free tier e o que o Google indica para projetos novos.

> ⚠️ Os modelos da família **2.5 estão com acesso restrito** a contas que já os usavam. Se você criou sua chave agora, `gemini-2.5-flash-lite` provavelmente vai falhar com 404. Use o modelo acima.

## 💸 Limites de uso

Os limites do free tier (RPM, TPM, RPD) variam por modelo e mudam com o tempo. Consulte os **seus** limites ao vivo em:

👉 https://aistudio.google.com/rate-limit

Se tomar **429** (`RESOURCE_EXHAUSTED`), espere ~30s. O notebook traz um helper de retry com backoff na seção de setup.

## 🔁 Se a API do Google ficar instável

Erros **503** (`UNAVAILABLE`) acontecem quando o modelo está sobrecarregado no Google, não é a sua chave. Duas saídas:

1. Troque o `MODEL` no topo do notebook para `gemini-3.5-flash-lite` ou outro. É outra fila de capacidade.
2. Troque de provedor. Serviços como o **OpenRouter** expõem uma API compatível com o formato da OpenAI — o mesmo da seção *Formato compatível com a OpenAI* deste notebook. Na prática você troca `base_url` e `api_key` e o resto do código continua igual.

## 🔗 Referências

- [Documentação da API](https://ai.google.dev/api?hl=pt-br&lang=python)
- [Estratégias de prompting](https://ai.google.dev/gemini-api/docs/prompting-strategies)
- [Structured Output](https://ai.google.dev/gemini-api/docs/structured-output)
- [Function Calling](https://ai.google.dev/gemini-api/docs/function-calling)
- [Grounding](https://ai.google.dev/gemini-api/docs/grounding?lang=python)
