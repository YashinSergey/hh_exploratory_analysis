# Разведывательный анализ данных (EDA) резюме HeadHunter

## Описание проекта

В рамках проекта выполнен разведывательный анализ данных (Exploratory Data Analysis, EDA) резюме соискателей HeadHunter.  
Цель работы — исследовать распределения ключевых признаков, выявить зависимости между ними, обнаружить аномальные наблюдения и выполнить корректную очистку данных.

Анализ включает:
- исследование распределений числовых признаков (возраст, зарплата, опыт работы);
- анализ зависимостей между социально-демографическими характеристиками и уровнем дохода;
- выявление и сравнение аномалий с использованием различных критериев строгости;
- формирование финального очищенного датасета.

Интерактивные визуализации построены с использованием **plotly seaborn и matplotlib**.
Визуализации, созданные с помощбю библиотеки plotly сохранены в формате HTML для корректного отображения в GitHub.

---

## Используемые данные

В связи с ограничениями GitHub на размер файлов, исходные датасеты размещены во внешнем хранилище.

- **Основной датасет резюме (hh_dataset):**  
  https://drive.google.com/file/d/1pV8uBTVSXcgDtKnV5MCIUZ4EXy31uGXR/view?usp=sharing

- **Датасет валют (currencies_ds):**  
  https://drive.google.com/file/d/1EwYavX60nYwVubh_a70-7LQl1rCFiveC/view?usp=sharing

---

## Интерактивные визуализации

GitHub не поддерживает отображение интерактивных графиков Plotly напрямую в ноутбуке, поэтому все визуализации, созданные с помощью этой библиотеки, сохранены в формате HTML.  
Файлы можно открыть в браузере напрямую из репозитория.

Папка с визуализациями:  
https://github.com/YashinSergey/hh_exploratory_analysis/tree/main/assets

### Интерактивные визуализации (Plotly)

- [`age_distribution.html`](https://github.com/YashinSergey/hh_exploratory_analysis/blob/main/assets/age_distribution.html) — распределение возраста соискателей  
- [`work_experience_distribution.html`](https://github.com/YashinSergey/hh_exploratory_analysis/blob/main/assets/work_experience_distribution.html) — распределение признака "Опыт работы (месяц)" 
- [`salary_distribution.html`](https://github.com/YashinSergey/hh_exploratory_analysis/blob/main/assets/salary_distribution.html) — распределение признака "ЗП (руб)" 
- [`salary_on_age_dependency.html`](https://github.com/YashinSergey/hh_exploratory_analysis/blob/main/assets/salary_on_age_dependency.html) — зависимость зарплаты от возраста  
- [`exp_on_age_dependency.html`](https://github.com/YashinSergey/hh_exploratory_analysis/blob/main/assets/exp_on_age_dependency.html) — зависимость опыта работы от возраста  
- [`salary_by_city_destribution.html`](https://github.com/YashinSergey/hh_exploratory_analysis/blob/main/assets/salary_by_city_destribution.html) — распределение желаемой заработной платы по городам (ЗП < 1 млн руб)
- [`salary_by_education_destribution.html`](https://github.com/YashinSergey/hh_exploratory_analysis/blob/main/assets/salary_by_education_destribution.html) — Зависимость медианной ЗП (руб) от уровня образования (ЗП < 1 млн руб)  
- [`median_salary_by_relocation.html`](https://github.com/YashinSergey/hh_exploratory_analysis/blob/main/assets/median_salary_by_relocation.html) — медианная ЗП по готовности к переезду и командировкам (ЗП < 1 млн руб)  

---

## Очистка данных и аномалии

В ходе разведывательного анализа данных (EDA) была применена расширенная система выявления аномалий, основанная на анализе распределений и взаимосвязей между несколькими признаками. По результатам данного этапа было выявлено 5914 строк, потенциально подлежащих удалению. На этом шаге удаление данных не выполнялось — формировался перечень аномальных наблюдений.

Далее, в рамках этапа очистки данных, выполненного строго в соответствии с инструкциями задания, были применены формальные критерии фильтрации. В результате данного этапа из датасета было удалено 101 наблюдение.

Сопоставление результатов показало, что часть строк, удалённых на этапе формальной очистки, уже присутствовала среди ранее выявленных аномалий. Итоговое количество уникальных строк, подлежащих удалению по совокупности применённых критериев, составило **5915**. На основании этого был сформирован финальный очищенный датасет.

---

## Стек

- Python  
- pandas, numpy  
- matplotlib, seaborn, plotly  
- Jupyter / Google Colab  
