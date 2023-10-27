# getGJAccountComments20.php

Получает комментарии под профилем пользователя.

## Параметры

### Обязательные параметры

**accountID** - ID аккаунта, комментарии которого вы хотите получить

**page** - Какую страницу комментариев вы хотите увидеть

**secret** - Wmfd2893gb7

### Необязательные параметры

**gameVersion** - 21

**binaryVersion** - 35

**gdw** - 0

**total** - Не понятно используется ли это или нет. Обычно этот параметр является количеством комментариев под профилем пользователя, но если значение будет 0, то это все равно сработает.

## Ответ

Возвращает список [комментариев](/resources/server/comment.md), которые разделены через `|`.

## Пример

<!-- tabs:start -->

### **Python**

```py
import requests

# Этот код вернёт комментарии под профилем DevExit

data = {
    "accountID": 173831, # ID аккаунта DevExit
    "page": 0,
    "secret": "Wmfd2893gb7"
}

req = requests.post("https://www.boomlings.com/database/getGJAccountComments20.php", data=data)
print(req.text)
```

**Ответ**
```py
2~NTAwMCBzdGFycyE=~4~9~9~2 months~6~1756926|2~Qmxvb2RiYXRoIEdHISEh~4~19~9~6 months~6~1745624|2~QWxsZWdpYW5jZSAxMDAl~4~2~9~6 months~6~1744292|2~SUNEWCAxMDAlIDop~4~1~9~6 months~6~1743608|2~T2ggeWVhaCBDYXRhIGFuZCBUVVAgMTAwJQ==~4~1~9~7 months~6~1742661|2~Mi4xMSBpcyBvdXQgOik=~4~43~9~2 years~6~1295890|2~SSBsaWtlIGhvdyBzb21lb25lIGRpc2xpa2UgYm90dGVkIG1vc3Qgb2YgbXkgY29tbWVudHMgOikgU2hvd3MgdGhhdCBJJ20uLi5mQW1PdVM=~4~16~9~2 years~6~1279970|2~TmVjcm9wb2xpeCBpbiAyMTYgYXR0IGluIHByYWN0aWNl~4~14~9~2 years~6~1264265|2~IkhpIEx1bmEi~4~15~9~3 years~6~1246506|2~TyB3YWl0IG15IDUwdGggZGVtb24gd2FzIGdvaW5nIHRvIGJlIEJ1Y2sgRm9yY2UsIG5vdCByZWFsbHkgY2VsZWJyYXRvcnkuLi4=~4~7~9~3 years~6~1238082#67:0:10
```

<!-- tabs:end -->