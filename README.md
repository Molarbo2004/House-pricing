# House Prices: Advanced Regression Techniques

Решение задачи регрессии для предсказания цен на жилье (Kaggle House Prices). Реализована собственная версия Ridge-регрессии на NumPy.

## 📊 Результаты
- **Модель:** Ridge Regression (собственная реализация на NumPy)
- **Признаки:** Числовые + One-Hot категориальные (127 признаков)
- **Валидация (RMSE, деление train.csv на train/val/test):** ~0.138 
- **RMSE на полных данных train.csv:** ~0.125 (in-sample)
- **Kaggle Score:** *[Вставь свой результат, когда посчитает Kaggle]*

## 🛠 Стек
- Python 3
- Pandas, NumPy (обработка данных и математика)
- Matplotlib, Seaborn (визуализация)

## 🚀 Как запустить
1. Скачай данные с [Kaggle](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data) и положи `train.csv` и `test.csv` в папку `data/`.
2. Установи зависимости:
   ```bash
   pip install -r requirements.txt
   ``` 
3. Открой и запусти ноутбук notebooks/main.ipynb следуя шаг за шагом

## 🧠 Шаги пайплайна 
1. Загрузка данных и их объединение в общий датасет
   
<img width="1502" height="399" alt="image" src="https://github.com/user-attachments/assets/89e1c507-6529-477f-89bf-9b7b1080df19" />

2. Приведение к общему стилю строк (названия столбцов)

<img width="1480" height="332" alt="image" src="https://github.com/user-attachments/assets/6693d112-526d-40cb-ab66-22e8b502a396" />

3. Подсчет кол-ва признаков

<img width="199" height="34" alt="image" src="https://github.com/user-attachments/assets/da3b54df-7b60-4ced-a890-2f0556e1a715" />

4. Приведение к общему виду строк (значений столбцов с типом "str")

<img width="1493" height="405" alt="image" src="https://github.com/user-attachments/assets/9ad4b771-e9ca-4e21-a490-39f99c32e31c" />

5. Просмотр каждой колонки признаков

<img width="664" height="568" alt="image" src="https://github.com/user-attachments/assets/e800e326-de2d-4759-8fc1-c636e3bbb92e" />

6. Распределение цен на дом 

<img width="618" height="449" alt="image" src="https://github.com/user-attachments/assets/2da6958b-a189-4e54-973f-2d28cfe38138" />

Цены меньше 100000:

<img width="591" height="456" alt="image" src="https://github.com/user-attachments/assets/b2a7e1cd-2524-4c8e-83d0-68771acd156e" />

7. Приведение цены к нормальному распределению через log1p

<img width="632" height="507" alt="image" src="https://github.com/user-attachments/assets/f0bee97a-d2ab-4a29-97d7-d82b4c11f23c" />

8. Подсчет пропущенных значений 

<img width="255" height="258" alt="image" src="https://github.com/user-attachments/assets/f95d1cbb-d7a7-4f05-939a-979c1fd34582" />

9. Деление данных и реализация функции с Ridge регрессией (восстанавливаем границу и берем только train.csv)

<img width="286" height="85" alt="image" src="https://github.com/user-attachments/assets/07d8ba87-aa19-4404-8ddc-7500ea6daf33" />

10. Процесс обучения и вывод весов модели

<img width="696" height="194" alt="image" src="https://github.com/user-attachments/assets/bd17b3b0-047a-461f-a50e-11ea36713645" />

11. График: истинные значения vs предсказанные значения

<img width="632" height="462" alt="image" src="https://github.com/user-attachments/assets/4b7c2565-e800-4cb2-9143-dffb2d540e11" />

12. Функция квадратичной ошибки и проверка среднеквадратичной ошибки при alpha = 1.0 на обучающих данных

<img width="273" height="33" alt="image" src="https://github.com/user-attachments/assets/a6fd907d-93bb-447d-92df-586b982bf6bc" />

13. Оценка масштабов признаков

<img width="655" height="604" alt="image" src="https://github.com/user-attachments/assets/86c009e2-b7f8-4729-8897-f9adddc78c06" />

14. Стандартизация признаков
15. Подбор лучшего alpha на данных валидации

<img width="364" height="196" alt="image" src="https://github.com/user-attachments/assets/8a6c6938-a191-4bce-ab33-d353e91834d0" />

16. Вывод RMSE на train/val/test с учетом Best alpha = 0.0001

<img width="250" height="91" alt="image" src="https://github.com/user-attachments/assets/ef74e398-eb58-43bb-b2b8-4365c5d4c2de" />

17. Подсчет категориальных колонок и других типов признаков

<img width="1497" height="181" alt="image" src="https://github.com/user-attachments/assets/660bfa0e-be3b-4e5c-97a3-0b2c927c47d9" />

18. Анализ категориальных переменных

<img width="768" height="582" alt="image" src="https://github.com/user-attachments/assets/f0db1cf0-b066-4be3-8799-d236799ef3e2" />

19. Используемые категориальные переменные и one-hot encoding

<img width="262" height="35" alt="image" src="https://github.com/user-attachments/assets/c6f2d5d7-af00-415f-9d6e-5bd6b24f9b8e" />

20. Финальная модель с числовыми+категориальными признаками и RMSE на трех выборках

<img width="351" height="303" alt="image" src="https://github.com/user-attachments/assets/14f290e5-cee6-4fee-87f8-1f410662fa94" />

21. Переобучение на всем train.csv чтобы точность была больше

<img width="456" height="115" alt="image" src="https://github.com/user-attachments/assets/d4f9bcd8-54ef-4f52-a86c-9cad0d4c3444" />

22. Загрузка test.csv

<img width="371" height="73" alt="image" src="https://github.com/user-attachments/assets/488a1353-79f4-464f-8a42-59fecb9bc00a" />

23. Базовая предобработка test.csv (по аналогии как выше)

<img width="1509" height="183" alt="image" src="https://github.com/user-attachments/assets/fba89304-e14e-4d6a-a3c4-f7f8c8faf4ee" />

24. Стандартизация как в train.csv и просмотр диапазонов предсказанных цен через min/max/mean/median и поиск NaN

<img width="263" height="170" alt="image" src="https://github.com/user-attachments/assets/9a0c26d1-a4ba-46bd-a109-d85052c4b1ec" />

25. Конечный submission

<img width="326" height="280" alt="image" src="https://github.com/user-attachments/assets/673b0ff4-2f9e-4867-a8d6-aea91123b0b2" />

