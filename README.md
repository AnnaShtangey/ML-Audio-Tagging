# ML-Audio-Tagging
# ML: Обнаружение звуковых событий
Задача: научиться "размечать" аудио события. 
Датасет: https://www.kaggle.com/c/freesound-audio-tagging-2019 

Данные загружены и исследованы.
Применена One-hot-encoding для тегов.
Анализ аудио производится при помощи PCEN-коэффициентов (per-channel energy normalization - PCEN), которые добавляются в таблицу.
Обучена модель градиентного бустинга CatBoostRegressor (берем регрессионную модель, т.к. для нее возможен рассчет мультитаргета, как в нашем случае). 
В качестве функции потерь использовалась MultiRMSE.
Модель протестирована. Исследованы звуки из других источников.
Использованы библиотеки librosa, catboost.