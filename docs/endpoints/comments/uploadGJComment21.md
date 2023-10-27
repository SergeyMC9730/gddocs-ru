# uploadGJComment21.php

Добавляет комментарий под уровнем.

## Параметры

### Обязательные параметры

**accountID** - ID аккаунта комментатора

**gjp** - [GJP](/topics/encryption/gjp.md) комментатора

**userName** - Имя комментатора

**comment** - Текст комментария, конвертированный в [URL-safe base64](/topics/encryption/base64)

**secret** - Wmfd2893gb7

**levelID** - ID уровня, под которым будет комментарий

**percent** - Прогресс уровня, который будет показан в комментарии

[**chk**](/topics/encryption/chk) - `userName` + `comment` + `levelID` + `percent`

### Необязательные параметры

**gameVersion** - 21

**binaryVersion** - 35

**gdw** - 0

## Ответ

Возвращает ID отправленного комментария или `-1`, если запрос отклонён.

## Пример

<!-- tabs:start -->

### **Python**

```py
import requests

# Этот код выложит комментарий от DevExit с текстом "Hello from the GDDocs!" под уровнем 62687277

chk = generate_chk(key="29481", values=["devexit", "SGVsbG8gZnJvbSB0aGUgR0REb2NzIQ==", 62687277, 69], salt="0xPT6iUrtws0J")
# Эти значения могут быть найдены в страницах про XOR и CHK

data = {
    "accountID": 173831, # ID аккаунта DevExit
    "gjp": "********", # Это пароль аккаунта DevExit, зашифрованный через GJP
    "userName": "devexit",
    "comment": "SGVsbG8gZnJvbSB0aGUgR0REb2NzIQ==", # "Hello from the GDDocs!"
    "levelID": 62687277,
    "percent": 69,
    "chk": chk,
    "secret": "Wmfd2893gb7"
}

req = requests.post("https://www.boomlings.com/database/uploadGJComment21.php", data=data)
print(req.text)
```

**Ответ**
```py
31444784
```

<!-- tabs:end -->
