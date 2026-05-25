#Projeto ETL: Enriquecimento de Dados Bancários com IA Generativa

Este projeto foi desenvolvido como parte de um desafio prático da **DIO**, com foco na construção de um pipeline de **ETL (Extract, Transform, Load)** aplicado a um cenário bancário.

A proposta consiste em extrair dados de clientes, processá-los com apoio de Inteligência Artificial Generativa e gerar uma nova base de dados enriquecida com mensagens personalizadas.

---

#Sobre o Projeto

O desafio original utilizava uma API pública para realizar operações de leitura e atualização de dados. Como a API deixou de funcionar, o projeto foi adaptado para trabalhar com arquivos locais, mantendo toda a lógica do processo ETL.

Em vez de consumir endpoints externos, os dados passaram a ser manipulados diretamente com **Pandas**, permitindo que o fluxo continuasse funcional e mais simples de reproduzir.

Essa adaptação também serviu para reforçar conceitos importantes de engenharia de dados, como tratamento de erros, flexibilidade do pipeline e continuidade do processamento mesmo em cenários de falha.

---

#Estrutura do Pipeline ETL

## 1. Extração (Extract)

Os dados dos clientes bancários são carregados a partir do arquivo `SDW2023.csv` utilizando a biblioteca **Pandas**.

As informações são organizadas em estruturas manipuláveis no Python, contendo dados como:

* Nome do cliente
* Número da conta
* Limites bancários
* Informações financeiras simuladas

---

## 2. Transformação (Transform)

Na etapa de transformação, o projeto utiliza a API da OpenAI para gerar mensagens personalizadas de marketing bancário.

A IA interpreta os dados do cliente e cria sugestões voltadas para investimentos e relacionamento financeiro.

Exemplo de transformação:

* Entrada: nome e perfil do cliente
* Saída: mensagem personalizada gerada por IA

O código também possui tratamento de exceções para garantir maior robustez do pipeline. Caso a chave da API da OpenAI não seja informada, o sistema continua funcionando normalmente utilizando mensagens padrão como fallback.

---

## 3. Carregamento (Load)

Após o enriquecimento dos dados, o resultado final é salvo no arquivo:

```bash
SDW2023_Atualizado.json
```

Esse arquivo representa a etapa de carregamento do pipeline, simulando a persistência dos dados em uma base NoSQL.

---

#Tecnologias Utilizadas

* Python
* Pandas
* OpenAI API
* Google Colab

---

#Como Executar

1. Clone este repositório ou faça o download do notebook `.ipynb`
2. Abra o projeto no Google Colab
3. Faça upload do arquivo `SDW2023.csv`
4. Execute as células em sequência
5. Informe sua API Key da OpenAI quando solicitado

   * Ou apenas pressione `Enter` para executar o modo fallback
6. Ao final da execução, o arquivo `SDW2023_Atualizado.json` será gerado automaticamente

---

# Estrutura dos Arquivos

```bash
📁 projeto-etl
 ├── SDW2023.csv
 ├── SDW2023_Atualizado.json
 ├── projeto_etl.ipynb
 └── README.md
```

---

#Objetivos do Projeto

* Aplicar conceitos de ETL na prática
* Trabalhar com manipulação de dados utilizando Pandas
* Integrar IA Generativa em pipelines de dados
* Desenvolver resiliência e tratamento de falhas
* Simular enriquecimento de dados em ambiente bancário

---

# Autor

**Mateus Rodrigues de Oliveira**
Implementador e entusiasta de Ciência de Dados, IA e Análise de Dados.
