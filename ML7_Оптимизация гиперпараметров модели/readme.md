## <center><font color = 'springblue'>**<center><font color='red'> Подбор гиперпараметров для задачи классификации </font></center>**</font></center>

**Данный проект основан на датасете с соревнования [Kaggle: Predicting a Biological Response](https://www.kaggle.com/c/bioresponse).**

### <center><font color = 'springblue'>**Цель проекта**</font></center>
**На основе различных оптимизаторов подобрать гиперпараметры для алгоритма логистической регрессии и алгоритма случайного леса, которые улучшат качество измеряемой метрики F1-score.**

Все факторы подготовлены для моделирования, то есть они очищены, преобразованы и закодированы.
Мы решаем задачу бинарной классификации, где целевой таргет - признак **Activity**.


### <center><font color = 'springblue'>**Этапы проекта**</font></center>

**1. Создание двух моделей с default параметрами.**
  - логистическая регрессии (LogisticRegression),
  - случайный лес (RandomForestClassifier)

**2. Подбор наилучших гиперпараметров и создание на их основе моделей:**
  * 2.1  с помощью оптимизатора GridSearchCV;
  * 2.2  с помощью оптимизатора RandomSearchCV;
  * 2.3  с помощью оптимизатора Hyperopt;
  * 2.4  с помощью оптимизатора Optuna.

**3. Анализ и сравнение значений метрик и затраченного на подбор времени**


  ### <center><font color = 'springblue'>**Результаты**</font></center>

1. Неожиданным результатом оказалось, что качественные признаки, поданные в модели без подбора гиперпарамертов показали хорошее качество предсказания:
 - LogisticRegression F1-score = 0.792
 - RandomForestClassifier F1-score = 0.835
2. Поиск наилучших гиперпараметров всех четырех оптимизатор не улучшил данных значений и стабильно выдавал похожие значения метрик.
3. Оптимальным алгоритмом для решения данной задачи по предсказанию биологического ответа молекул можно считать алгоритм случайного леса RandomForestClassifier.
4. Ключевым этапов по построению качественной модели является не только правильно выбрать модель согласно решаемой задачи, но и подготовить очищенные, нормализованные и информативные признаки, которые и будут определять в итоге качество предсказания.


#### Какие библиотеки использовались для проекта:
<font color = 'springblue'>pandas</font>\
<font color = 'springblue'>sklearn</font>\
<font color = 'springblue'>hyperopt</font>\
<font color = 'springblue'>matplotlib</font>\
<font color = 'springblue'>seaborn</font>
<font color = 'springblue'>optuna</font>




**Проект создан на базе языка Python в Jupyter Notebook.**

Автор: Ярослава Вобшаркян\
(студент школы SkillFactory по курсу Data Science)
