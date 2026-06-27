# 💳 Credit Scoring sob Desbalanceamento Severo

Repositório destinado ao projeto final da disciplina de Reconhecimento de Padrões (PPGCC21).
Este projeto implementa um pipeline de *Machine Learning* fim-a-fim para análise de risco de crédito, enfrentando problemas de modelagem longitudinal (*Vintage Analysis*), imputação semântica (MNAR) e classificação sob extremo desbalanceamento de classes.

**Autor:** Caio Henrique Barreto Costa  
**Instituição:** Universidade Tecnológica Federal do Paraná (UTFPR) - Programa de Pós-Graduação em Ciência da Computação (PPGCC)

---

## 🎯 Objetivo do Projeto
Avaliar algoritmos de classificação binária (*Random Forest*, *XGBoost* e *Rede Neural MLP*) na predição de inadimplência (maus pagadores). Devido ao desbalanceamento massivo da base de dados ($\approx 2\%$ de classe positiva), as métricas globais como Acurácia foram descartadas em favor da **Área sob a Curva Precision-Recall (AUC-PR)**. O ganho de generalização foi validado estatisticamente pelo Teste Não-Paramétrico de Wilcoxon.

---

## 📁 Conjunto de Dados
Os dados originais foram extraídos da base *Credit Card Approval Prediction* via Kaggle.
Devido a restrições de tamanho, as bases originais não estão versionadas neste repositório. Para reproduzir os testes, efetue o download dos ficheiros abaixo e coloque-os na mesma diretoria do notebook:
- `application_record.csv` (Dados Demográficos)
- `credit_record.csv` (Série Temporal de Pagamentos)

> **Link para Download:** [Kaggle - Credit Card Approval Prediction](https://www.kaggle.com/rikdifos/credit-card-approval-prediction)

---

## 🛠️ Tecnologias e Dependências

A execução do pipeline computacional requer **Python 3.10+** e as seguintes bibliotecas:

```bash
# Bibliotecas Core
pip install pandas numpy scipy matplotlib seaborn

# Bibliotecas de Machine Learning e Modelagem
pip install scikit-learn xgboost

# Bibliotecas para Tratamento de Cardinalidade e Desbalanceamento
pip install category_encoders imbalanced-learn
