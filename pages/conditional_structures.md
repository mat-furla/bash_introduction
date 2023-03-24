## Estruturas Condicionais

---

### if else

---

```bash {all|1,5|2|3|4|all}
if [[ arg1 operador arg2 ]]; then
  código se expressão = true
else
  código se expressão = false
fi
```

---

```bash {all|1,7|2|3|4|5|6|all}
if [[ arg1 operador arg2 ]]; then
  expressão = true
elif [[ arg3 operador arg4 ]]; then
  expressão = true
else
  expressão = false
fi
```

---

<v-clicks>

 - A expressão colocada entre `[[ ]]` é avalidada como `true` ou `false`
 - A expressão pode ser uma simples string, número ou variável
 - Uma string somente com espaços ou uma variável indefinida serão avaliadas como falsas
 - A expressão pode ser uma combinação de operadores
 - Existem diversos operadores para operações: lógicas, numéricas, com string e com arquivos

</v-clicks>

---

| **Operações lógicas** | **Operador** |
| --------------------- | ------------ |
| Not                   | `! $a`       |
| And                   | `$a && $b`   |
| Or                    | `$a \|\| $b` |

---

| **Operações com números** | **Operador** |
| ------------------------- | ------------ |
| Maior                     | `$a -gt $b`  |
| Menor                     | `$a -lt $b`  |
| Maior igual               | `$a -ge $b`  |
| Menor igual               | `$a -le $b`  |
| Igual                     | `$a -eq $b`  |
| Não é igual               | `$a -ne $b`  |

---

| **Operações com strings** | **Operador** |
| ------------------------- | ------------ |
| Igual                     | `$a = $b`    |
| Igual                     | `$a == $b`   |
| Diferente                 | `$a != $b`   |
| String vazia              | `-z $a`      |

---

| **Operações com arquivos**                 | **Operador** |
| ------------------------------------------ | ------------ |
| Arquivo existe                             | `-e $file`   |
| Arquivo existe e não está vazio            | `-s $file`   |
| Arquivo existe e é um arquivo normal       | `-f $file`   |
| Arquivo existe e tem permissão de escrita  | `-w $file`   |
| Arquivo existe e tem permissão de execução | `-x $file`   |
| Arquivo existe e é diretório               | `-d $file`   |

---

```bash {all|1|3-4|5-6|7-9|all}
subscription="TU"

if [[ "$subscription" == "TU" ]]; then
  echo "A subscription é OPENBANKING_TU"
elif [[ "$subscription" == "TH" ]]; then
  echo "A subscription é OPENBANKING_TH"
else
  echo "A subscription é OPENBANKING_PR"
fi
```

---

```bash {all|1-2|4-5|6-8|all}
read -p "Digite um número: " number
echo "O número digitado é $number"

if [[ $number -gt 100 ]]; then
  echo "O número é maior que 100"
else
  echo "O número digitado é menor que 100"
fi
```

---

#### Diferenças entre `[ ]` e `[[ ]]`

---

<v-clicks>

 - Strings com espaços
 - Expansão em nomes de arquivos
 - Melhor combinação entre operadores

</v-clicks>

---

```bash {all}
if [ $stringcomespaco != foo ]; then
```

```bash {all}
if [[ $stringcomespaco != foo ]]; then
```

---

```bash {all}
if [ -a *.sh ]; then
```

```bash {all}
if [[ -a *.sh ]]; then
```

---

```bash
if [[ $num -eq 3 && "$string" == foo ]]; then
```

---

### case

---

```bash {all|1,11|2-4|5-7|8-10|all}
case "$variavel" in
  "$condicao1")
    comando...
  ;;
  "$condicao2")
    comando...
  ;;
  *)
    comando...
  ;;
esac
```

---

```bash {all|1|2,8|3-7|all}
opcao=1
case $opcao in
    1) echo "KEYVAULT";;
    2) echo "ACR";;
    3) echo "AKS";;
    4) echo "VM";;
    5) exit
esac
```
