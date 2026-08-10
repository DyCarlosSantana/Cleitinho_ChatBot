<div align="center">

# 🤖 Cleitinho ChatBot

**Chatbot em Python com Groq API - do script de terminal à interface gráfica com voz.**

</div>

---

## Sobre o projeto

O **Cleitinho** é um assistente conversacional construído em cima da **Groq API** (modelo `llama-3.1-8b-instant`), desenvolvido como uma trilha de aprendizado incremental: cada módulo adiciona uma capacidade nova — histórico de conversa, personalidade, leitura de arquivos, saída estruturada, voz — até chegar numa aplicação desktop completa.

<p align="center">
  <img width="100%" alt="trilha_evolucao_chatbot" src="https://github.com/user-attachments/assets/0a25d642-527c-4bb5-b5cb-e33b64cc9113" />
</p>

---

## Como funciona

O núcleo do projeto é simples: a conversa é mantida como uma lista de mensagens (`role` + `content`) reenviada a cada turno para a API, o que dá memória de curto prazo ao assistente.

<p align="center">
  <img width="100%" alt="Fluxo de Funcionamento" src="https://github.com/user-attachments/assets/42536823-45f1-40a5-a6ff-aa2da9dad35f" />
</p>

---

## Estrutura do projeto

```
Cleitinho_ChatBot/
├── script_teste/            # Chamada mínima à API, sem estado
├── Exercicio_01/             # Loop de chat + histórico de mensagens
├── Exercicio_02/             # + personalidade via system prompt
├── Exercicio_03/             # + leitura de arquivo local como contexto
├── Exercicio_04/             # + extração de dados em JSON estruturado
├── Code_Captura_de_fala/     # + entrada por voz (speech-to-text)
└── Cleitinho - ChatBot/      # Aplicação final: GUI (CustomTkinter) + voz
    ├── __main__.py
    └── Interface.py
```

---

## Stack técnica

| Camada | Tecnologia |
|---|---|
| LLM / inferência | Groq API (`llama-3.1-8b-instant`) |
| Interface gráfica | CustomTkinter |
| Reconhecimento de voz | SpeechRecognition + PyAudio |
| Output de terminal | Rich |
| Variáveis de ambiente | python-dotenv |

---

## Como executar

```bash
# 1. Instale as dependências
pip install -r requirements.txt

# 2. Configure sua chave da Groq
cp .env.example .env
# edite o .env e insira sua GROQ_API_KEY

# 3. Rode a aplicação principal
cd "Cleitinho - ChatBot"
python __main__.py
```

Os módulos em `Exercicio_01` a `Exercicio_04` e `Code_Captura_de_fala` podem ser executados individualmente da mesma forma, e servem como registro da evolução do projeto.

---

## Interface (até o momento)

<p align="center">
  <img width="80%" alt="image" src="https://github.com/user-attachments/assets/a11e6de4-d64b-4f7e-acb1-45f82810e990" />
</p>

<p align="center"><i>Chat em texto e voz, histórico de conversa e resposta via Groq API em uma janela desktop.</i></p>

