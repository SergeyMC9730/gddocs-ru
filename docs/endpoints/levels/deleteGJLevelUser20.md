# deleteGJLevelUser20.php

Удаляет уровень со сервера.

## Параметры

### Требуемые параметры

**accountID** - Айди аккунта автора уровня

**gjp** - [GJP](/topics/encryption/gjp.md) автора уровня

**levelID** - Айди удаляемого уровня

**secret** - Wmfv2898gc9

### Дополнительные параметры

**gameVersion** - 21

**binaryVersion** - 35

**gdw** - 0

## Ответ

Возвращает 1 если удалён, -1 если действие было провалено или уровень не существует.

## Пример

<!-- tabs:start -->

### **Python**

```py
import requests

# С помощью данного кода DevExit удаляет уровень с его айди 62689548

data = {
        "accountID": 173831, # Айди аккаунта DevExit
        "gjp": "********", # Зашифрованный с помощью GJP пароль DevExit
        "levelID": 62689548,
        "secret": "Wmfv2898gc9"
}

req = requests.post("http://boomlings.com/database/deleteGJLevelUser20.php", data=data)
print(req.text)
```

**Ответ**
```py
1
```

<!-- tabs:end -->
