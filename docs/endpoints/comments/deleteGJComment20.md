# deleteGJComment20.php

Удаляет комментарий под уровнем

## Параметры

### Обязательные параметры

**accountID** - ID аккаунта пользователя, который удаляет комментарий

**gjp** - [GJP](/topics/encryption/gjp.md) пользователя, который удаляет комментарий

**commentID** - ID комментария

**levelID** - ID уровня, под которым находится комментарий

**secret** - Wmfd2893gb7

### Необязательные параметры

**gameVersion** - 21

**binaryVersion** - 35

**gdw** - 0

## Ответ

Возвращает 1, если комментарий удален, иначе -1.

## Пример

<!-- tabs:start -->

### **Python**

```py
import requests

# Этот код удалит комментарий DevExit с ID 31415926

data = {
        "accountID": 173831, # ID аккаунта DevExit
        "gjp": "********", # Это пароль аккаунта DevExit, зашифрованный через GJP
        "commentID": 31415926,
        "levelID": 54953085,
        "secret": "Wmfd2893gb7"
}

req = requests.post("https://www.boomlings.com/database/deleteGJComment20.php", data=data)
print(req.text)
```

**Ответ**
```py
1
```

<!-- tabs:end -->