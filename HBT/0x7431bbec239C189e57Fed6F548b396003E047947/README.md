# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7431bbec239C189e57Fed6F548b396003E047947`.

The ordered steps of contract function invocations are included below and in
the corresponding [steps.json](./steps.json). Please read [the general recipe
for settling Nahmii 1 balance](../../README.md) before starting on the first
step of settlement.

## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000004eceb6d0000000000000000000000000000000000000000000000000000000004eceb6d0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004eceb6d0000000000000000000000000000000000000000000000000000000004eceb6d07d18ac6e3fb80a6763777687e52554ee961747421a6ffc6b4e4a6a1fe6a7a3af4dc8905be74498bd998bbfb072c9ee7ae87bb979f6b545ebdcdbbf8bb7452e403d1d347ba62605a47aa57f82bb0b39e9cbf8235d8b62a49a24815ece7e5d9d64000000000000000000000000000000000000000000000000000000000000001b42e9b2144cc6a118cba830a6c8a845439c26420e3ac0b96073ffffd5a893bbbda09ed93f8cfdcc48f9d7547b45be6d3375f07629f1438feedb819b25c14636062c098e416ea6cb7593b9cad0247b57a7163e835bafc02bd1beeb5912fb2c1a85000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56850000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000182800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1aeb3e7835e7000000000000000000000000000000000000000000000000002e1aeb8d5b197100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000142cba000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000095e07a5fd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a57597a4f5441354e7930354d4755774c5455774f445174596a6b354f53316a596d566b4d324e684e474e694e32496966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000007431bbec239c189e57fed6f548b396003e047947000000000000000000000000000000000000000000000000000000004eceb6d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7d18ac6e3fb80a6763777687e52554ee961747421a6ffc6b4e4a6a1fe6a7a3af",
      "signature": {
        "s": "0x3d1d347ba62605a47aa57f82bb0b39e9cbf8235d8b62a49a24815ece7e5d9d64",
        "r": "0x4dc8905be74498bd998bbfb072c9ee7ae87bb979f6b545ebdcdbbf8bb7452e40",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x42e9b2144cc6a118cba830a6c8a845439c26420e3ac0b96073ffffd5a893bbbd",
      "signature": {
        "s": "0x2c098e416ea6cb7593b9cad0247b57a7163e835bafc02bd1beeb5912fb2c1a85",
        "r": "0xa09ed93f8cfdcc48f9d7547b45be6d3375f07629f1438feedb819b25c1463606",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1322170064",
    "total": "1322170064"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1322170064",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "40232265213"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1322170"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZWYzOTA5Ny05MGUwLTUwODQtYjk5OS1jYmVkM2NhNGNiN2IifQ==",
    "nonce": 6184,
    "balances": {
      "current": "12977446596392423",
      "previous": "12977447919884657"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7431bbec239c189e57fed6f548b396003e047947",
    "nonce": 22,
    "balances": {
      "current": "1322170064",
      "previous": "0"
    }
  },
  "blockNumber": "10114693",
  "created": "2020-05-22T08:47:11.134Z",
  "updated": "2020-05-22T08:47:11.203Z",
  "id": "5ec7918fb0c6090011d5b0d4"
}
```
* *stageAmount*: `1322170064`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000004eceb6d0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004eceb6d0000000000000000000000000000000000000000000000000000000004eceb6d07d18ac6e3fb80a6763777687e52554ee961747421a6ffc6b4e4a6a1fe6a7a3af4dc8905be74498bd998bbfb072c9ee7ae87bb979f6b545ebdcdbbf8bb7452e403d1d347ba62605a47aa57f82bb0b39e9cbf8235d8b62a49a24815ece7e5d9d64000000000000000000000000000000000000000000000000000000000000001b42e9b2144cc6a118cba830a6c8a845439c26420e3ac0b96073ffffd5a893bbbda09ed93f8cfdcc48f9d7547b45be6d3375f07629f1438feedb819b25c14636062c098e416ea6cb7593b9cad0247b57a7163e835bafc02bd1beeb5912fb2c1a85000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56850000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000182800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1aeb3e7835e7000000000000000000000000000000000000000000000000002e1aeb8d5b197100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000142cba000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000095e07a5fd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a57597a4f5441354e7930354d4755774c5455774f445174596a6b354f53316a596d566b4d324e684e474e694e32496966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000007431bbec239c189e57fed6f548b396003e047947000000000000000000000000000000000000000000000000000000004eceb6d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7d18ac6e3fb80a6763777687e52554ee961747421a6ffc6b4e4a6a1fe6a7a3af",
      "signature": {
        "s": "0x3d1d347ba62605a47aa57f82bb0b39e9cbf8235d8b62a49a24815ece7e5d9d64",
        "r": "0x4dc8905be74498bd998bbfb072c9ee7ae87bb979f6b545ebdcdbbf8bb7452e40",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x42e9b2144cc6a118cba830a6c8a845439c26420e3ac0b96073ffffd5a893bbbd",
      "signature": {
        "s": "0x2c098e416ea6cb7593b9cad0247b57a7163e835bafc02bd1beeb5912fb2c1a85",
        "r": "0xa09ed93f8cfdcc48f9d7547b45be6d3375f07629f1438feedb819b25c1463606",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1322170064",
    "total": "1322170064"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1322170064",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "40232265213"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1322170"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZWYzOTA5Ny05MGUwLTUwODQtYjk5OS1jYmVkM2NhNGNiN2IifQ==",
    "nonce": 6184,
    "balances": {
      "current": "12977446596392423",
      "previous": "12977447919884657"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7431bbec239c189e57fed6f548b396003e047947",
    "nonce": 22,
    "balances": {
      "current": "1322170064",
      "previous": "0"
    }
  },
  "blockNumber": "10114693",
  "created": "2020-05-22T08:47:11.134Z",
  "updated": "2020-05-22T08:47:11.203Z",
  "id": "5ec7918fb0c6090011d5b0d4"
}
```
* *standard*: `ERC20`
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b000000000000000000000000000000000000000000000000000000004eceb6d0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1322170064`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`