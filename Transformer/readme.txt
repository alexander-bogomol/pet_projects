Написал трансформер "с нуля".
Из примечательного:
- В блоке MHA используется матричное перемножение для всех "голов" сразу с последующим транспонированием и 
выравниванием. Такой подход описан в оригинальной статье и увеличивает скорость работы модели в отличие от
более интуитивного подсчёта weighted score отдельно для каждой головы и последующей конкатенации.
- В слое positional encoding используются срезы тензоров для заполнения соответствующих значений pe-векторов.
Кроме того, вместо возведения в степень используется умножение и деление логарифмов (с последующим вызовом
экспоненты), что также должно ускорять модель и делать вычисления более стабильными.
- Слои были протестированы и сравнены с аналогичными имплементациями от pytorch. Результаты были или близки
(LayerNorm) или полностью эквивалентны (MultiheadAttention)
