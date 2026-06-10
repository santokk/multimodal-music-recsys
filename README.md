# Курсовая: Мультимодальные эмбеддинги в рекомендательных системах

Магистерская курсовая работа (1 курс). Исследование применения мультимодальных эмбеддингов (текст + изображение + аудио) для рекомендации музыкальных треков, с фокусом на **холодный старт новых треков**.

## Быстрый старт

```bash
jupyter notebook workshop.ipynb          # 1. Парсинг датасета
jupyter notebook 02_embeddings.ipynb     # 2. Эмбеддинги
jupyter notebook 03_fusion.ipynb         # 3. Fusion
jupyter notebook 04_recsys_eval.ipynb      # 4. Evaluation
jupyter notebook 05_compute.ipynb        # 5. Compute-отчёт
```

Полный отчёт: `report.Rmd`

## Структура

| Файл | Описание |
|---|---|
| `workshop.ipynb` | Сбор датасета (iTunes + Last.fm) + CF-граф |
| `02_embeddings.ipynb` | E5 + CLIP + CLAP эмбеддинги |
| `03_fusion.ipynb` | Early / Late / Cross-attention fusion |
| `04_recsys_eval.ipynb` | Warm vs Cold evaluation |
| `05_compute.ipynb` | Вычислительная сложность |
| `report.Rmd` | Полный отчёт с результатами |

## Результаты (кратко)

- **14 787** треков с 3 модальностями
- **Fusion > text-only** на +22–34% (Recall@10, cold)
- **CF = 0 на cold**, multimodal ≈ 0.11 — главный результат
- Датасет: ~17 ГБ, эмбеддинги: ~2 ч на CPU

## Данные

В git нет `data/audio/`, `data/images/` и `data/raw/` (~17 ГБ). Аудио и обложки можно скачать через `workshop.ipynb`.
