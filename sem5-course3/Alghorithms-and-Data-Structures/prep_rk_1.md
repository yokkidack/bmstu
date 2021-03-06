# Алгоритм

- 1. `Алгоритм быстрого возведения в степерь`

Алгоритм бинарного возведения аль-Каши

[шмяк](https://ru.wikipedia.org/wiki/Алгоритмы_быстрого_возведения_в_степень)

- 2. `Алгоритм получения N числа фибоначчи за O(log n)`

Кнут: 

```
( Fn+1 Fn ) = ( 1 1 )^n
( Fn Fn-1 )   ( 1 0 )
```

- 3. `Алгоритм генерации подстановок`

[шмяк](https://habr.com/ru/post/248493/)

- 4. `Проверка числа на простоту `

```
Проверка на простоту

Чтобы определить, является ли данное число N простым, безусловно, достаточно написать простой цикл поиска делителей числа N:

bool prime(long long n){ 
	for(long long i=2;i<=sqrt(n);i++)
		if(n%i==0)
			return false;
	return true;
}


Данная функция проверки числа на простоту достаточно эффективна — асимптотика ее работы O (sqrt(N)).
```
лучше: (O (log N))
[шмяк](https://habr.com/ru/post/205318/) 

- 5. `Разворот списка за О(n) и О(1) по памяти`

```format=go
func (chain *links) Reverse() *links {
    if chain == nil || chain.Next == nil {
        return chain
    }

    left, next := chain, chain.Next.Next
    chain = chain.Next
    left.Next = nil

    for {
        chain.Next = left

        if next == nil {
            break
        }

        left, chain, next = chain, next, next.Next
    }

    return chain
}
```

[шмяк](https://bolknote.ru/all/3814/)

- 6. `Двусвязная очередь`
 
 кнут. искусство. 269
 
- 7. Удаление идущих подряд идущих идентичных членов в односвязном списке

/нашел какоето решение но пока не разобрался/

- 8. Найти есть ли в списке цикл за константу по памяти

```format=c++
bool isCycled(struct List *head) {
    if (!head) return false;
    struct List *fast = head->next;
    struct List *slow = head;
    bool slow_advance = false;
    while(fast) {
        if(fast == slow) // догнали slow
            return true;
        if(slow_advance) // замедляем slow
            slow = slow->next;
        slow_advance = !slow_advance;
        fast = fast->next;
    }
    return false;
}
```

- 9. Рекурсивный обход доски конем

[шмяк](http://algolist.manual.ru/maths/combinat/knight.php)

```
int arr[8][8], row[64], col[64];
int ktmov1[8] = { -2, -1, 1, 2, 2, 1, -1, -2 };
int ktmov2[8] = { 1, 2, 2, 1, -1, -2, -2, -1 };

int i, j, move_num, d; 
	  
main() {
  addknight( );
}
	  
addknight( )  {
  register int a, b, e; 
		  
 /* пометить клетку как посещенную и запомнить координаты клетки */
  arr[i][j] = 1;
  row[move_num] = i;
  col[move_num] = j;
  move_num++;
		  
 /* проверить 8 возможных перемещений коня */
  for ( a = 0 ; a <= 7 ; a++ ) {
   /* если все ходы сделаны, печатаем их */
    if ( move_num >= 64 ) {
      writeboard( ); 
      exit ( 0 );
    }
			  
   /* определяем колонку и строку для следующего хода */
    b = i + ktmov1[a];
    e = j + ktmov2[a];
			  
   /* проверяем, что после выполенения хода конь остается на шахматной доске */
    if ( b < 0 || b > 7 || e < 0 || e > 7 )
      continue; 

   /* проверяем, были ли мы уже в этой клетке */
    if ( arr[b][e] == 1 )
      continue; 
     i = b; j = e;
    addknight();
  } 
		  
 /* уменьшить счетчик ходов и попробовать сделать следующий ход */
  move_num-- ;
	  
 /* освобождаем клетку, ранее занятую конем */
  arr[row[move_num]][col[move_num]] = 0;
  move_num--;  /* пробуем сделать следующий ход */
  i = row[move_num]; j = col[move_num];
  move_num++; 
}
	  
writeboard( ) {
  int a;
		  
  clrscr( );
  gotoxy ( 1, 10 );
  printf ( "Hit any key for next move " );
  gotoxy ( 1, 11 );
  for ( a = 0 ; a <= 63 ; a++ ) {
    if ( a % 8 == 0 )
      printf ( "\n" );
    printf ( "#" );
  }
  for ( a = 0 ; a &lt;= 63 ; a++ ) {
    gotoxy ( col[a] * 3 + 1, 12 + row[a] );
    printf ( "%3d", a + 1 );
    getch( );
  }
}
```

- 10. Рекурсивный алгоритм прохождения лабиринта

/не знаю что это значит, надеюсь пойму/

- 11. Оценить время выполнения рекурсии в мастер теореме

/will pass on that/

- 12. рекурсивный алгоритм вычисления биномиального коэф

[жмяк](https://habr.com/ru/post/274689/)
```
// расчет факториала n
unsigned fakt(int n)
{
   unsigned r;
   for (r=1;n>0;--n)  
         r*=n;
   return r;
}
// расчет C(n,k)
unsinged bci(int n,int k)
{
   return fakt(n)/(fakt(k)*fakt(n-k));
}
```
- 13. Ханойская башня

[рекурсивное решение](https://ru.wikipedia.org/wiki/Ханойская_башня)

- 14. Олгоритм выведения узов дерева поиска в неубывающем порядке

см алгоритм inorderTreeWalk

- 15. Алгоритм подсчета слов в строке

/не понял суть тип найти количество пробелов хз/

- 16. написать алгоритм проверки является ли множество из м элементов подмножеством множества с н элементами

```
     1.3.5. Проверка включения слиянием
     Рассмотрим алгоритм слияния, который определяет, является ли
множество A подмножеством множества B.
     Алгоритм 1.4. Проверка включения слиянием.
     Вход: проверяемые множества A и B, которые заданы указате-
лями a и b.
     Выход: true, если AB, в противном случае false.

34


     pa := a; pb := b // инициализация
     while panil & pbnil do
           if pa.i < pb.i then
                  return false     // элемент множества A
                                   // отсутствует в множестве B
           elseif pa.i > pb.i then
                  pb := pb.n       // элемент множества A, может быть,
                                   // присутствует в множествеB
           else
                  pa := pa.n       // здесь pa.i = pb.i, то есть
                  pb := pb.n       // элемент множества A точно
                                   // присутствует в множестве B
           end if
     end while
     return pa=nil // true, если A исчерпано, false — иначе
     Обоснование. На каждом шаге основного цикла возможна одна
из трѐх ситуаций: текущий элемент множества A меньше, больше или
равен текущему элементу множества B. В первом случае текущий
элемент множества A заведомо меньше, чем текущий и все после-
дующие элементы множества B, а потому он не содержится в множе-
стве B и можно завершить выполнение алгоритма. Во втором случае
происходит продвижение по множеству B в надежде отыскать эле-
мент, совпадающий с текущим элементом множества A. В третьем
случае найдены совпадающие элементы и происходит продвижение
сразу в обоих множествах. По завершении основного цикла возмож-
ны два варианта: либо pa=nil, либо panil. Первый вариант означает,
что для всех элементов множества A удалось найти совпадающие
элементы в множестве B. Второй — что множество B закончилось
раньше, то есть не для всех элементов множества A удалось найти
совпадающие элементы в множестве B.
```

## trash

- рекурсивный факториал

```
function Factorial(n: Word): integer;
begin
if n > 1 then
Factorial:=n*Factorial(n-1)
else
Factorial:=1;
end;
```

## Алгоритмы для работы с деревьями
 
[может перейти в итмо, они классные, а это все что может понадобиться](https://neerc.ifmo.ru/wiki/index.php?title=Дерево_поиска,_наивная_реализация)
