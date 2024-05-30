# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x93a367C90062b0cA5447c4bFe9b8E82677b264af`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000047930000000000000000000000000000000000000000000000000000000000004793000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000047930000000000000000000000000000000000000000000000000000000000004793e159a49e7b3f3c7f154cf0df247afbfa01f69d8b9f1314d3e4dadb293dba1123bf69f44c7a28bfc89ce45dd8dd9e353d3e9b69ffcb21635d137f24521a1ee304402f10ba5300cb43299249bd16206cafdb037e204882e47e33634ee59b71f257000000000000000000000000000000000000000000000000000000000000001b2467b498bd66ede46b863cce4e5196a5911469c71eff937d06c477aa9026e87a86a485c7a0dc4007693bcc054df382b0c24d713f1bc1eb5e9ab4b479df4693cc63532c62955003f66996b6ac516edbde152929193345aca443648ee9facee034000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000054d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c74a5757000000000000000000000000000000000000000000000000002386f2c74a9efc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009623b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4f5463334f44426c5a5330794e7a6b314c54557a4d7a63744f5455354d6930304e5745784f4755344d54453459574d6966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000093a367c90062b0ca5447c4bfe9b8e82677b264af0000000000000000000000000000000000000000000000000000000000004793000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe159a49e7b3f3c7f154cf0df247afbfa01f69d8b9f1314d3e4dadb293dba1123",
      "signature": {
        "s": "0x402f10ba5300cb43299249bd16206cafdb037e204882e47e33634ee59b71f257",
        "r": "0xbf69f44c7a28bfc89ce45dd8dd9e353d3e9b69ffcb21635d137f24521a1ee304",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2467b498bd66ede46b863cce4e5196a5911469c71eff937d06c477aa9026e87a",
      "signature": {
        "s": "0x63532c62955003f66996b6ac516edbde152929193345aca443648ee9facee034",
        "r": "0x86a485c7a0dc4007693bcc054df382b0c24d713f1bc1eb5e9ab4b479df4693cc",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18323",
    "total": "18323"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18323",
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
            "amount": "614971"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzOTc3ODBlZS0yNzk1LTUzMzctOTU5Mi00NWExOGU4MTE4YWMifQ==",
    "nonce": 1357,
    "balances": {
      "current": "10000001468618583",
      "previous": "10000001468636924"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x93a367c90062b0ca5447c4bfe9b8e82677b264af",
    "nonce": 20,
    "balances": {
      "current": "18323",
      "previous": "0"
    }
  },
  "blockNumber": "10114525",
  "created": "2020-05-22T08:08:45.455Z",
  "updated": "2020-05-22T08:08:45.519Z",
  "id": "5ec7888d005df800101bc3ed"
}
```
* *stageAmount*: `18323`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000004793000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000047930000000000000000000000000000000000000000000000000000000000004793e159a49e7b3f3c7f154cf0df247afbfa01f69d8b9f1314d3e4dadb293dba1123bf69f44c7a28bfc89ce45dd8dd9e353d3e9b69ffcb21635d137f24521a1ee304402f10ba5300cb43299249bd16206cafdb037e204882e47e33634ee59b71f257000000000000000000000000000000000000000000000000000000000000001b2467b498bd66ede46b863cce4e5196a5911469c71eff937d06c477aa9026e87a86a485c7a0dc4007693bcc054df382b0c24d713f1bc1eb5e9ab4b479df4693cc63532c62955003f66996b6ac516edbde152929193345aca443648ee9facee034000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000054d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c74a5757000000000000000000000000000000000000000000000000002386f2c74a9efc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009623b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4f5463334f44426c5a5330794e7a6b314c54557a4d7a63744f5455354d6930304e5745784f4755344d54453459574d6966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000093a367c90062b0ca5447c4bfe9b8e82677b264af0000000000000000000000000000000000000000000000000000000000004793000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe159a49e7b3f3c7f154cf0df247afbfa01f69d8b9f1314d3e4dadb293dba1123",
      "signature": {
        "s": "0x402f10ba5300cb43299249bd16206cafdb037e204882e47e33634ee59b71f257",
        "r": "0xbf69f44c7a28bfc89ce45dd8dd9e353d3e9b69ffcb21635d137f24521a1ee304",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2467b498bd66ede46b863cce4e5196a5911469c71eff937d06c477aa9026e87a",
      "signature": {
        "s": "0x63532c62955003f66996b6ac516edbde152929193345aca443648ee9facee034",
        "r": "0x86a485c7a0dc4007693bcc054df382b0c24d713f1bc1eb5e9ab4b479df4693cc",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18323",
    "total": "18323"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18323",
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
            "amount": "614971"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzOTc3ODBlZS0yNzk1LTUzMzctOTU5Mi00NWExOGU4MTE4YWMifQ==",
    "nonce": 1357,
    "balances": {
      "current": "10000001468618583",
      "previous": "10000001468636924"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x93a367c90062b0ca5447c4bfe9b8e82677b264af",
    "nonce": 20,
    "balances": {
      "current": "18323",
      "previous": "0"
    }
  },
  "blockNumber": "10114525",
  "created": "2020-05-22T08:08:45.455Z",
  "updated": "2020-05-22T08:08:45.519Z",
  "id": "5ec7888d005df800101bc3ed"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000047930000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18323`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``