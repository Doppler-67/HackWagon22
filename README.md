# HackWagon22
**В рамках хакатона HackWagon22, который проводила Первая Грузовая Компания, нужно было разработать сервис для прогнозирования длительности движения вагонов.**
## Цель проекта
Разработка ML-решения для прогнозирования длительности движения вагонов.

## Задачи
Я был капитаном и поэтому вначале я распределил задачи между членами команды.

В мои задачи входило:

1) предобработка данных.
2) исследователський анализ данных.
3) проверка различных гипотез по данным.
4) выбор фитчей для обучения.
5) обучение и тюнинг градиентного бустинга.
6) попробовать применить нейронные сети для данной задачи.
## Результаты
Удалось достичь 63.2278 RMSE на публичной части тестовой выборки и занять 9 место в лидерборде.

Удалось достичь 63.2899 RMSE на приватной части тестовой выборки и занять 11 место в лидерборде.

## Про данные 
Доступно 4.22 млн. строк для обучения и 1.18 млн. строк для теста (без таргета).

Значение метрики на тестовой выборке расчитывалось на удаленном сервере и показывалось в лидерборде. Можно было делать максимум 10 сабмитов в день. 

### Описание данных:

**df_train.parquet**
---
* **st_code_snd —** id станции отправления.

* **st_code_rsv —** id станции назначения.

* **date_depart_year —** год отправления.

* **date_depart_month —** месяц отправления.

* **date_depart_week —** неделя отправления.

* **date_depart_day —** день отправления.

* **date_depart_hour —** час отправления.

* **fr_id —** id груза.

* **route_type —** тип отправки.

* **is_load —** признак гружёности (1 - гружёный, 0 - порожний.

* **rod —** род подвижного состава.

* **common_ch —** id обобщённой характеристики вагона.

* **vidsobst —** вид собственности.

* **distance —** расстояние рейса.

* **snd_org_id —** id грузоотправителя.

* **rsv_org_id —** id грузополучателя.

* **snd_roadid —** id дороги отправления.

* **rsv_roadid —** id дороги назначения.

* **snd_dp_id —** id региона отправления.

* **rsv_dp_id —** id региона назначения.

* **y —** таргет (время в пути в часах).
