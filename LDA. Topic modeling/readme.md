В данной работе решается задача тематического моделирования отзывов на парфюмерию.
Так как в каждом отзыве может быть несколько тем, было принято решение разбить каждый отзыв на предложения 
и уже потом обучать модель. В результате coherence score вырос с ~40 до ~60. Также были построены граффики,
показывающие зависимость coherence score от количества топиков. На их основании было выбрано количество
топиков для финальной модели.
 
Во время выполнения были использованы разные библиотеки для лемматизации текста:<br>
 -pymystem3<br>
 -pymorphy<br>
 -spacy (в качестве лемматизатора использует pymorphy, поддерживает "встроенную" многопоточность)<br>
 
Самую высокую скорость обработки показал pymorphy при использовании многопоточности (multiprocessing, pool).
 
Также, возможно дополнительно обучить модель решающую задачу Sentiment Analysis. Потенциально - это может
дать полезную информацию для бизнеса. Например, оценить удовлетворённость клиентами внешним видом, ароматом,
упаковкой и т.д. Задача непростая и подразумевает применение различных подходов, помимо представленного в
бейзлайне.

*Симпатичные визуализации github не показывает. Если открыть через [github.dev](https://github.dev/alexander-bogomol/pet_projects/blob/master/LDA.%20Topic%20modeling/topic_modeling%20(LDA).ipynb) - всё ок.
