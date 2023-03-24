## Funções

---

```bash {all|2-4|6|all}
#!/bin/bash
function function_name {
  command...
}

function_name
```

---

```bash {all|7|2-5|all}
#!/bin/bash
function function_name {
  echo $1
  echo $2
}

function_name param1 param2
```

---

```text
param1
param2
```

---

```bash {all|2-7|9|11-12|all}
#!/bin/bash
function function_name {
  var1="$1"
  var2="$2"
  echo $var1
  echo $var2
}

function_name param1 param2

echo $var1
echo $var2
```

---

```text
param1
param2
param1
param2
```

---

```bash {all|2-7|9|11-12|all}
#!/bin/bash
function function_name {
  local var1="$1"
  local var2="$2"
  echo $var1
  echo $var2
}

function_name param1 param2

echo $var1
echo $var2
```

---

```text
param1
param2


```
