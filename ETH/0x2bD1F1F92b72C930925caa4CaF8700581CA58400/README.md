# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2bD1F1F92b72C930925caa4CaF8700581CA58400`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000002af10000000000000000000000000000000000000000000000000000000000002af100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000002af10000000000000000000000000000000000000000000000000000000000002af1696a976336aa35b2ffdf28f328f1862938f85cf6ef693ca5ba57a9187e0f8ebdef9964bb40f3a21fa8dedaf0c6817982773300e2106fa1097e8b882f9e2cf8192e0acd19471ed18bfb38021b6b8b4604117d9a460bddb074405a49ab357db4be000000000000000000000000000000000000000000000000000000000000001c38a069d0f42a3dd340c5d775bfc0dec936ef346ab70aad2e53d9d6cbeebe609306b4165108a237a19afc2a8e5ecea6ed5a13b6c896bdf6c3dc2b910e5717d1ba28d3b32a9277c41844f7cc321606e91a739551f230bfd08a5d0d64cbaf8c851e000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ef000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007d700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3b42ee7000000000000000000000000000000000000000000000000002386f2c3b459e200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a4c2f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d6a59784f445179595330304e7a5a684c54566c596a67744f5749354d5330324f4746685a5463324e6a67774e7a4d6966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000002bd1f1f92b72c930925caa4caf8700581ca584000000000000000000000000000000000000000000000000000000000000002af1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x696a976336aa35b2ffdf28f328f1862938f85cf6ef693ca5ba57a9187e0f8ebd",
      "signature": {
        "s": "0x2e0acd19471ed18bfb38021b6b8b4604117d9a460bddb074405a49ab357db4be",
        "r": "0xef9964bb40f3a21fa8dedaf0c6817982773300e2106fa1097e8b882f9e2cf819",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x38a069d0f42a3dd340c5d775bfc0dec936ef346ab70aad2e53d9d6cbeebe6093",
      "signature": {
        "s": "0x28d3b32a9277c41844f7cc321606e91a739551f230bfd08a5d0d64cbaf8c851e",
        "r": "0x06b4165108a237a19afc2a8e5ecea6ed5a13b6c896bdf6c3dc2b910e5717d1ba",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "10993",
    "total": "10993"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10993",
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
            "amount": "674863"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "10"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5MjYxODQyYS00NzZhLTVlYjgtOWI5MS02OGFhZTc2NjgwNzMifQ==",
    "nonce": 2007,
    "balances": {
      "current": "10000001408446183",
      "previous": "10000001408457186"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2bd1f1f92b72c930925caa4caf8700581ca58400",
    "nonce": 20,
    "balances": {
      "current": "10993",
      "previous": "0"
    }
  },
  "blockNumber": "10114543",
  "created": "2020-05-22T08:13:41.441Z",
  "updated": "2020-05-22T08:13:41.514Z",
  "id": "5ec789b5e5756b00111b81f9"
}
```
* *stageAmount*: `10993`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000002af100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000002af10000000000000000000000000000000000000000000000000000000000002af1696a976336aa35b2ffdf28f328f1862938f85cf6ef693ca5ba57a9187e0f8ebdef9964bb40f3a21fa8dedaf0c6817982773300e2106fa1097e8b882f9e2cf8192e0acd19471ed18bfb38021b6b8b4604117d9a460bddb074405a49ab357db4be000000000000000000000000000000000000000000000000000000000000001c38a069d0f42a3dd340c5d775bfc0dec936ef346ab70aad2e53d9d6cbeebe609306b4165108a237a19afc2a8e5ecea6ed5a13b6c896bdf6c3dc2b910e5717d1ba28d3b32a9277c41844f7cc321606e91a739551f230bfd08a5d0d64cbaf8c851e000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ef000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007d700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3b42ee7000000000000000000000000000000000000000000000000002386f2c3b459e200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a4c2f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d6a59784f445179595330304e7a5a684c54566c596a67744f5749354d5330324f4746685a5463324e6a67774e7a4d6966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000002bd1f1f92b72c930925caa4caf8700581ca584000000000000000000000000000000000000000000000000000000000000002af1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x696a976336aa35b2ffdf28f328f1862938f85cf6ef693ca5ba57a9187e0f8ebd",
      "signature": {
        "s": "0x2e0acd19471ed18bfb38021b6b8b4604117d9a460bddb074405a49ab357db4be",
        "r": "0xef9964bb40f3a21fa8dedaf0c6817982773300e2106fa1097e8b882f9e2cf819",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x38a069d0f42a3dd340c5d775bfc0dec936ef346ab70aad2e53d9d6cbeebe6093",
      "signature": {
        "s": "0x28d3b32a9277c41844f7cc321606e91a739551f230bfd08a5d0d64cbaf8c851e",
        "r": "0x06b4165108a237a19afc2a8e5ecea6ed5a13b6c896bdf6c3dc2b910e5717d1ba",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "10993",
    "total": "10993"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10993",
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
            "amount": "674863"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "10"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5MjYxODQyYS00NzZhLTVlYjgtOWI5MS02OGFhZTc2NjgwNzMifQ==",
    "nonce": 2007,
    "balances": {
      "current": "10000001408446183",
      "previous": "10000001408457186"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2bd1f1f92b72c930925caa4caf8700581ca58400",
    "nonce": 20,
    "balances": {
      "current": "10993",
      "previous": "0"
    }
  },
  "blockNumber": "10114543",
  "created": "2020-05-22T08:13:41.441Z",
  "updated": "2020-05-22T08:13:41.514Z",
  "id": "5ec789b5e5756b00111b81f9"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000002af10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `10993`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``