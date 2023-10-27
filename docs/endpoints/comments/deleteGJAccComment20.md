# deleteGJAccComment20.php

Удаляет комментарий под профилем

## Параметры

### Обязательные параметры

**accountID** - ID аккаунта пользователя

**gjp** - [GJP](/topics/encryption/gjp.md) пользователя

**commentID** - ID комментария, который будет удалён (Возвращается от [uploadGJAccComment20](/endpoints/uploadGJAccComment20.md))

**secret** - Wmfd2893gb7

### Необязательные параметры

**gameVersion** - 21

**binaryVersion** - 35

**gdw** - 0

## Ответ

1, если комментарий был удалён, -1, если произошла ошибка

## Пример

<!-- tabs:start -->

### **Python**

```py
import requests

# Этот код удалит комментарий от DevExit с ID 1772717
# (на самом деле не удалит потому что надо очистить User-Agent)

data = {
    "accountID": 173831, # ID аккаунта DevExit
    "gjp": "********", # Это пароль аккаунта DevExit, зашифрованный через GJP
    "commentID": 1772717,
    "secret": "Wmfd2893gb7"
}

r = requests.post('https://www.boomlings.com/database/deleteGJAccComment20.php', data=data)
print(req.text)
```

**Ответ**
```py
1
```

<!-- tabs:end -->