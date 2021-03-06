---
title: passwordState
description: Represents current state of the two-step verification
---
## Constructor: passwordState  
[Back to constructors index](index.md)



Represents current state of the two-step verification

### Attributes:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|
|has\_password|[Bool](../types/Bool.md) | Yes|Is password set up|
|password\_hint|[string](../types/string.md) | Yes|Hint on password, can be empty|
|has\_recovery\_email|[Bool](../types/Bool.md) | Yes|Is recovery email set up|
|unconfirmed\_recovery\_email\_pattern|[string](../types/string.md) | Yes|Pattern of email to which confirmation mail was sent|



### Type: [PasswordState](../types/PasswordState.md)


### Example:

```
$passwordState = ['_' => 'passwordState', 'has_password' => Bool, 'password_hint' => 'string', 'has_recovery_email' => Bool, 'unconfirmed_recovery_email_pattern' => 'string'];
```  

[PWRTelegram](https://pwrtelegram.xyz) json-encoded version:

```
{"_": "passwordState", "has_password": Bool, "password_hint": "string", "has_recovery_email": Bool, "unconfirmed_recovery_email_pattern": "string"}
```


Or, if you're into Lua:  


```
passwordState={_='passwordState', has_password=Bool, password_hint='string', has_recovery_email=Bool, unconfirmed_recovery_email_pattern='string'}

```


