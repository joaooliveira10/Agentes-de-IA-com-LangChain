# 🤖 Agentes de IA com Python e LangChain 🐍

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![LangChain](https://img.shields.io/badge/LangChain-Latest-green)](https://langchain.readthedocs.io/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📖 Sobre o Projeto

Este repositório contém exemplos práticos de como construir e implementar agentes de IA utilizando Python e o framework LangChain. Os agentes de IA são sistemas que podem tomar decisões autônomas com base em objetivos definidos, utilizando modelos de linguagem de grande escala (LLMs) como seu "cérebro".

## ✨ Características

- 🧠 Implementação de agentes autônomos com LangChain
- 🔍 Exemplos de diferentes ferramentas e capacidades de agentes
- 🛠️ Código limpo e bem documentado
- 📊 Demonstrações práticas de casos de uso reais

## 🚀 Começando

### Pré-requisitos

- Python 3.8 ou superior
- pip (gerenciador de pacotes Python)
- Acesso a uma API de modelo de linguagem (OpenAI, HuggingFace, etc.)

### 📥 Instalação

```bash
# Clone o repositório
git clone https://github.com/joaooliveira10/agentes-ia-langchain.git
cd agentes-ia-langchain

# Crie um ambiente virtual
python -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate

# Instale as dependências
pip install -r requirements.txt
```

### 🔑 Configuração de API Keys

```python
# Crie um arquivo .env na raiz do projeto
OPENAI_API_KEY=sua_chave_api_aqui
# Outras chaves conforme necessário
```

## 📁 Estrutura do Projeto

- `agents/`: Implementações de diferentes tipos de agentes
- `tools/`: Ferramentas personalizadas para uso com agentes
- `examples/`: Exemplos completos de aplicações usando agentes
- `utils/`: Funções auxiliares e utilitários
- `notebooks/`: Jupyter notebooks com tutoriais passo a passo

## 📋 Descrição dos Arquivos

### 🤖 Agentes

- `simple_agent.py` - Implementação básica de um agente de conversação
- `react_agent.py` - Agente que utiliza o padrão ReAct (Reasoning and Acting)
- `plan_execute_agent.py` - Agente que planeja ações antes de executá-las

### 🛠️ Ferramentas

- `web_search.py` - Ferramenta para pesquisa na web
- `calculator.py` - Ferramenta para cálculos matemáticos
- `document_analyzer.py` - Ferramenta para análise de documentos

### 📘 Exemplos

- `qa_system.py` - Sistema de perguntas e respostas
- `research_assistant.py` - Assistente de pesquisa automatizado
- `data_analyst.py` - Análise de dados usando agentes

## 💡 Como Usar

### Exemplo Básico

```python
from langchain.agents import initialize_agent
from langchain.llms import OpenAI

# Inicializar o LLM
llm = OpenAI(temperature=0)

# Inicializar o agente com ferramentas
agent = initialize_agent(tools, llm, agent="zero-shot-react-description", verbose=True)

# Executar o agente
agent.run("Qual é a população atual do Brasil?")
```

### Exemplo Avançado

```python
# Carregar um agente personalizado
from agents.plan_execute_agent import PlanExecuteAgent
from tools.web_search import WebSearchTool

# Configurar ferramentas
tools = [WebSearchTool()]

# Inicializar agente
agent = PlanExecuteAgent(tools=tools, llm=llm)

# Executar uma tarefa complexa
result = agent.execute("Pesquise sobre os últimos avanços em IA generativa e crie um resumo dos três desenvolvimentos mais importantes.")
print(result)
```

## 📊 Exemplos de Casos de Uso

- 🔍 **Assistente de Pesquisa**: Automatize a coleta e análise de informações da web
- 📈 **Análise de Dados**: Use agentes para explorar e visualizar conjuntos de dados
- 📝 **Geração de Conteúdo**: Crie textos, resumos e relatórios automaticamente
- 🧪 **Automação de Processos**: Desenvolva fluxos de trabalho autônomos para tarefas repetitivas

## 🤝 Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests.

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova feature'`)
4. Push para a branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

---

⭐️ **Gostou do projeto? Deixe uma estrela!** ⭐️
