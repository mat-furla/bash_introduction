## Estruturas de Repetição

---

### for

---

```bash {all|2,4|3|all}
#!/bin/bash
for arg in [[list]]; do
  command(s)...
done
```

---

```bash {all|2,6|3-5|all}
#!/bin/bash
for var in 1 2 3 4 5 .. N; do
  command1
  command2
  commandN
done
```

---

```bash {all|2,6|3-5|all}
#!/bin/bash
for var in file1 file2 file3; do
  command1 on $var
  command2
  commandN
done
```

---

```bash {all|2,6|3-5|all}
#!/bin/bash
for output in $(command); do
  command1 on $output
  command2 on $output
  commandN
done
```

---

```bash {all|2,4|3|all}
#!/bin/bash
for i in {1..5}; do
  echo "Hello world $i"
done
```

```text
Hello world 1
Hello world 2
Hello world 3
Hello world 4
Hello world 5
```

---

```bash {all|2,4|3|all}
#!/bin/bash
for i in {1..10..2}; do
  echo "Hello world $i"
done
```

```text
Hello world 1
Hello world 3
Hello world 5
Hello world 7
Hello world 9
```

---

```bash {all|2,4|3|all}
#!/bin/bash
for (( i=1; i<=5; i++ )); do
  echo "Hello world $i"
done
```

```text
Hello world 1
Hello world 2
Hello world 3
Hello world 4
Hello world 5
```

---

```bash
#!/bin/bash
names=(Joe Jenny Sara Tony)
for name in ${names[@]} ; do
  echo "Meu nome é $name"
done

for file in $( ls $HOME ) ; do
  echo "Arquivo $file"
done
```

```text
Meu nome é Joe
Meu nome é Jenny
Meu nome é Sara
Meu nome é Tony
Arquivo: Desktop
Arquivo: Documents
```

---

### while

---

```bash {all|2,4|3|all}
#!/bin/bash
while [[ condition ]]; do
  command(s)...
done
```

---

```bash {all|2|4,7|5-6|all}
#!/bin/bash
i=4

while [[ $i -gt 0 ]]; do
  echo "Valor de i é $i"
  i=$(($i - 1))
done
```

```text
Valor de i é 4
Valor de i é 3
Valor de i é 2
Valor de i é 1
```

---

### until

---

```bash {all|2,4|3|all}
#!/bin/bash
until [[ condition ]]; do
  command(s)...
done
```

---

```bash {all|2|4,7|5-6|all}
#!/bin/bash
i=1

until [[ $i -gt 5 ]]; do
  echo "Valor de i é $i"
  i=$(($i + 1))
done
```

---

### break, continue

---

```bash
#!/bin/bash
i=0

while [[ $i -ge 0 ]]; do
  echo "Valor de i é: $i"
  i=$((i+1))

  if [[ $i -ge 5 ]]; then
    break
  fi
done
```

---

```text
Valor de i é: 0
Valor de i é: 1
Valor de i é: 2
Valor de i é: 3
Valor de i é: 4
```

---

```bash
#!/bin/bash
i=0

while [ $i -lt 10 ]; do
  i=$((i+1))

  if [ $(($i % 2)) = 0 ] ; then
    continue
  fi

  echo "Valor de i é $i"
done
```

---

```text
Valor de i é 1
Valor de i é 3
Valor de i é 5
Valor de i é 7
Valor de i é 9
```