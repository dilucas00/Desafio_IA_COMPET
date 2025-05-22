# Predição de Nível de Experiência de Membros de Academia 🏋️‍♂️

Este projeto utiliza técnicas de machine learning para prever o **nível de experiência** (Beginner, Intermediate ou Advanced) de um membro de academia com base em características fisiológicas e hábitos de treino.

Motivação da escolha do projeto: Escolhi esse dataset porque tenho grande interesse pela área de academias e treinamento físico. Embora não tenha concluído minha primeira graduação em Educação Física, sempre tive afinidade com o tema e continuo acompanhando o assunto por interesse pessoal. Essa conexão com a área motivou minha escolha por um projeto que une saúde, exercício e ciência de dados.

## 📁 Dataset

O dataset utilizado é `gym_members_exercise_tracking.csv` contendo informações como:

- Idade  
- Sexo  
- Peso e altura  
- BPM médio e de repouso  
- Frequência de treino semanal  
- Duração média das sessões  
- Ingestão de água diária  
- Nível de experiência (alvo)

> Apenas 10 variáveis foram utilizadas conforme especificado no desafio.

---

## 🧪 Objetivo

Desenvolver um modelo de classificação que, a partir de dados inseridos por um usuário, retorne seu provável nível de experiência na academia.

---

## 📊 Etapas do projeto

### ✅ Nível I – Preparação e Modelagem

1. Carregamento e renomeação das colunas para português  
2. Imputação de valores ausentes (mediana)  
3. Codificação de variáveis categóricas (`LabelEncoder`)  
4. Separação treino/teste  
5. Treinamento de dois modelos:
   - Regressão Logística  
   - Random Forest  
6. Avaliação por acurácia e classification report

### ✅ Nível II – Avaliação Estendida e Interface

7. Avaliação em 30 execuções com random_state variável  
8. Cálculo da média e desvio-padrão da acurácia  
9. Salvamento do melhor modelo com `pickle`  
10. Criação de uma interface Gradio para entrada de dados

---

## 💡 Tecnologias utilizadas

- Python 3.11+  
- Pandas, NumPy  
- Scikit-learn  
- Gradio  
- Jupyter Notebook

---

## 🚀 Como usar

1. Clone o repositório  
2. Crie o ambiente virtual:

   ```bash
   python -m venv .venv
   source .venv/bin/activate  # ou .venv\Scripts\activate no Windows
   pip install -r requirements.txt


💬 Exemplo de entrada na interface
Idade: 28

Peso: 75

Altura: 1.78

BPM médio: 130

BPM repouso: 60

Duração sessão: 1.5

Frequência semanal: 6

Ingestão de água: 2.5

Sexo: Masculino

Resultado esperado: Advanced



📦 Arquivos gerados
melhor_modelo_gym.pkl: modelo treinado com melhor desempenho
