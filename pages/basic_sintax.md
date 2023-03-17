## Conceitos básicos

---

### Configurando o ambiente

---

### O primeiro script

---

```shell {all|1|2|4|all}
#!/bin/bash
# Description: display hello world

echo "Hello World"
```

`Hello World`

---

### Permissões

|                | Owner | Group | Others |
| -------------- | ----- | ----- | ------ |
| Read( r )      | 4     | 4     | 4      |
| Write( w )     | 2     |       |        |
| Execution( x ) | 1     | 1     | 1      |
| **Total**      | **7** | **5** | **5**  |

---

### Permissões

|                | Owner | Group | Others |
| -------------- | ----- | ----- | ------ |
| Read( r )      | 4     | 4     | 4      |
| Write( w )     | 2     |       |        |
| Execution( x ) |       |       |        |
| **Total**      | **6** | **4** | **4**  |

---

### Variáveis

---

```shell {all|4|6|all}
#!/bin/bash
# Description: show image name

image_name="openbankingdevops/hello-world"

echo "O nome da imagem é: $image_name"
```

`O nome da imagem é: openbankingdevops/hello-world`

---

<v-clicks>

 - Podem conter números, um caracter ou uma string de caracteres
 - São case-sensitive
 - O caracter `\` pode ser usado para dar escape em caracteres especiais

</v-clicks>

---

<v-clicks>

 - <emojione-cross-mark-button /> Iniciar com números `1image_name`
 - <emojione-cross-mark-button /> Conter "-" `image-name`
 - <emojione-cross-mark-button /> Conter "@" `image@name`

</v-clicks>

---

```shell {all|6|all}
#!/bin/bash
# Description: show image name

image_name="openbankingdevops/hello-world"

echo 'O nome da imagem é: $image_name'
```

`O nome da imagem é: $image_name`

---

```shell {all|6|all}
#!/bin/bash
# Description: show image name

image_name="openbankingdevops/hello-world"

echo "O nome da imagem é: ${image_name}"
```

`O nome da imagem é: openbankingdevops/hello-world`

---

```shell {all|6|all}
#!/bin/bash
# Description: show image name

image_name="openbankingdevops/hello-world"

echo "O nome da imagem é: ${image_name}:1.0.0"
```

`O nome da imagem é: openbankingdevops/hello-world:1.0.0`

---

```shell {all|4|6|all}
#!/bin/bash
# Description: get az subscription name

subscription_name="$(az account show --query name)"

echo "O nome da subscription atual é: ${subscription_name}"
```

`O nome da subscription atual é: "Plataforma - DevOps"`

---

```shell {all|4|all}
#!/bin/bash
# Description: get az subscription name

subscription_name=`az account show --query name`

echo "O nome da subscription atual é: ${subscription_name}"
```

`O nome da subscription atual é: "Plataforma - DevOps"`

---

```shell {all|4|all}
#!/bin/bash
# Description: get user input and echo value

read -p "Digite o nome da imagem: " image_name

echo "O nome da imagem é: ${image_name}"
```

`O nome da imagem é: openbankingdevops/hello-world:1.0.0`

---

### Variáveis de Ambiente

---

<v-clicks>

 - Forma simples de passar informação entre o ambiente e o programa sendo executado
 - Array de strings no formato de `chave=valor`
 - Exemplos: `$PATH` e `$HOME`

</v-clicks>

---

<v-clicks>

 - Podem ser configuradas em runtime através de `declare -x` ou `export`  
 - Edição do arquivo `.bashrc`
 - `TZ=UTC date`

</v-clicks>

---

`export` 

<v-clicks>

 - Listar: `export [-p]`
 - Adicionar: `export CHAVE=VALOR`
 - Remover: `export -n CHAVE`

</v-clicks>

---

`declare`

<v-clicks>

 - Listar: `declare [-p]`
 - Adicionar: `declare -x CHAVE=VALOR`
 - Remover: `declare +x CHAVE`

</v-clicks>

---

<v-clicks>

 - `set`: listar ou exportar variáveis
 - `unset`: remover variável
 - `printenv`: listar variáveis

</v-clicks>

---

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

```shell {all|4|5|7|9|10|11|12}
#!/bin/bash
# Description: example using arguments

echo "Nome do arquivo = $0"
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

---

### Arrays

---

