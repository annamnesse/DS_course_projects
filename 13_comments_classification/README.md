## Обучение модели классификации комментариев

Определение токсичности комментариев

**Навыки и инструменты:**
* python
* pandas
* nltk
* tf-idf

### Общий вывод

В ходе работы над проектом выполнены следующие шаги:

* Исходные данные подготовлены к обучению с использованием токенизации и лемматизации текстов
* Датасет поделен на обучающую и тестовую выборки в отношении 70:30
* Обучены модели решающего дерева, логистической регрессии, случайного леса и CatBoost с балансировкой классов. 

Лучший показатель качества по метрике F1=0.75 показала модель логистической регрессии. Данный результат подтверждается при работе модели на тестовых данных.
