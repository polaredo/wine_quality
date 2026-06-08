# wine_quality
# 🍷 Analiza jakości wina czerwonego

## Opis danych
Zbiór danych pochodzi z serwisu Kaggle: [Wine Quality Dataset](https://www.kaggle.com/datasets/yasserh/wine-quality-dataset).  
Zawiera 1143 próbki czerwonego wina z 11 cechami fizykochemicznymi (m.in. zawartość alkoholu, kwasowość, siarczany) oraz zmienną docelową `quality` (skala 3–8).

## Cel analizy
Celem projektu jest zbadanie które składniki chemiczne wina mają największy wpływ na jego jakość oraz zbudowanie modelu predykcyjnego przewidującego ocenę jakości na podstawie parametrów fizykochemicznych.

## Modele
Zaimplementowano i porównano 3 modele regresji:
- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor (z Grid Search)

## Wyniki
| Model | RMSE |
|---|---|
| Regresja liniowa | ~0.64 |
| Drzewo decyzyjne | ~0.82 |
| **Random Forest** | **~0.62** |

Najlepszym modelem okazał się **Random Forest** (n_estimators=50, max_features=6).  
Najważniejsze cechy wpływające na jakość wina: **alkohol**, **siarczany**, **kwasowość lotna**.
