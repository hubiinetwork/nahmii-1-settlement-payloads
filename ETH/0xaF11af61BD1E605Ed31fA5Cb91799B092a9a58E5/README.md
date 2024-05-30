# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xaF11af61BD1E605Ed31fA5Cb91799B092a9a58E5`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000013af00000000000000000000000000000000000000000000000000000000000013af000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000013af00000000000000000000000000000000000000000000000000000000000013af591cad6c18b4652602721e78694fec022bc69d87b69a6e8c8a671c42d282abe075c55e353a3f9f6b049b98b9e8bdc96c3a0095504f7f3cbebf3fe1264c10555541643b4471807252aee88a7f3b3ca2a4a70adfd4118445fbb204e916d05a9bb1000000000000000000000000000000000000000000000000000000000000001bf470fda9ad346151df16133a4a0dde29ad0fe16b7e257106cc2881e4a5b0acbddaa49d665e00f39742b41ce685048dfad4b33fb9ab779f4e6f97b0161b405a123d845b11217d33bbdb5d7e652bf09ff311b0970ef4dfa63adc0fca33bbfa7428000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55da000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004db00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7e1ddef000000000000000000000000000000000000000000000000002386f2c7e1f1a300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000005000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000093ba400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d3245345a544d335a43316b596d5a6a4c545532595751744f4451334f4330354d574d785a544a6859574d35596a6b6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000af11af61bd1e605ed31fa5cb91799b092a9a58e500000000000000000000000000000000000000000000000000000000000013af000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x591cad6c18b4652602721e78694fec022bc69d87b69a6e8c8a671c42d282abe0",
      "signature": {
        "s": "0x41643b4471807252aee88a7f3b3ca2a4a70adfd4118445fbb204e916d05a9bb1",
        "r": "0x75c55e353a3f9f6b049b98b9e8bdc96c3a0095504f7f3cbebf3fe1264c105555",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf470fda9ad346151df16133a4a0dde29ad0fe16b7e257106cc2881e4a5b0acbd",
      "signature": {
        "s": "0x3d845b11217d33bbdb5d7e652bf09ff311b0970ef4dfa63adc0fca33bbfa7428",
        "r": "0xdaa49d665e00f39742b41ce685048dfad4b33fb9ab779f4e6f97b0161b405a12",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5039",
    "total": "5039"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5039",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "605092"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "5"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3M2E4ZTM3ZC1kYmZjLTU2YWQtODQ3OC05MWMxZTJhYWM5YjkifQ==",
    "nonce": 1243,
    "balances": {
      "current": "10000001478548975",
      "previous": "10000001478554019"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xaf11af61bd1e605ed31fa5cb91799b092a9a58e5",
    "nonce": 20,
    "balances": {
      "current": "5039",
      "previous": "0"
    }
  },
  "blockNumber": "10114522",
  "created": "2020-05-22T08:07:51.406Z",
  "updated": "2020-05-22T08:07:51.473Z",
  "id": "5ec78857005df800101bc3c2"
}
```
* *stageAmount*: `5039`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000013af000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000013af00000000000000000000000000000000000000000000000000000000000013af591cad6c18b4652602721e78694fec022bc69d87b69a6e8c8a671c42d282abe075c55e353a3f9f6b049b98b9e8bdc96c3a0095504f7f3cbebf3fe1264c10555541643b4471807252aee88a7f3b3ca2a4a70adfd4118445fbb204e916d05a9bb1000000000000000000000000000000000000000000000000000000000000001bf470fda9ad346151df16133a4a0dde29ad0fe16b7e257106cc2881e4a5b0acbddaa49d665e00f39742b41ce685048dfad4b33fb9ab779f4e6f97b0161b405a123d845b11217d33bbdb5d7e652bf09ff311b0970ef4dfa63adc0fca33bbfa7428000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55da000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004db00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7e1ddef000000000000000000000000000000000000000000000000002386f2c7e1f1a300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000005000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000093ba400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d3245345a544d335a43316b596d5a6a4c545532595751744f4451334f4330354d574d785a544a6859574d35596a6b6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000af11af61bd1e605ed31fa5cb91799b092a9a58e500000000000000000000000000000000000000000000000000000000000013af000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x591cad6c18b4652602721e78694fec022bc69d87b69a6e8c8a671c42d282abe0",
      "signature": {
        "s": "0x41643b4471807252aee88a7f3b3ca2a4a70adfd4118445fbb204e916d05a9bb1",
        "r": "0x75c55e353a3f9f6b049b98b9e8bdc96c3a0095504f7f3cbebf3fe1264c105555",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf470fda9ad346151df16133a4a0dde29ad0fe16b7e257106cc2881e4a5b0acbd",
      "signature": {
        "s": "0x3d845b11217d33bbdb5d7e652bf09ff311b0970ef4dfa63adc0fca33bbfa7428",
        "r": "0xdaa49d665e00f39742b41ce685048dfad4b33fb9ab779f4e6f97b0161b405a12",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5039",
    "total": "5039"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5039",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "605092"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "5"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3M2E4ZTM3ZC1kYmZjLTU2YWQtODQ3OC05MWMxZTJhYWM5YjkifQ==",
    "nonce": 1243,
    "balances": {
      "current": "10000001478548975",
      "previous": "10000001478554019"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xaf11af61bd1e605ed31fa5cb91799b092a9a58e5",
    "nonce": 20,
    "balances": {
      "current": "5039",
      "previous": "0"
    }
  },
  "blockNumber": "10114522",
  "created": "2020-05-22T08:07:51.406Z",
  "updated": "2020-05-22T08:07:51.473Z",
  "id": "5ec78857005df800101bc3c2"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000000000000000013af0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5039`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``