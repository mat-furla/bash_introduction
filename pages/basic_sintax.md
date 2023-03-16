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
|----------------|-------|-------|--------|
| Read( r )      | 4     |       |        |
| Write( w )     | 2     | 2     | 2      |
| Execution( x ) | 1     | 1     | 1      |
| **Total**      | **7** | **5** | **5**  |

---

### Permissões

|                | Owner | Group | Others |
|----------------|-------|-------|--------|
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

