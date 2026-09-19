# 📚 Miniguia de Estudos: Arquitetura de Software e IA com NotebookLM

Este repositório foi desenvolvido para o Desafio de Projeto da [DIO (Digital Innovation One)](https://www.dio.me/). O objetivo do projeto é demonstrar a aplicação prática do **NotebookLM** e da **Engenharia de Prompts** como ferramentas de aprendizagem ativa, curadoria de conteúdo técnico e documentação estruturada.

---

## 🎯 1. Contexto e Objetivos

### 💡 Tema Escolhido
**Arquitetura de Software, Boas Práticas de Código e Engenharia de Prompts para IA**

### 🎯 Objetivos de Aprendizado
- Centralizar fontes oficiais e confiáveis de documentação técnica em um único caderno do NotebookLM.
- Desenvolver o pensamento crítico ao sintetizar conceitos de arquitetura com boas práticas de código.
- Aplicar técnicas de **Engenharia de Prompts** para extrair respostas precisas e evitar "alucinações" do modelo.
- Documentar o processo de aprendizado, incluindo os testes e correções de problemas (*troubleshooting*).

---

## 📂 2. Curadoria de Fontes Selecionadas

As seguintes fontes oficiais foram carregadas no caderno do NotebookLM para formar a base de conhecimento do projeto:

1. 🌐 **[Martin Fowler - Software Architecture Guide](https://martinfowler.com/architecture/)**: Conceitos essenciais e definições sobre arquitetura de software moderna.
2. 🌐 **[12-Factor App Methodology (PT-BR)](https://12factor.net/pt_br/)**: Doze fatores para construção de aplicações prontas para ambiente Cloud/SaaS.
3. 🌐 **[PEP 8 -- Style Guide for Python Code](https://peps.python.org/pep-0008/)**: Guia oficial de estilo, convenções de código e legibilidade em Python.
4. 🌐 **[Google AI - Prompting Strategies Guide](https://ai.google.dev/gemini-api/docs/prompting-strategies)**: Boas práticas e estratégias avançadas de engenharia de prompts.

---

## 🧪 3. Engenharia de Prompts e "Cicatrizes" (Troubleshooting)

Nesta etapa, documentamos os testes de perguntas, a evolução da escrita dos prompts e a resolução de dificuldades encontradas no processo de extração.

### 🔄 Teste 1: Síntese e Comparação Técnica
- **Prompt Inicial (Ambíguo):**  
  `"Me explica o que é Clean Code e o 12-Factor App."`
- **Resultado Obtido:** A resposta foi genérica, sem relacionar os dois conceitos diretamente com as fontes carregadas no caderno.
- **Prompt Refinado (Estratégico):**  
  `"Atuando como um Arquiteto de Software Sênior, analise as fontes sobre PEP 8 e 12-Factor App. Crie uma tabela comparando boas práticas no nível de código (micro) versus boas práticas de arquitetura em nuvem (macro). Baseie-se apenas nas fontes do caderno."`
- **Resultado:** A IA gerou um quadro comparativo preciso, citando trechos das documentações e separando conceitos de legibilidade de código de decisões de infraestrutura.

### ⚠️ Cicatriz / Aprendizado (*Troubleshooting*)
- **Problema:** Quando questionada sobre "segurança em contêineres Docker", a IA trouxe explicações externas que não constavam nos materiais adicionados.
- **Causa:** O escopo do prompt permitiu que o modelo buscasse conhecimentos gerais da sua base original em vez de se limitar ao acervo.
- **Solução:** Inclusão de uma trava no prompt:  
  `"Responda EXCLUSIVAMENTE com base nas fontes fornecidas neste caderno. Caso o assunto não seja abordado em nenhuma das fontes, informe explicitamente que o material não contém essa informação."`

---

## 📖 4. Miniguia de Estudo (Entrega Final)

### 📌 Resumos Estruturados do Assunto
1. **Arquitetura de Software:** Não se resume a diagramas, mas sim às decisões de design mais difíceis de alterar ao longo do ciclo de vida do sistema.
2. **Boas Práticas de Código (PEP 8):** A legibilidade do código é prioritária. Convenções claras de nomenclatura, espaçamento e estrutura facilitam a manutenção do software.
3. **Aplicações 12-Factor:** Estabelecem padrões para que sistemas funcionem de forma isolada, escalável e independente do ambiente onde são executados.

---

### 📖 Glossário de Conceitos Fundamentais

| Conceito | Definição Rápida |
| :--- | :--- |
| **Grounding (Ancoragem)** | Restringir as respostas da IA estritamente ao conjunto de documentos fornecido. |
| **PEP 8** | Documento oficial da comunidade Python que define o padrão de formatação de código. |
| **12-Factor App** | Conjunto de 12 princípios universais para desenvolvimento de softwares na nuvem. |
| **Troubleshooting** | Diagnóstico sistemático e resolução de falhas ou comportamentos inesperados. |

---

## 🤖 5. Banco de Prompts Reutilizáveis para Estudos

Abaixo estão prompts modelos configurados para apoiar futuras revisões de conteúdo:

```markdown
1. Explicativo por Analogia:
"Explique o conceito de [CONCEITO] para um desenvolvedor iniciante, utilizando uma analogia simples do dia a dia baseada nas fontes fornecidas."

2. Resumo Executivo:
"Sintetize o documento [NOME_DO_DOCUMENTO] em 5 tópicos (bullet points) principais, destacando os pontos de atenção para arquitetura."

3. Quiz de Fixação:
"Com base no material do caderno, crie 3 perguntas de múltipla escolha sobre [TEMA] com gabarito comentado ao final."
