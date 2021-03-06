---
title: payments.validateRequestedInfo
description: payments.validateRequestedInfo parameters, return type and example
---
## Method: payments.validateRequestedInfo  
[Back to methods index](index.md)


### Parameters:

| Name     |    Type       | Required |
|----------|:-------------:|---------:|
|save|[Bool](../types/Bool.md) | Optional|
|msg\_id|[int](../types/int.md) | Yes|
|info|[PaymentRequestedInfo](../types/PaymentRequestedInfo.md) | Yes|


### Return type: [payments\_ValidatedRequestedInfo](../types/payments_ValidatedRequestedInfo.md)

### Example:


```
$MadelineProto = new \danog\MadelineProto\API();
if (isset($token)) { // Login as a bot
    $MadelineProto->bot_login($token);
}
if (isset($number)) { // Login as a user
    $sentCode = $MadelineProto->phone_login($number);
    echo 'Enter the code you received: ';
    $code = '';
    for ($x = 0; $x < $sentCode['type']['length']; $x++) {
        $code .= fgetc(STDIN);
    }
    $MadelineProto->complete_phone_login($code);
}

$payments_ValidatedRequestedInfo = $MadelineProto->payments->validateRequestedInfo(['save' => Bool, 'msg_id' => int, 'info' => PaymentRequestedInfo, ]);
```

Or, if you're using the [PWRTelegram HTTP API](https://pwrtelegram.xyz):

### As a bot:

POST/GET to `https://api.pwrtelegram.xyz/botTOKEN/madeline`

Parameters:

* method - payments.validateRequestedInfo
* params - `{"save": Bool, "msg_id": int, "info": PaymentRequestedInfo, }`



### As a user:

POST/GET to `https://api.pwrtelegram.xyz/userTOKEN/payments.validateRequestedInfo`

Parameters:

save - Json encoded Bool
msg_id - Json encoded int
info - Json encoded PaymentRequestedInfo



Or, if you're into Lua:

```
payments_ValidatedRequestedInfo = payments.validateRequestedInfo({save=Bool, msg_id=int, info=PaymentRequestedInfo, })
```

