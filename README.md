# Top 10 Criptomonedas por Market Cap

Análisis exploratorio de datos sobre el **tamaño, la liquidez y la estructura del mercado cripto**, usando datos en vivo de la API de CoinGecko.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/TU_USUARIO/TU_REPO/blob/main/top10_criptomonedas_market_cap.ipynb)

## Objetivo

Entender cómo se distribuye el tamaño del mercado entre las 10 criptomonedas más grandes, qué monedas concentran más actividad de trading en relación a su tamaño y qué rol cumplen las stablecoins dentro del ecosistema.

## Preguntas que responde

1. ¿Qué tan concentrado está el mercado en Bitcoin?
2. ¿Tamaño de mercado es lo mismo que actividad de trading?
3. ¿Cómo se reparte el market cap entre las principales monedas?
4. ¿Qué moneda se negocia más en relación a su tamaño? (ratio volumen / market cap)
5. ¿Qué rol cumplen las stablecoins (USDT, USDC) frente al resto?

## Hallazgos principales

En la foto analizada en el informe original:

- Bitcoin concentra el **70,1%** del market cap del top 10 y, junto con Ethereum, cerca del **80%**.
- Tether mueve más volumen diario que Bitcoin a pesar de tener un market cap mucho menor.
- Bitcoin tiene uno de los ratios de liquidez relativa más bajos: se comporta más como reserva de valor que como activo de trading frecuente.
- Las stablecoins son una fracción menor del market cap pero concentran cerca de la mitad del volumen operado: funcionan como "puente" del ecosistema.

> Los datos se descargan en vivo, así que al ejecutar el notebook los números van a diferir de los del informe. Las conclusiones del notebook se recalculan automáticamente.

## Visualizaciones

- Market cap por moneda en escala logarítmica
- Dispersión market cap vs. volumen (ejes logarítmicos)
- Participación en el market cap (top 5 + "Otros")
- Liquidez relativa por moneda (stablecoins resaltadas)
- Stablecoins vs. resto: market cap y volumen

## Cómo ejecutarlo

**En Google Colab (recomendado):** hacé clic en el botón "Open in Colab" de arriba y ejecutá todo con *Entorno de ejecución → Ejecutar todo*.

**En local:**

```bash
git clone https://github.com/TU_USUARIO/TU_REPO.git
cd TU_REPO
pip install requests pandas numpy matplotlib jupyter
jupyter notebook top10_criptomonedas_market_cap.ipynb
```

## Estructura

```
.
├── top10_criptomonedas_market_cap.ipynb   # análisis completo
├── top10_cripto.csv                       # foto de datos (se genera al ejecutar)
└── README.md
```

## Stack

Python · pandas · NumPy · matplotlib · CoinGecko API

## Datos

Fuente: [CoinGecko API](https://www.coingecko.com/en/api) (endpoint `/coins/markets`, sin API key). Si la API no responde o limita las consultas, el notebook usa la copia local `top10_cripto.csv`.

## Autor

**Lorenzo Ciprés** · proyecto de portfolio de ciencia de datos.# Top_10_criptomonedas_DataAnalisis
