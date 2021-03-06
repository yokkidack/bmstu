# `Линейные структуры данных.`
## 1/2
## Список

- структура данных, каждый элемент который состоит из данных и ссылки на следующий элемент, у последнего элемента ссылка пустая.

## Двусвязный список

- структура данных, каждый элемент который состоит из данных и ссылки на следующий элемент и ссылки на предыдущий элемент, у последнего элемента ссылка на следующий пустая, у первого ссылка на предыдущий пустая.

## Очередь

- это структура данных, реализующая принцып FIFO

## Стек

- это структура данных, реализующая принцып FILO

## Поиск в глубину

Посещаем крайнюю не посещенную до тех пор пока может переходить, когда не можем переходим на уровень выше

### Алгоритм
```
#есть:
# neighbours(v)
# visit(v)

# Дано:
граф
вершина_начало

# Пусть:
список_ответ.
стек_необойденные.

# Решение:
добавить в очередь neighbours(вершина_начало)
visit(вершина_начало)
добавить в список_ответ вершина_начало

до тех пор пока очередь_непосещенные не пустое сделать

    взять из очередь_непосещенные вершину
    если вершина посещена скипъ
    в обратном случае
        добавить в очередь neighbours(вершина)
        visit(вершина)
        добавить в список_ответ вершина

сделано
```

### Оценка

O(V+U)

по памяти: O(V)

## Поиск в ширину

Последовательно спрашивает список соседей, а потом обходим их. Использовать очередь для хранения не обойденных соседей.

### Алгоритм

```
#есть:
# neighbours(v)
# visit(v)

# Дано:
граф
вершина_начало

# Пусть:
список_ответ.
очередь_необойденные.

# Решение:
добавить в очередь neighbours(вершина_начало)
visit(вершина_начало)
добавить в список_ответ вершина_начало

до тех пор пока очередь_непосещенные не пустое сделать

    взять из очередь_непосещенные вершину
    если вершина посещена скипъ
    в обратном случае
        добавить в очередь neighbours(вершина)
        visit(вершина)
        добавить в список_ответ вершина

сделано
```

### Оценка

O(V+U)

по памяти: O(V)

## 2/2

() - ok
((())()) - ok
)()( - x
((( - x

[(]) - x

### Многочлен

`x^3 + 5*x^2 + 10`

1. в строку
2. ассоциативный массив
3. массив
4. массив с каждым элементом-структурой <pow, k>
5. СДДП

### Развернуть список

```
#Дано:
начало
список

#Путь:
новый_список
начало_нового
рабочая_ссылка

#Решение:
рабочая ссылка = начало
начало_нового = пусто
до тех пор пока рабочая сссылка не равна пусто делать
    добавить элемент в новый спимсок по рабочей_ссылке, ссылка на следующий равна начало_нового, начало_нового = ссылка на новый элемент.
    рабочая_ссылка = рабочая_ссылка.следующий_элемент
сделано
```
