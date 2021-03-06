# Теория алгоритмов (весенний семестр 2018)

Курс для студентов 3-го года программы [Фундаментальная и компьютерная лингвистика](https://www.hse.ru/ba/ling/)

* [Задачи и текущие оценки](https://docs.google.com/spreadsheets/d/e/2PACX-1vRkI9ORu_drRCs7EGCNriny9_zrseHFBuIl8-aJt--NMskHg1jj7LWojfsCNxhqDmsZjIbcsa42MvN2/pubhtml)
* [О подозрениях в списывании](meta/cheating.md)
* [Визуализатор алгоритмов](http://algo-visualizer.jasonpark.me)

# Литература

* **CLRS:** Thomas H. Cormen, Charles E. Leiserson, Ronald L. Rivest and Clifford Stein *Introduction to Algorithms*, 3rd edition, 2009
  (*Алгоритмы: построение и анализ*, 3-е издание, 2013)
* Steven Skiena *Algorithm Design Manual* (2nd edition, 2008)
* Бабенко, Левин *Введение в теорию алгоритмов и структур данных*
* D. Gusfield. *Algorithms on Strings, Trees, and Sequences: Computer Science and Computational Biology.* (1997)

# Конспект лекций

[PDF](https://mkuznets.com/hse/2018-alg/lecture_notes.pdf)


# Программа курса

## Модуль 3

1. **Анализ алгоритмов. Асимптотическое оценки вычислительной сложности.** [задание](problems/01)

  * Вычислительная модель (Word RAM model)
  * Понятие элементарных с точки зрения процессора операций
  * Временная сложность алгоритма в худшем и среднем случаях
  * Асимптотическая оценка временной сложности. Классы O, Ω, Θ
  * Сравнение темпов роста функций. Типичные для анализа алгоритмов асимптотические классы.
  * Примеры: возведение в целую степень, числа Фибоначчи, умножение Карацубы.

2. **Базовые структуры данных.** [задание](problems/02)

  * Массивы
    * Статический массив. Многомерный случай. Хранение разреженных матриц (CSR format) [[1]](https://en.wikipedia.org/wiki/Sparse_matrix#Compressed_sparse_row_(CSR,_CRS_or_Yale_format)).
    * Динамический массив (вектор) *(Skiena 3.1.1, Бабенко 1.1)*.
    * Амортизационная сложность (учётная стоимость операций)
      * «Метод бухгалтерского учёта» (accounting method) *(CLRS 17.2)*
  * Стеки
      * Реализация через динамический массив.
  * Очереди
    * Реализация очереди с помощью двух стеков [[1]](https://stackoverflow.com/questions/69192/how-to-implement-a-queue-using-two-stacks).
    * Вычисление минимума/максимума за O(1).
    * Реализация через кольцевой буфер.
  * Ссылочные структуры данных
    * Одно- и двусвязные списки. Двухсторонняя очередь как двусвязный список.
  * Битовые массивы [[1]](https://en.wikipedia.org/wiki/Bit_array), [[2]](https://wiki.python.org/moin/BitArrays)
  * Хэширование и хэш-таблицы *(Бабенко, 5.1-5.3, CLRS 11)*
    * Разрешение коллизий: цепочки, открытая адресация (linear probing, double hashing).
    * Защита от намеренных коллизий через universal hashing *(CLRS 11.3.3)*.
    * Feature hashing (hashing trick) [[1]](https://en.wikipedia.org/wiki/Feature_hashing),[[2]](http://scikit-learn.org/stable/modules/feature_extraction.html#feature-hashing)
    * LRU кэш как пример комбинации хэш-таблицы и двухсвязного списка.

3. **Алгоритмы сортировки.** [задание](problems/03)

  * Задача сортировки. Сортировки основанные на сравнениях (Comparison sort).
  * Сортировка пузырьком (Bubble sort).
  * Сортировка вставками (Insertion sort)
  * Нижняя граница сложности сортировки, основанной на сравнениях.
  * Парадигма «разделяй и властвуй» (divide and conquer).
  * Сортировка слиянием (Mergesort). Master theorem и её применение для оценки сложности.
  * Quicksort. Поиск порядковых статистик (selection problem) через Quickselect.
  * Примеры non-comparison sort: сортировка подсчётом (count sort).
  * Selection sort (как приквел к Heapsort).
  * Двоичная куча (Binary heap).
  * Пирамидальная сортировка (Heapsort).

## Контрольная

*Ожидается 27 марта 2018 в 12:10*

## Модуль 4

1. **Структуры данных поиска**
  * Двоичные деревья поиска (binary search trees):
    * Определения, реализация, операции поиска
      * Поиск элемента
      * Поиск минимума/максимума
      * Обходы дерева: в глубину (pre-, in-, post-order), в ширину
      * Поиск следующего и предыдущего значений
    * Динамические деревья поиска
      * Добавление и удаление элементов
      * Сбалансированные деревья поиска (Balanced BST)
        * ... (либо RB, либо splay)
2. **Жадное программирование. Динамическое программирование.**
  * ???
3. **Алгоритмы на графах.**
  * ???
4. **Алгоритмы на строках.**
  * ???
5. Что-нибудь специфичное для лингвистики/численных методов/баз данных
  * ???

## Экзамен