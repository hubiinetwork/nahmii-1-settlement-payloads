# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xB6fe1657F40A3D695D36C3B1f727286E504d42C2`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000073a5938e0000000000000000000000000000000000000000000000000000000073a5938e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000073a5938e0000000000000000000000000000000000000000000000000000000073a5938e5fedc237cb8d0de87528c0339a14fb048b603e652b929e9d927cd1f949f749439b1df59970eeb0a0521b738cd9440a67d2b7087013fba40fa9d6f280fc7c22db65edcbf9bce4559c8f26aace8007d8743dbd1625261576d722d0bc850cec8df8000000000000000000000000000000000000000000000000000000000000001ca381d86dd2d1c46605f9ae6031188e93812c0035b80737342df107541c924bffe4e6808874d3c53c0442a151d843c2f13f7976f37fcd9cfa25c8eba842eaf89e3de7a029fa58ff29c3f5224bbe12a7df7fc437597796fffd6286644278c115fe000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56a700000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b7c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e157036325f54000000000000000000000000000000000000000000000000002e1570a9f58de900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001d9b07000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ac4d8e95b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e6d5135595745345969307a5a474d774c5455324e324d74595455305a6930774e5455314e446c6d4d4749304f44416966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000b6fe1657f40a3d695d36c3b1f727286e504d42c20000000000000000000000000000000000000000000000000000000073a5938e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5fedc237cb8d0de87528c0339a14fb048b603e652b929e9d927cd1f949f74943",
      "signature": {
        "s": "0x65edcbf9bce4559c8f26aace8007d8743dbd1625261576d722d0bc850cec8df8",
        "r": "0x9b1df59970eeb0a0521b738cd9440a67d2b7087013fba40fa9d6f280fc7c22db",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa381d86dd2d1c46605f9ae6031188e93812c0035b80737342df107541c924bff",
      "signature": {
        "s": "0x3de7a029fa58ff29c3f5224bbe12a7df7fc437597796fffd6286644278c115fe",
        "r": "0xe4e6808874d3c53c0442a151d843c2f13f7976f37fcd9cfa25c8eba842eaf89e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1940231054",
    "total": "1940231054"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1940231054",
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
            "amount": "46252222811"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1940231"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzNmQ5YWE4Yi0zZGMwLTU2N2MtYTU0Zi0wNTU1NDlmMGI0ODAifQ==",
    "nonce": 7036,
    "balances": {
      "current": "12971420618481492",
      "previous": "12971422560652777"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb6fe1657f40a3d695d36c3b1f727286e504d42c2",
    "nonce": 22,
    "balances": {
      "current": "1940231054",
      "previous": "0"
    }
  },
  "blockNumber": "10114727",
  "created": "2020-05-22T08:53:37.437Z",
  "updated": "2020-05-22T08:53:37.506Z",
  "id": "5ec79311005df800101bcb6a"
}
```
* *stageAmount*: `1940231054`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000073a5938e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000073a5938e0000000000000000000000000000000000000000000000000000000073a5938e5fedc237cb8d0de87528c0339a14fb048b603e652b929e9d927cd1f949f749439b1df59970eeb0a0521b738cd9440a67d2b7087013fba40fa9d6f280fc7c22db65edcbf9bce4559c8f26aace8007d8743dbd1625261576d722d0bc850cec8df8000000000000000000000000000000000000000000000000000000000000001ca381d86dd2d1c46605f9ae6031188e93812c0035b80737342df107541c924bffe4e6808874d3c53c0442a151d843c2f13f7976f37fcd9cfa25c8eba842eaf89e3de7a029fa58ff29c3f5224bbe12a7df7fc437597796fffd6286644278c115fe000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56a700000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b7c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e157036325f54000000000000000000000000000000000000000000000000002e1570a9f58de900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001d9b07000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ac4d8e95b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e6d5135595745345969307a5a474d774c5455324e324d74595455305a6930774e5455314e446c6d4d4749304f44416966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000b6fe1657f40a3d695d36c3b1f727286e504d42c20000000000000000000000000000000000000000000000000000000073a5938e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5fedc237cb8d0de87528c0339a14fb048b603e652b929e9d927cd1f949f74943",
      "signature": {
        "s": "0x65edcbf9bce4559c8f26aace8007d8743dbd1625261576d722d0bc850cec8df8",
        "r": "0x9b1df59970eeb0a0521b738cd9440a67d2b7087013fba40fa9d6f280fc7c22db",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa381d86dd2d1c46605f9ae6031188e93812c0035b80737342df107541c924bff",
      "signature": {
        "s": "0x3de7a029fa58ff29c3f5224bbe12a7df7fc437597796fffd6286644278c115fe",
        "r": "0xe4e6808874d3c53c0442a151d843c2f13f7976f37fcd9cfa25c8eba842eaf89e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1940231054",
    "total": "1940231054"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1940231054",
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
            "amount": "46252222811"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1940231"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzNmQ5YWE4Yi0zZGMwLTU2N2MtYTU0Zi0wNTU1NDlmMGI0ODAifQ==",
    "nonce": 7036,
    "balances": {
      "current": "12971420618481492",
      "previous": "12971422560652777"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb6fe1657f40a3d695d36c3b1f727286e504d42c2",
    "nonce": 22,
    "balances": {
      "current": "1940231054",
      "previous": "0"
    }
  },
  "blockNumber": "10114727",
  "created": "2020-05-22T08:53:37.437Z",
  "updated": "2020-05-22T08:53:37.506Z",
  "id": "5ec79311005df800101bcb6a"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000073a5938e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1940231054`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`