## O que é Bash?
<v-clicks>

 - Bourne-Again Shell
 - Interpretador de linha de comando do GNU <logos-gnu />
 - Incorpora funções do Kourne Shell(`ksh`) e C Shell(`csh`)

</v-clicks>

---

## O que é um shell
<v-clicks>

 - Processador de macros que executa comandos
 - Um shell Unix é um interpretador de comandos e uma linguagem de programação
 - Funcionam de forma interativa ou não-interativa

</v-clicks>

---

## Porque aprender?

---

Nem tudo precisa de Python

---

```shell
cat ./exemplo.csv | grep "opban2"
```

```python
import csv

with open('exemplo.csv', 'r') as arquivo_csv:
    leitor_csv = csv.reader(arquivo_csv, delimiter=',')

    for linha in leitor_csv:
        if 'opban2' in linha:
            print(linha)
```

---

Ajuda a se familiarizar com o Linux e suas ferramentas

---

```bash
cat usuarios.json | \
jq '.[] | select(.idade > 25)' | \
awk '{print $1 "," $3 "@gmail.com"}' | \
sed 's/"//g' > usuarios_filtrados.txt
```

---

E principalmente...

---

```bash
find ./opbk-scripts-devops -type f -iname "*.sh" | wc -l
```

---

275 arquivos
