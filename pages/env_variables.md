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
