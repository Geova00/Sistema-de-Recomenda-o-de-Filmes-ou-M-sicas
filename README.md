# Projeto Integrador III: Sistema de Recomendação Colaborativo

![Badge de Status](https://img.shields.io/badge/Status-Concluído-brightgreen)
![Badge de Linguagem](https://img.shields.io/badge/Linguagem-Python-blue)
![Badge de Modelo](https://img.shields.io/badge/Modelo-Filtro%20Colaborativo-orange)

## Objetivo do Projeto

Desenvolver um **Sistema de Recomendação Personalizado** de Filmes ou Músicas utilizando a técnica de **Filtro Colaborativo Baseado em Usuários (User-Based)**. O projeto visa aplicar e integrar conceitos das disciplinas de **Estrutura de Dados**, **Aprendizado Estatístico** e **Inteligência Computacional**.

O sistema gera sugestões ao identificar usuários com perfis de avaliação semelhantes e prever as notas de itens que o usuário-alvo ainda não viu.

## Fundamentação Acadêmica

O desenvolvimento do sistema está estritamente ligado às disciplinas do Projeto Integrador III:

| Disciplina | Conceitos Aplicados | Função no Sistema |
| :--- | :--- | :--- |
| **Estrutura de Dados** | Matrizes Esparsas (Pivot Table), Pandas DataFrames. | Organização de milhões de avaliações na forma de **Matriz Usuário x Item**. |
| **Aprendizado Estatístico** | Métrica **Similaridade de Cosseno**. | Cálculo estatístico para quantificar a semelhança entre os vetores de notas dos usuários. |
| **Inteligência Computacional** | **Filtro Colaborativo** (KNN). | Algoritmo que usa a similaridade para prever a nota de um item não visto, gerando a recomendação. |

## Tecnologias Utilizadas

* **Python:** Linguagem de programação central.
* **Pandas & NumPy:** Manipulação e suporte para operações matriciais.
* **Scikit-learn:** Implementação do modelo **KNN** e da métrica **Similaridade de Cosseno**.
* **Google Colab:** Ambiente de desenvolvimento e execução principal.

## Base de Dados

O sistema foi treinado e avaliado utilizando a base de dados real **MovieLens Latest Small (100k)**. Os dados são carregados diretamente através das URLs `raw` dos arquivos hospedados neste repositório:

* `ratings.csv` (Notas dos usuários).
* `movies.csv` (Títulos dos filmes).

## Como Executar o Projeto

O projeto é projetado para ser executado integralmente no **Google Colaboratory (Colab)**.

1.  **Acesse o Notebook:** [Link para o Notebook Colab] *(Substitua esta linha pelo link do seu Notebook)*

2.  **Carregamento dos Dados:** A Célula 3 do Notebook realiza o download automático dos arquivos CSV diretamente das URLs `raw` deste repositório, garantindo que o ambiente de execução esteja sempre atualizado.

3.  **Execução Sequencial:** Execute todas as células do Notebook sequencialmente para:
    * Carregar e Estruturar os Dados (Célula 3).
    * Treinar o Modelo e Gerar Recomendações (Célula 4).
    * Realizar a Validação de Desempenho (Holdout) (Célula 5).

## Resultados e Validação

A eficácia do modelo é validada por meio de duas etapas essenciais:

1.  **Geração de Recomendação (Teste Rápido):** A Célula 4 demonstra o funcionamento do filtro colaborativo em tempo real, gerando as 5 melhores sugestões para um usuário específico.

2.  **Teste Formal Holdout:** A Célula 5 executa um teste rigoroso, que separa 20% das avaliações do usuário para teste, e utiliza a métrica **Recall** para medir a proporção de acertos. Este teste formaliza a seção de Resultados, validando a precisão preditiva do sistema.

---
*Desenvolvido como parte dos requisitos do **Projeto Integrador III** - FATEC (2025).*
