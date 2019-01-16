## Вопросы

- [x] Основные понятия и классы задач исследования операций.
- [x] Постановка задачи линейного программирования (ЛП)
- [ ] Симплекс-метод решения задачи ЛП. Основные этапы симплекс-метода.
- [ ] Двойственность в ЛП. Постановка двойственной задачи ЛП. Формулировка принципа двойственности в ЛП.
- [x] Постановка задачи целочисленного программирования (ЦП). Методы решения задач ЦП.
- [ ] Метод ветвей и границ решения задачи ЦП.
- [ ] Постановка задачи булева программирования (БП). Комбинаторная сложность задачи БП. Идея «жадного» алгоритма.
- [ ] Метод Балаша решения задачи БП.
- [ ] Задачи управления проектами. Диаграмма Ганта.
- [ ] Топологическая сортировка и частичное упорядочение. Основные понятия теории паросочетаний.
- [ ] Метод критического пути.
- [ ] Задача о назначениях. Квадратичная задача о назначениях.
- [ ] Основные понятия многокритериальной оптимизации (МКО). Типы критериев.
- [ ] Методы свертывания критериев в МКО.
- [ ] Эффективное и слабо эффективное решения. Множество Парето и «точка утопии».
- [ ] Метод Саати.
- [ ] Методы прямого поиска: пассивный поиск, последовательный (дихотомии, золотого сечения, Фибоначчи) поиск.
- [ ] Стохастические алгоритмы. Случайный поиск. Алгоритм прямого отжига. 
- [ ] Эволюционные алгоритмы.
- [ ] Генетические алгоритмы: критерии останова, алгоритмы селекции, кроссовера, мутации.
- [ ] ROC-анализ. 

## Ответы:
### 1 Основные понятия и классы задач исследования операций.
Основные понятия и классы задач исследования операций.
Основные определения:
Критерий оптимальности – признаки и предпочтения по которым следует производить сравнительную характеристику альтернатив и 
выбрать среди них наилучшую.
Математическая модель объекта оптимизации – модель, описывающая объект с помощью соотношений между величинами, описывающими 
его свойства.
Параметры оптимизации – это изменяемые при оптимизации величины, входящие в ММО.
Ограничения – соотношения, устанавливающие возможные пределы изменения этих параметров.
Целевая функция – функция параметров оптимизации, выражающая количественную меру достижения цели оптимизации рассматриваемого 
объекта.
Конечномерная задача оптимизации – если множество параметров оптимизации является подмножеством конечномерного линейного 
пространства.
Задача математического программированиям – конечномерная задача с единственной ЦФ; в противном случае – задача много-
критериальной оптимизации.
Задача линейного программирования – ЦФ и ограничения являются линейными относительно параметров оптимизации; в противном 
случае – задача нелинейного программирования.
Классы задач оптимизации:
- 1. Общая задача математического программирования:
 где  -  множество различных альтернатив, рассматриваемых при поиске решения задачи.  – допустимое множество.   
 при которой ЦФ достигает наименьшего значения называют оптимальным решением. Данную задачу также будем называть задачей 
 минимизации целевой функции.
- 2. Стандартная задача линейного программирования:
- 3. Общая задача линейного программирования:
Если к (1.20 – 1.22) добавить ограничения типа неравенства.
- 4. Основная задача линейного программирования -  если убрать из 3 ограничения типа равенства.
- 5. Задача квадратичного программирования
- 6. Задача дробно-линейного программирования
- 7.  Задача сепарабельного программирования.
- 8. Задача геометрического программирования (обе части - позиномами)

### 3 Постановка задачи линейного программирования (ЛП). Каноническая форма задачи ЛП. ЛП как раздел выпуклого программирования.
### 4 Двойственность в ЛП. Постановка двойственной задачи ЛП. Формулировка принципа двойственности в ЛП.
### 5 Постановка задачи целочисленного программирования (ЦП). Методы решения задач ЦП.

Постановка задачи целочисленного программирования (ЦП). Методы решения задач ЦП.
Под задачей целочисленного программирования (ЦП) понимается задача, в которой все или некоторые переменные должны принимать 
целые значения. В том случае, когда ограничения и целевая функция задачи представляют собой линейные зависимости, задачу 
называют целочисленной задачей линейного программирования. В противном случае, когда хотя бы одна зависимость будет 
нелинейной, это будет целочисленной задачей нелинейного программирования.

### 6 Метод ветвей и границ решения задачи ЦП.
### 7 Постановка задачи булева программирования (БП). Комбинаторная сложность задачи БП. Идея «жадного» алгоритма.
### 8 Метод Балаша решения задачи БП.
### 9 Задачи управления проектами. Диаграмма Ганта.
### 10 Топологическая сортировка и частичное упорядочение. Основные понятия теории паросочетаний.
### 11 Метод критического пути.
### 12 Задача о назначениях. Квадратичная задача о назначениях.
### 13 Основные понятия многокритериальной оптимизации (МКО). Типы критериев.
### 14 Методы свертывания критериев в МКО.
### 15 Эффективное и слабо эффективное решения. Множество Парето и «точка утопии».
### 16 Метод Саати.
### 17 Методы прямого поиска: пассивный поиск, последовательный (дихотомии, золотого сечения, Фибоначчи) поиск.
### 18 Стохастические алгоритмы. Случайный поиск. Алгоритм прямого отжига. 
### 19 Эволюционные алгоритмы.
### 20 Генетические алгоритмы: критерии останова, алгоритмы селекции, кроссовера, мутации.
### 21 ROC-анализ. 