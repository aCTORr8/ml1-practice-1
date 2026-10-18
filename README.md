# Практичне завдання №1 — лінійна регресія

**Виконав:** Новак Сергій, ФЕІ-43с

Практична робота з курсу машинного навчання на наборі даних Ames Housing.
Цільова змінна — `SalePrice`.

## Файли

- `practice_1_solution.ipynb` — виконане практичне завдання;
- `data/ames_housing.csv` — набір даних;
- `requirements.txt` — Python-залежності.

## Реалізовано

- дослідницький аналіз даних та аналіз пропусків;
- розбиття на Train, Validation і Test у пропорції 70/15/15;
- відбір числових та категоріальних ознак тільки на Train;
- заповнення пропусків, One-Hot Encoding і стандартизація;
- лінійна регресія та обчислення градієнтів засобами NumPy;
- Batch GD, SGD та Mini-batch GD;
- підбір learning rate за Validation;
- оцінювання за R², RMSE та MAE;
- аналіз залишків і перевірка мультиколінеарності за VIF;
- вплив мультиколінеарності на стабільність коефіцієнтів (bootstrap);
- порівняння навчання з масштабуванням і без нього (експеримент A).

## Запуск

Потрібен Python 3.9 або новіший. Команди виконуються з кореня репозиторію.

```bash
python -m pip install -r requirements.txt
jupyter notebook
```

Після запуску Jupyter потрібно відкрити `practice_1_solution.ipynb` і виконати
всі клітинки послідовно. У notebook використовується `random_state=42`, тому
розбиття даних і результати відтворюються.

## Результати

Найкращим за Validation R² став Batch Gradient Descent.

| Метрика на Test | Значення |
|---|---:|
| R² | 0.8197 |
| RMSE | $37 038 |
| MAE | $21 887 |

## Джерело даних

[House Prices — Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data)
