# requestUserAccess.php

Requests moderator access

## Parameters

### Required Parameters

**accountID** - The accountID of the user requesting mod access

**gjp** - The [GJP](/topics/encryption/gjp.md) of the user requesting mod access

**secret** - Wmfd2893gb7

### Optional Parameters

**gameVersion** - 21

**binaryVersion** - 35

**gdw** - 0

## Response

1 if granted, -1 if not

## Example

<!-- tabs:start -->

### **Python**

```py
import requests

data = {
    'accountID': 173831, # DevExit's account ID
    'gjp': "********", # This would be DevExit's password encoded with GJP encryption
    "secret": "Wmfd2893gb7"
}

req = requests.post('https://www.boomlings.com/database/requestUserAccess.php', data=data)
print(req.text)
```

**Response**
```py
-1
```

<!-- tabs:end -->