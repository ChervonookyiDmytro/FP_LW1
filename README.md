<p align="center"><b>МОНУ НТУУ КПІ ім. Ігоря Сікорського ФПМ СПіСКС</b></p>
<p align="center">
<b>Звіт з лабораторної роботи 1</b><br/>
"Обробка списків з використанням базових функцій"<br/>
дисципліни "Вступ до функціонального програмування"
</p>

<p align="right"> 
<b>Студент</b>: 
<em> Червоноокий Дмитро Сергійович</em></p>

<p align="right"><b>Рік</b>: <em>2025</em></p>

## Загальне завдання

```lisp
;; Пункт 1 (створення списку)
CL-USER> (set 'lst (cons 'q (cons '(NIL) (list 7 'Q 8))))
(Q (NIL) 7 Q 8)

;; Пункт 2 (отримання голови списку)
CL-USER> (car lst)
Q

;; Пункт 3 (отримання хвоста списку)
CL-USER> (cdr lst)
((NIL) 7 Q 8)

;; Пункт 4 (отримання третього елемента списку)
CL-USER> (third lst)
7

;; Пункт 5 (отримання останнього елемента списку)
CL-USER> (car (last lst))
8

;; Пункт 6 (Використання предикатів ATOM та LISTP)
;;ATOM
CL-USER> (atom (car (second lst)))
T
CL-USER> (atom (second lst))
NIL
CL-USER> (atom (car (last lst)))
T

;;LISTP
CL-USER> (listp (first lst))
NIL
CL-USER> (listp (second lst))
T
CL-USER> (listp (car (second lst)))
T

;; Пункт 7 (Використання інших предикатів)
;;ODDP
CL-USER> (oddp (third lst))
T

;;EQ
CL-USER> (eq (car (second lst)) (first (nth 1 lst)))
T

;;EQUALP
CL-USER> (eql (third lst) (nth 4 lst))
NIL

;; Пункт 8 (Об'єднання списку із підсписком)
CL-USER> (append (second lst) lst)
(NIL Q (NIL) 7 Q 8)

```

## Варіант 2
<p align="center"><img src="https://github.com/ChervonookyiDmytro/FP_LW1/blob/main/image_2025-09-22_14-13-33.png"></p>

### Лістинг команди конструювання списку та результат її виконанння
```lisp
CL-USER> (let ((y (list 'A 2 1))) (list y 'B (cdr y) 'C ))
((A 2 1) B (2 1) C)

;; або

CL-USER> (list (list 'A 2 1) 'B (list 2 1) 'C)
((A 2 1) B (2 1) C)
```
