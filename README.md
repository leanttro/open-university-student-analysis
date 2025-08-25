# 🎓 Análise de Engajamento e Desempenho de Alunos - Open University

Este projeto foi desenvolvido como **projeto final** para o curso de **Python para Data Science do SENAI** e utiliza o **dataset público da Open University** para realizar uma análise completa sobre o engajamento e o desempenho dos alunos no Ambiente Virtual de Aprendizagem (**VLE - Virtual Learning Environment**).

O objetivo principal é explorar os dados demográficos, analisar a interação dos alunos com a plataforma, identificar fatores que influenciam o sucesso acadêmico e construir um modelo de Machine Learning para prever a probabilidade de aprovação de um aluno.

---

## ▶️ Como Executar no Google Colab

Você pode abrir e executar o projeto diretamente no Google Colab clicando no link abaixo:

👉 [Abrir no Google Colab](https://colab.research.google.com/drive/1PlLEMSQORYXghT9JbP4IMlL8UX3Ih-Lu?usp=sharing)

> Obs: Para execução completa do notebook, faça o upload dos seguintes arquivos para a área de arquivos do Colab:
>
> - `studentAssessment.csv`
> - `studentInfo.csv`
> - `studentRegistration.csv`
> - `studentVle.csv`

---

## 📊 Visão Geral da Análise

A análise segue um **pipeline de dados estruturado em camadas** (Bronze, Prata e Ouro) e explora diversas áreas:

### 🔹 Análise Exploratória de Dados

- **Perfil Geral dos Alunos:** Investigação sobre a distribuição dos resultados finais, participação por região, índice de pobreza (`imd_band`), e o número total de alunos com deficiência.
- **Engajamento com o VLE:** Análise da quantidade de cliques e interações dos alunos com a plataforma ao longo do tempo, identificando picos de atividade, especialmente em períodos de avaliação.
- **Análise Comparativa (Aprovados vs. Reprovados):** Uma análise detalhada que segmenta os alunos entre sucesso (`Aprovados/Distinção`) e insucesso (`Reprovados/Desistentes`) para comparar fatores como gênero, região, índice de pobreza e número de tentativas anteriores.

### 🔹 Machine Learning

- Foi desenvolvido um modelo com **Random Forest** para classificar os alunos em duas categorias: sucesso (`Pass/Distinction`) ou não-sucesso (`Fail/Withdrawn`).
- O modelo utiliza a **matriz de cliques dos alunos** como principal recurso para prever o resultado final.

---

## 💡 Principais Insights

- O número de alunos aprovados em regiões com mais de 50% de pobreza é maior do que o número de reprovados nessas mesmas regiões.
- O número de cliques próximo à avaliação aumenta consideravelmente em todas as categorias de resultado final, mas é ainda maior entre os alunos aprovados.
- Apesar de a região da **Irlanda** ter menos participantes do que a North Region, ela apresentou um número maior de aprovados. Vale destacar que também é a região com o menor índice de pobreza entre todas.
- O número de cliques no segundo semestre do ano tende a ser maior do que no começo do ano, o que pode ser explicado por cursos que iniciam a partir de julho.
- O número de alunas aprovadas é maior do que o de alunos aprovados, embora o total de alunos seja maior do que o total de alunas.
- Entre os alunos que não tiveram sucesso, a grande maioria desistiu do curso, em vez de ser reprovada por desempenho.
- Como o número de aprovados é maior que o de reprovados, o modelo de Machine Learning (Random Forest) tende a acertar mais os aprovados. Isso explica por que a acurácia para aprovados apresenta um valor mais alto.

---

## 🛠️ Tecnologias Utilizadas

- **Python** → Linguagem de programação principal.
- **Pandas & NumPy** → Manipulação e análise de dados.
- **Matplotlib & Seaborn** → Visualização dos dados.
- **Scikit-learn** → Construção do modelo de Machine Learning.
- **SQLAlchemy & SQLite** → Armazenamento dos dados em um banco de dados local (simulando um lakehouse).
- **Google Colab** → Ambiente de desenvolvimento e apresentação da análise.

---

## 📂 Estrutura do Projeto

- `pipeline_vle_open_university_projeto_final.ipynb` → Google Colab com todo o código, análises e visualizações.
- `studentAssessment.csv` → Dados de avaliações.
- `studentInfo.csv` → Dados demográficos dos alunos.
- `studentRegistration.csv` → Registro de matrícula dos alunos.
- `studentVle.csv` → Interações dos alunos com o VLE.
