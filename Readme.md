# Toxicity Detection

Модель для определения токсичности русскоязычных комментариев на основе ai-forever/ruElectra-small (PyTorch + Transformers).

---
## Задача

Multi-label классификация по трём независимым меткам:

* INSULT
* OBSCENITY
* THREAT

NORMAL определяется как отсутствие всех трёх меток.

---
## Архитекрута

* Модель: ai-forever/ruElectra-small
* Голова: Linear → 3 выхода
* Loss: BCEWithLogitsLoss (с учётом дисбаланса классов)

Macro F1 на тесте: ~0.81

---
## Датасет

Использован датасет “Toxic Russian Comments”.

Автор: Alexander Semiletov
Источник: https://www.kaggle.com/datasets/alexandersemiletov/toxic-russian-comments/
Лицензия: Creative Commons CC BY-NC-SA 4.0

---
\### Лицензия проекта

Проект (включая обученную модель и веса) распространяется в соответствии с лицензией
Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)
https://creativecommons.org/licenses/by-nc-sa/4.0/

Это означает:
* требуется указание авторства исходного датасета
* запрещено коммерческое использование
* производные работы должны распространяться на тех же условиях

---







