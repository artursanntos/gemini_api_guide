# 🚀 Gemini API Passo-a-Passo – Rocket Lab

Este repositório contém um **notebook interativo** com os conceitos essenciais para utilizar a **API do Gemini**, a plataforma de modelos de linguagem da Google. O material foi preparado como suporte para os participantes do **Rocket Lab**.

## 📘 O que você vai encontrar

- 📌 Como obter e configurar sua chave de API
- 📌 Como fazer chamadas básicas para geração de texto
- 📌 Conceito de Roles, Instruções de Sistema e Parâmetros Configuráveis
- 📌 Janela de Contexto e Boas Práticas
- 📌 Output Estruturado
- 📌 Function Calling (Web Search e funções customizadas)
- 📌 Inputs multimodais
- 📌 Exemplos práticos com `google.generativeai` no Python
- 📌 Dicas de boas práticas para consumo da API

---

## 🧰 Pré-requisitos

Antes de executar o notebook, certifique-se de ter instalado:

```bash
pip install google-generativeai
```

Você também precisará de uma chave de API válida da Google. Acesse:

👉 https://ai.google.dev

Ou diretamente no Console para utilizar o Teste Grátis com U$300

👉 https://console.cloud.google.com/

Após conseguir a chave, garanta que está guardando-a em um lugar seguro.

## ▶️ Como usar
1. Abra o arquivo aqui e clique em "Open in Collab" para utilizá-lo via Google Collab.

Ou, caso deseje executar localmente,

1. Clone este repositório:

```bash
git clone https://github.com/seu-usuario/gemini-api-essentials.git
cd gemini-api-essentials
```
2. Abra o Jupyter Notebook:
```
jupyter notebook Gemini_API_Essentials.ipynb
```
Siga os passos indicados no notebook!

## 💸Limites de Uso de Modelos Gemini

| Modelo | RPM | RPD | TPM |
|---|---|---|---|
| Gemini 2.5 Pro | 5 | 100 | 250.000 |
| Gemini 2.5 Flash | 10 | 250 | 1.000.000 |
| Gemini 2.5 Flash-Lite | 15 | 1.000 | 1.000.000 |

*RPM = Requests Per Minute · RPD = Requests Per Day · TPM = Tokens Per Minute*
