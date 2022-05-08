## Лабораторная работа №2
__Задача__:  Моделирование алгоритма Chord, используемого при создании структурированных пиринговых сетей. Модель должна быть реализована в виде массива объектов класса ChordNode. Для выполнения задания требуется выполнить следующие операции:  
1. Реализовать класс ChordNode, содержащий всю необходимую информацию об узле
2. Реализовать функции:  
    a. Поиск по идентификатору  
    b. Добавление узла  
    c. Удаление узла  
    d. Стабилизация системы (доп.)  

__Исходные данные__:  
• Количество бит, используемых для генерации идентификаторов  (m_bits)  
• Идентификаторы позиций, в которых находятся узлы (id)

__Пояснения__:  
|Параметр|Содержание|
|---|---|
|finger[i].start|(id + 2**i) % 2 ** m_bits|
|finger[i].succ_id / successor().id| следующий узел в кольце данного узла|
|predecessor_id| предыдущий узел в кольце данного узла |

Класс Finger хранит start и succ_id пальцев узла.  
Класс ChordNode хранит информацию об узле, методы работы с узлами.  
Класс ChordCircle содержит словарь со всеми узлами данного кольца, выводит информацию о кольце, генерирует узлы.   
