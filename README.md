# 🎓 Análise de Engajamento e Desempenho de Alunos - Open University

Este projeto foi desenvolvido como **projeto final** para o curso de **Python para Data Science** e utiliza o **dataset público da Open University** para realizar uma análise completa sobre o engajamento e o desempenho dos alunos no Ambiente Virtual de Aprendizagem (**VLE - Virtual Learning Environment**).

O objetivo principal é explorar os dados demográficos, analisar a interação dos alunos com a plataforma, identificar fatores que influenciam o sucesso acadêmico e construir um modelo de Machine Learning para prever a probabilidade de aprovação de um aluno.

---

## ▶️ Como Executar no Google Colab

Antes de abrir o notebook no Colab, **faça o download dos arquivos de dados** disponíveis neste link:

👉 [Baixar arquivos do Google Drive](https://drive.google.com/drive/folders/1pUQCxPj76qyrXrU3YhrzDVuFuW7kwXSo?usp=sharing)

Em seguida, abra o notebook no Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1PlLEMSQORYXghT9JbP4IMlL8UX3Ih-Lu?usp=sharing)

> Após abrir o notebook, faça upload dos arquivos baixados para a área de arquivos do Colab.

---

## 📊 Visão Geral da Análise

A análise segue um **pipeline de dados estruturado em camadas** (Bronze, Prata e Ouro) e explora diversas áreas:

### 🔹 Análise Exploratória de Dados

- **Perfil Geral dos Alunos:** Distribuição dos resultados finais, participação por região, índice de pobreza (`imd_band`) e número total de alunos com deficiência.  
- **Engajamento com o VLE:** Quantidade de cliques e interações ao longo do tempo, identificando picos de atividade, especialmente em períodos de avaliação.  
- **Comparação (Aprovados vs. Reprovados):** Segmentação dos alunos entre sucesso (`Pass/Distinction`) e insucesso (`Fail/Withdrawn`) para comparar fatores como gênero, região, índice de pobreza e tentativas anteriores.

### 🔹 Machine Learning

- Modelo **Random Forest** para classificar alunos em **sucesso** ou **não-sucesso**.  
- Utiliza a **matriz de cliques dos alunos** como principal recurso para prever o resultado final.

---

## 💡 Principais Insights

- Alunos de regiões com mais de 50% de pobreza tiveram mais aprovados que reprovados.  
- Cliques próximos à avaliação aumentam significativamente, principalmente entre aprovados.  
- A região da **Irlanda** apresentou mais aprovados, apesar de menor participação, sendo a região com menor índice de pobreza.  
- Cliques no segundo semestre do ano tendem a ser maiores, devido a cursos iniciados em julho.  
- Mais alunas foram aprovadas do que alunos, embora haja mais alunos no total.  
- Entre os alunos que não tiveram sucesso, a maioria desistiu do curso.  
- O modelo Random Forest tende a acertar mais alunos aprovados, refletindo na acurácia.

---

## 🛠️ Tecnologias Utilizadas

- **Python** → Linguagem de programação principal  
- **Pandas & NumPy** → Manipulação e análise de dados  
- **Matplotlib & Seaborn** → Visualização dos dados  
- **Scikit-learn** → Construção do modelo de Machine Learning  
- **SQLAlchemy & SQLite** → Armazenamento dos dados (simulando um lakehouse)  
- **Google Colab** → Ambiente de desenvolvimento e apresentação

---

## 📂 Estrutura do Projeto

- `pipeline_vle_open_university_projeto_final.ipynb` → Notebook Google Colab com código, análises e visualizações  
- `studentAssessment.csv` → Dados de avaliações  
- `studentInfo.csv` → Dados demográficos dos alunos  
- `studentRegistration.csv` → Registro de matrícula dos alunos  
- `studentVle.csv` → Interações dos alunos com o VLE

