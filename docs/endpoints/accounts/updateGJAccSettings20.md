# updateGJAccSettings20.php

Обновляет настройки аккаунта

## Параметры

### Обязательные параметры

**accountID** - ID аккаунта пользователя

**gjp** - [GJP](/topics/encryption/gjp.md) пользователя

**secret** - Wmfv3899gc9

### Необязательные параметры

**mS** - Кому пользователь разрешает отправлять сообщения: 0 - всем, 1 - только друзьям, и 2 - никому

**frS** - Кому пользователь разрешает отправлять запросы в друзья: 0 - всем, и 1 - никому

**cS** - Кому пользователь разрешает смотреть в историю его комментариев: 0 - всем, 1 - только друзьям, и 2 - никому

**yt** - Конец ссылки на YouTube канал пользователя, тоесть то, что идет после `/channel/`. Например `UCZoN2WLAooS6uhREa9Cgpwg`

**twitter** - Тег пользователя в X.

**twitch** - Имя в twitch

## Ответ

1, если требуемые параметры одобрены, даже если ничего не обновляется, иначе -1

## Пример

<!-- tabs:start -->

### **Python**

```py
import requests

data = {
    "accountID": 173831, # ID аккаунта DevExit
    "gjp": "********", # Это пароль аккаунта DevExit, зашифрованный через GJP
    "secret": "Wmfv3899gc9",
    "mS": 0,
    "frS": 0,
    "cS": 0,
    "yt": "UCZoN2WLAooS6uhREa9Cgpwg",
    "twitter": "DevExit",
    "twitch": "devexit"
}

req = requests.post('https://www.boomlings.com/database/updateGJAccSettings20.php', data=data)
print(req.text)
```

**Ответ**
```py
1
```

<!-- tabs:end -->