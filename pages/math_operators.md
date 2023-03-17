### Operações Matemáticas

---

<v-clicks>

Utilização com expressões aritméticas `$(( expressão ))`

</v-clicks>

---

| **Operação**  | **Operador** |
| ------------- | ------------ |
| Soma          | `a + b`      |
| Subtração     | `a - b`      |
| Multiplicação | `a * b`      |
| Divisão       | `a / b`      |
| Resto         | `a % b`      |
| Exponencial   | `a ** b`     |

---

```shell
#!/bin/bash
# Description: Example math operators

a=5
echo "a = 5"
echo "a + 5 = $(( $a + 5 ))"
echo "a - 5 = $(( $a - 5 ))"
echo "a / 5 = $(( $a / 5 ))"
echo "a % 5 = $(( $a % 5 ))"
echo "a ^ 5 = $(( $a ** 5 ))"
```

---

```text
a = 5
a + 5 = 10
a - 5 = 0
a / 5 = 1
a % 5 = 0
a ^ 5 = 3125
```
