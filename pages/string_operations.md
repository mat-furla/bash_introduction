### Operações com String

---

<v-clicks>

 - Tamanho de uma string: `${#string}`
 - Extração de substrings: `${string:position[:lenght]}`
 - Remover correnpondência mais curta de uma substring dentro da string pelo início: `${string#substring}`
 - Remover correspondência mais curta de uma substring dentro da string pelo final: `${string%substring}`
 - Remover correspondência mais longa de uma substring dentro da string pelo início: `${string##substring}`
 - Remover correspondência mais longa de uma substring dentro da string pelo final: `${string%%substring}`
 - Substituição: `${string/pattern/replacement}`

</v-clicks>

---

```bash {all|4|4,6|4,7|4,8|4,10-11|4,12-13|4,14-15|4,16-17|all}
#!/bin/bash
# Description: string examples

string="Essa é uma string. Ela é bem longa. Vamos ver o que acontece"

echo "Tamanho: ${#string}"
echo "Extraindo primeira sentença: ${string:0:18}"
echo "Extraindo segunda sentença: ${string:19:16}"

echo "Removendo terceira sentença:"
echo ${string%.*}
echo "Removendo primeira sentença:"
echo ${string#*.}
echo "Extraindo primeira sentença:"
echo ${string%%.*}
echo "Extraindo terceira sentença:"
echo ${string##*.}
```

---

```text
Tamanho: 60
Extraindo primeira sentença: Essa é uma string.
Extraindo segunda sentença: Ela é bem longa.

Removendo terceira sentença:
Essa é uma string. Ela é bem longa

Removendo primeira sentença:
Ela é bem longa. Vamos ver o que acontece

Extraindo primeira sentença:
Essa é uma string

Extraindo terceira sentença:
Vamos ver o que acontece
```

---

```bash {all|4|4,6|4,7|4,9-10|4,11-12|all}
#!/bin/bash
# Description: string examples

string="ser ou não ser, eis a questão"

echo "Substituindo primeira ocorrência: ${string/ser/comer}"
echo "Substituindo todas as ocorrências: ${string//ser/comer}"

echo "Substituindo no início:"
echo "${string/#*,/dormir ou não dormir,}"
echo "Substituindo no final:"
echo "${string/%,*/, Shakespeare}"
```

---

```text
Substituindo primeira ocorrência: comer ou não ser, eis a questão
Substituindo todas as ocorrências: comer ou não comer, eis a questão

Substituindo no início:
dormir ou não dormir, eis a questão

Substituindo no final:
ser ou não ser, Shakespeare
```