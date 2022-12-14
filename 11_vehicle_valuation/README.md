## Построение модели определения стоимости автомобиля

Разработка системы рекомендации стоимости автомобиля на основе его описания

**Навыки и инструменты:**
* python
* pandas
* lightgbm

### Общий вывод

Для реализации проекта была проведена предобработка данных:
- удалены дубликаты
- пропуски заполнены самым частотным значением признаков
- удалены аномалии для данных с годом регистрации до 1900 и позднее 2016 года
- нулевые показатели мощности заменены медианными значениями признака по каждой модели
- нулевые значения месяца регистрации заменены самым частотным месяцем - 01
- отсечены аномальные данные с ценой ниже 10 евро, а также колонки с количеством фотографий (которое везде нулевое)

Для решения целей проекта были обучены следующие модели с подбором оптимальных гиперпараметров:
- Линейная регрессия (RMSE = 2989)
- Модель CatBoostRegressor (RMSE = 1604)
- Модель LightGBM (RMSE = 1650)
- Модель DecisionTreeRegressor (RMSE = 1914)

Была проанализирована скорость работы и качество моделей:

* Исходя из требований к качеству и скорости предсказания, а также времени обучения, оптимальным сочетанием гиперпараметров для самой успешной модели CatBoostRegressor будет iterations=85, depth=13, learning rate = 0.5.
