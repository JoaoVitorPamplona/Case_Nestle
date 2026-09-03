# Previsão de demanda semanal por tipo de café

Case técnico para Cientista de Dados Sênior — previsão de demanda em máquinas de café de autoatendimento.

## O problema

A máquina é reabastecida em rota fixa, sem visibilidade de demanda por produto. Falta produto é venda perdida. Sobra produto é capital parado. O objetivo é prever a demanda semanal de cada tipo de café e sugerir a quantidade de reposição com margem de segurança.

## A solução

Modelo linear misto (LMM) que aprende coeficientes comuns a todos os cafés e ajustes individuais por produto. Cafés com pouco histórico herdam a estrutura dos de alto giro. Testado contra ExtraTrees (individual e global), média móvel, Prophet e ARIMA(0,1,0) — vence em MAE, RMSE e WAPE.

## Estrutura

```
├── Case_cafe_nestle.ipynb   # notebook com a solução completa
├── apresentacao.pdf         # apresentação do case
├── requirements.txt         # dependências
└── README.md
```

## Como executar

1. Configurar credenciais do Kaggle (`~/.kaggle/kaggle.json`)

2. Instalar dependências:
```bash
pip install -r requirements.txt
```

3. Rodar o notebook de cima para baixo:
```bash
jupyter notebook Case_cafe_nestle.ipynb
```

O dataset é baixado automaticamente do Kaggle na primeira célula.

## Dependências

- Python 3.10+
- pandas, numpy, matplotlib
- scikit-learn
- statsmodels
- prophet
- kagglehub

## Autor

João Vitor Pamplona
