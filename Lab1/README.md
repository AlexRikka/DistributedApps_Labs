## Лабораторная работа №1
__Задача__:  Разработать клиент серверный механизм передачи цифрового изображения с помощью сокетов Беркли. Учесть возможность возникновения помех в канале передачи. Оценить потери данных при наличии блока восстановления ошибок и при его отсутствии.

Исходные данные:  
• Цифровое изображение  
• Алгоритм внесения искажений (импульсный шум)

__Алгоритм работы системы__:  
1. Client считывает изображение из файла, передает его размер и само изображение NoiseServer через порт 5065.
2. NoiseServer принимает данные от Client, добавляет на изображение белый шум, отправляет исходное и зашумленное иображения на FinalServer через порт 5066.
3. FinalServer принимает исходное и зашумленное изображения, применяет алгоритм восстановления для последнего. Далее проводится оценка потери данных для зашумленного и восстановленного изображений с помощью метрик Mean Squared Error, Structural Similarity Index, Peak signal-to-noise ratio.
