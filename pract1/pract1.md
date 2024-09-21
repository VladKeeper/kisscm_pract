# Практическое занятие №1. Введение, основы работы в командной строке


## Задача 1
```cut -d: -f1 /etc/passwd |sort```

![image](https://github.com/user-attachments/assets/f62e9261-3ac1-4b8c-8d00-e86ebce73acf)


## Задача 2
```awk '{print $2, $1}' /etc/protocols | sort -k1,1nr | head -n 5```

![image](https://github.com/user-attachments/assets/cb87d570-0feb-4909-9b24-144e28d0a178)

## Задача 3
```
#!/bin/bash

text=$*
length=${#text}

for i in $(seq 1 $((length + 2))); do
    line+="-"
done

echo "+${line}+"
echo "| ${text} |"
echo "+${line}+"
```            

![image](https://github.com/user-attachments/assets/e43cd7ea-2b8b-4532-a65e-270b7be1c2d9)

## Задача 4
```
grep -oE '\b[a-zA-Z_][a-zA-Z0-9_]*\b' test.c | grep -vE '\b(int|void|return|if|else|for|while|include|stdio)\b' | sort | uniq
```

![image](https://github.com/user-attachments/assets/cb62abdb-9e09-4670-8c89-05df285cdb66)


## Задача 5
```
chmod +x reg
ls /usr/local/bin
```

![image](https://github.com/user-attachments/assets/1360e919-9dac-4deb-9091-c833c97f9ef4)
