# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x098C621ab7523603023A88FfF134ae07050dBDe1`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000008f260000000000000000000000000000000000000000000000000000000000008f2600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000008f260000000000000000000000000000000000000000000000000000000000008f26762008d603eb7cf33f8a3b771706d4ae314b40db33436b5153956243c2038880d5c80fca57b99c042553d9e745b1444e811388881daf1843494cfa71e6fa6fd06fcc1565b8e7a320e0f260ebe0250acaa8e1a1c76c49ea5b7f77885321973b17000000000000000000000000000000000000000000000000000000000000001c5086bc7b393f2776d12974fca4c5c9d3c8fd0aa108af1d24ec83603947694b0d1dabb7a8721d2744d019ec4654e89c5cf665fedd56ec6ecb3e8fffc6733544d077880e9560ffc36a12c15b6d95761ed408a39b4a4bd1362dd78d2569c555f90d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ea000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000006e200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c5229374000000000000000000000000000000000000000000000000002386f2c52322be00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000002400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009eee000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a597a51354d57526c4e43307a4e7a49784c54557a4e6d55744f5455784f4330774f54566b4f5441344f474933596d516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000098c621ab7523603023a88fff134ae07050dbde10000000000000000000000000000000000000000000000000000000000008f26000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x762008d603eb7cf33f8a3b771706d4ae314b40db33436b5153956243c2038880",
      "signature": {
        "s": "0x6fcc1565b8e7a320e0f260ebe0250acaa8e1a1c76c49ea5b7f77885321973b17",
        "r": "0xd5c80fca57b99c042553d9e745b1444e811388881daf1843494cfa71e6fa6fd0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5086bc7b393f2776d12974fca4c5c9d3c8fd0aa108af1d24ec83603947694b0d",
      "signature": {
        "s": "0x77880e9560ffc36a12c15b6d95761ed408a39b4a4bd1362dd78d2569c555f90d",
        "r": "0x1dabb7a8721d2744d019ec4654e89c5cf665fedd56ec6ecb3e8fffc6733544d0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "36646",
    "total": "36646"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "36646",
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
            "amount": "650976"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "36"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjYzQ5MWRlNC0zNzIxLTUzNmUtOTUxOC0wOTVkOTA4OGI3YmQifQ==",
    "nonce": 1762,
    "balances": {
      "current": "10000001432458100",
      "previous": "10000001432494782"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x098c621ab7523603023a88fff134ae07050dbde1",
    "nonce": 20,
    "balances": {
      "current": "36646",
      "previous": "0"
    }
  },
  "blockNumber": "10114538",
  "created": "2020-05-22T08:11:51.370Z",
  "updated": "2020-05-22T08:11:51.434Z",
  "id": "5ec78947005df800101bc470"
}
```
* *stageAmount*: `36646`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000008f2600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000008f260000000000000000000000000000000000000000000000000000000000008f26762008d603eb7cf33f8a3b771706d4ae314b40db33436b5153956243c2038880d5c80fca57b99c042553d9e745b1444e811388881daf1843494cfa71e6fa6fd06fcc1565b8e7a320e0f260ebe0250acaa8e1a1c76c49ea5b7f77885321973b17000000000000000000000000000000000000000000000000000000000000001c5086bc7b393f2776d12974fca4c5c9d3c8fd0aa108af1d24ec83603947694b0d1dabb7a8721d2744d019ec4654e89c5cf665fedd56ec6ecb3e8fffc6733544d077880e9560ffc36a12c15b6d95761ed408a39b4a4bd1362dd78d2569c555f90d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ea000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000006e200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c5229374000000000000000000000000000000000000000000000000002386f2c52322be00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000002400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009eee000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a597a51354d57526c4e43307a4e7a49784c54557a4e6d55744f5455784f4330774f54566b4f5441344f474933596d516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000098c621ab7523603023a88fff134ae07050dbde10000000000000000000000000000000000000000000000000000000000008f26000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x762008d603eb7cf33f8a3b771706d4ae314b40db33436b5153956243c2038880",
      "signature": {
        "s": "0x6fcc1565b8e7a320e0f260ebe0250acaa8e1a1c76c49ea5b7f77885321973b17",
        "r": "0xd5c80fca57b99c042553d9e745b1444e811388881daf1843494cfa71e6fa6fd0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5086bc7b393f2776d12974fca4c5c9d3c8fd0aa108af1d24ec83603947694b0d",
      "signature": {
        "s": "0x77880e9560ffc36a12c15b6d95761ed408a39b4a4bd1362dd78d2569c555f90d",
        "r": "0x1dabb7a8721d2744d019ec4654e89c5cf665fedd56ec6ecb3e8fffc6733544d0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "36646",
    "total": "36646"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "36646",
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
            "amount": "650976"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "36"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjYzQ5MWRlNC0zNzIxLTUzNmUtOTUxOC0wOTVkOTA4OGI3YmQifQ==",
    "nonce": 1762,
    "balances": {
      "current": "10000001432458100",
      "previous": "10000001432494782"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x098c621ab7523603023a88fff134ae07050dbde1",
    "nonce": 20,
    "balances": {
      "current": "36646",
      "previous": "0"
    }
  },
  "blockNumber": "10114538",
  "created": "2020-05-22T08:11:51.370Z",
  "updated": "2020-05-22T08:11:51.434Z",
  "id": "5ec78947005df800101bc470"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000008f260000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `36646`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``