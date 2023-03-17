### Argumentos

---

<v-clicks>

 - Argumentos podem ser passados para o script através de uma lista delimitada por espaços
 - `$1` = primeiro argumento, `$2` referencia o segundo e assim por diante
 - `$0` = nome do script
 - `$#` = número de argumentos
 - `$@` = lista de argumentos

</v-clicks>

---

```shell {all|4|5|7|9|10|11|12|all}
#!/bin/bash
# Description: example using arguments

echo "Arquivo = $0"
echo "Terceiro argumento = $3"

argument=$5

echo "Quinto argumento = $argument"
echo "Sexto argumento = $6"
echo "Número de argumentos = $#"
echo "Lista de argumentos = $@"
```

`arguments.sh primeiro segundo terceiro quarto quinto sexto`

---

```text
Nome do arquivo = /home/matheus/Dev/scripts/arguments.sh
Terceiro argumento = terceiro
Sexto argumento = sexto
Número de argumentos = 6
Lista de argumentos = primeiro segundo terceiro quarto quinto sexto
```