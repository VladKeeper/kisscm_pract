# Практическое занятие №1. Введение, основы работы в командной строке


## Задача 1
```cut -d: -f1 /etc/passwd |sort```

![image](https://github.com/user-attachments/assets/38aab82b-6af9-4a3a-9969-3ea4c6ed6b36)


## Задача 2
```awk '{print $2, $1}' /etc/protocols | sort -k1,1nr | head -n 5```

![image](https://github.com/user-attachments/assets/cb87d570-0feb-4909-9b24-144e28d0a178)

## Задача 3
```
#!/bin/bash

if [ $# -eq 0 ]; then
    echo "Использование: $0 \"Ваш текст\""
    exit 1
fi

text="$1"

length=${#text}

border=$(printf "%0.s-" $(seq 1 $((length + 2))))

border="+$border+"

echo "$border"
echo "| $text |"
echo "$border"
```            


## Задача 4
```
grep -oE '\b[a-zA-Z_][a-zA-Z0-9_]*\b' test.c | grep -vE '\b(int|void|return|if|else|for|while|include|stdio)\b' | sort | uniq
```


## Задача 5
```
chmod +x reg
sudo cp $1 /usr/local/bin
```
