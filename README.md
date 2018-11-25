# Audio_1.2
Программа предназначена для воспроизведения текстовых файлов в звук. Программа считывает данные начиная с 19й строки.
Пример *.txt файлф с данными:

Агрегат: ***
Точка: ***
Направление измерений: Произвольное
Замер: ***
Дата и время: ***
Режим измерений: Основной
Тип замера: Форма сигнала
Тип диапазона: Временной
Выборка: 32768
Единицы: м/с
Представление величин: ПИК
Усреднения: Линейные
Количество усреднений: 1
ФВЧ (Гц): 500.000000
ФНЧ (Гц): 12800.000000
Период (мс): 1000.000000

мсек	Канал А, м/с
0.000000	10.417067 << эта строка считается 19-ой, именно с нее и начнется загрузка данных в буфер программы
0.030519	23.382513 < в 1-й колонке время, в 2-й колонке мгновенное значение
0.061037	32.245960
0.091556	31.810053
0.122074	19.045795

Одна строка данных считается как одна точка. Если видите 32768 точек в окне программы, то считайте, что у вас 32768
32768 точек с данными (время, амплитуда). Следовательно в вашем фале было 32768 строк данных начиная с 19 строки.

Для наглядности приводится график этого сигнала. Сигнал можно растянуть ползунком.
На данном этапе реализована только возможность растягивания сигнала в одну сторону.
Посмотреть малый участок сигнала не получистя, но и назначение программы не в этом. Ее задача -
перевести ваши текстовые данные в вид, который можно оцифровать с помощью другого ПО, которое позволит
произвести запись с линейного выхода PC или прямо с звуковой карты.

Если у вас есть сгенерированный файл сигнала в формате, который указан в примере, то вы без проблем сможете его
воспроизвести. Для примера с программой предоставлены несколько текстовых файлов сигнала.
В реальности получалось сгенерировать сигнал в EXCEL в виде таблицы:
    А           B
19   0.001      1.23424
20   0.002      -2.32323

Если вы знаете как генерировать сигнал, то без проблем сможете его прослушать.