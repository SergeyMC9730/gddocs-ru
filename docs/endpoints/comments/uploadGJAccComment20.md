# uploadGJAccComment20.php

Добавляет комментарий под профилем

## Параметры

### Обязательные параметры

**accountID** - ID аккаунта пользователя, который хочет отправить комментарий

**gjp** - [GJP](/topics/encryption/gjp.md) пользователя, который хочет отправить комментарий

**comment** - Текст комментария, конвертированный в [URL-safe base64](/topics/encryption/base64).

**secret** - Wmfd2893gb7

### Необязательные параметры

**gameVersion** - 21

**binaryVersion** - 35

**gdw** - 0

**cType** - Тип комментария, 0 - под уровнем, 1 под профилем (что?)

[**chk**](/topics/encryption/chk?id=comment) - Неуверен.

## Ответ

Возвращает ID комментария под профилем, если он был успешно отправлен или ошибку 500, если комментарий не может быть отправлен

## Пример

<!-- tabs:start -->

### **Python**

```py
import requests

data = {
    "accountID": 173831, # ID аккаунта DevExit
    "gjp": "********", # Это пароль аккаунта DevExit, зашифрованный через GJP
    "comment": base64.b64encode(b"This comment was uploaded for the GD Docs!").decode(),
    "secret": "Wmfd2893gb7",
}

r = requests.post('http://boomlings.com/database/uploadGJAccComment20.php', data=data)
print(req.text)
```

**Ответ**
```py
1772719
```

<!-- tabs:end -->
