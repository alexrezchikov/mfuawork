# Вариант 15: решения задач

## Задача 1
**Дано:** $(X > 1) \wedge \overline{(X < 5)} \vee (X < 3)$, $X = 2$.  
**Решение:**  
- $X > 1 \Rightarrow 2 > 1 \Rightarrow \text{истина}$;  
- $X < 5 \Rightarrow 2 < 5 \Rightarrow \text{истина} \Rightarrow \overline{\text{истина}} = \text{ложь}$;  
- $X < 3 \Rightarrow 2 < 3 \Rightarrow \text{истина}$;  
- $\text{истина} \wedge \text{ложь} \vee \text{истина} = \text{ложь} \vee \text{истина} = \text{истина}$.  
**Ответ:** $1$.

---

## Задача 2
**Дано:** «Если две прямые лежат в одной плоскости и не пересекаются, то такие прямые параллельны».  
**Решение:**  
- По определению параллельных прямых в планиметрии: две прямые на плоскости называются параллельными, если они не пересекаются;  
- Данное утверждение полностью соответствует этому определению;  
- Следовательно, высказывание является истинным.  
**Ответ:** утверждение истинно.

---

## Задача 3
**Дано:** $(\overline{X} \vee Y) \rightarrow (X \wedge Z) \rightarrow (\overline{Z} \vee \overline{X} \vee Y)$.  
**Решение:**  
- $A \rightarrow B = \overline{A} \vee B$;  
- Левая часть: $\overline{(\overline{X} \vee Y)} \vee (X \wedge Z) = (X \wedge \overline{Y}) \vee (X \wedge Z) = X \wedge (\overline{Y} \vee Z)$;  
- Всё выражение: $\overline{(X \wedge (\overline{Y} \vee Z))} \vee (\overline{Z} \vee \overline{X} \vee Y) = \overline{X} \vee (Y \wedge \overline{Z}) \vee \overline{Z} \vee \overline{X} \vee Y$;  
- $\overline{X} \vee \overline{X} \vee Y \vee (Y \wedge \overline{Z}) \vee \overline{Z} = \overline{X} \vee Y \vee \overline{Z}$.  
**Ответ:** $\overline{X} \vee Y \vee \overline{Z}$.

---

## Задача 4
**Дано:** $(B \vee A) \wedge \overline{A} \vee \overline{B}$.  
**Решение:**  
- Раскрываем скобки: $(B \wedge \overline{A}) \vee (A \wedge \overline{A}) \vee \overline{B}$;  
- $A \wedge \overline{A} = 0 \Rightarrow (B \wedge \overline{A}) \vee \overline{B}$;  
- $(B \vee \overline{B}) \wedge (\overline{A} \vee \overline{B}) = 1 \wedge (\overline{A} \vee \overline{B}) = \overline{A} \vee \overline{B}$.  
**Ответ:** $\overline{A} \vee \overline{B}$.

---

# Задача 5: построение таблицы истинности

**Дано:** $((\overline{X} \wedge Y) \leftrightarrow (\overline{Y} \vee \overline{X})) \vee \overline{X}$

| $X$ | $Y$ | $\overline{X}$ | $\overline{Y}$ | $\overline{X} \wedge Y$ | $\overline{Y} \vee \overline{X}$ | $(\overline{X} \wedge Y) \leftrightarrow (\overline{Y} \vee \overline{X})$ | $\overline{X}$ | $((\overline{X} \wedge Y) \leftrightarrow (\overline{Y} \vee \overline{X})) \vee \overline{X}$ |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 0   | 0   | 1   | 1   | 0               | 1               | 0                                             | 1              | 1                                                                                               |
| 0   | 1   | 1   | 0   | 1               | 1               | 1                                             | 1              | 1                                                                                               |
| 1   | 0   | 0   | 1   | 0               | 1               | 0                                             | 0              | 0                                                                                               |
| 1   | 1   | 0   | 0   | 0               | 0               | 1                                             | 0              | 1                                                                                               |

**Финальный ответ:** выражение не является тождественно истинным (принимает значение 0 при $X=1, Y=0$), упрощённый вид: $Y \vee \overline{X}$.