### Arrays

---

<v-clicks>

 - Variável que consegue armazenar vários valores em um mesmo nome
 - Nomenclatura segue as regras de variáveis
 - Inicializado por valores separados por espaço e delimitados por `()`
 - Elementos podem ser acessados através do seu índice
 - Contagem inicia no `0`
 - Ao acessar o valor a utilização de `{}` é obrigatória

</v-clicks>

---

```shell {all|4|6|8|10|11|all}
#!/bin/bash
# Description: example using arrays

novo_array=("cachorro" "gato" "maça" "laranja" "onça pintada")

echo "Terceiro valor = ${novo_array[2]}"

novo_array[2]="banana"

echo "Terceiro valor = ${novo_array[2]}"
echo "Todos os elementos = ${novo_array[@]}"
echo "Número de elementos = ${#novo_array[@]}"
```

---

```text
Terceiro valor = maça
Terceiro valor = banana
Todos os elementos = cachorro gato maça laranja onça pintada
Número de elementos = 5
```

---

```shell {all|4|5|7|9|11|13,14|16|all}
#!/bin/bash
# Description: Example append in arrays

array_1=("cachorro" "gato" "maça")
array_1+=("tartaruga")

echo "Último valor = ${array_1[-1]}"

array_1[${#array_1[@]}]="baleia"

echo "Último valor = ${array_1[-1]}"

array_2=("cachorro" "gato" "maça")
array_3=(${array_1[@]} ${array_2[@]})

echo "Todos os elementos = ${array_3[@]}"
```

---

```text
Último valor = tartaruga
Último valor = baleia
Todos os elementos = cachorro gato maça tartaruga baleia cachorro gato maça
```
