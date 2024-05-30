# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xca83b1d8E0E344083b7ddaC86B69178F28FEAcE3`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000001a680000000000000000000000000000000000000000000000000000000000001a6800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001a680000000000000000000000000000000000000000000000000000000000001a68cab97053ad73203ebaa6de202b578173b4e346ca58bee386a1eba62504baf4a9f7f4c6ac208d9d09843abfc6fb682d86fddeb878c5b10de7df0d6e72dc289bec3bb2f4bfc22665b4d72927a1bcf550b553ef80ca40fa24687eea321d6463f146000000000000000000000000000000000000000000000000000000000000001cd689d66c0e21d4253a4d81fc890bdbcc4d92b45c408912ed49f0ad9f13fc1f18e3b383b135d90783f83457d92348d4753eb16fa30184ed7e6dcd07340d28a55b67251730a535665c5588c5fb818cbdedaca8ebe699899fafd865705b2cc26e7a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000034300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cae11fb6000000000000000000000000000000000000000000000000002386f2cae13a2400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000877c300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d595463314e6a41344e793035596a49344c5456694d544974596a45324e69316c4f544d344e444e69597a6b794e6a636966513d3d0000000000000000000000000000000000000000000000000000000000000017000000000000000000000000ca83b1d8e0e344083b7ddac86b69178f28feace30000000000000000000000000000000000000000000000000000000000001a68000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcab97053ad73203ebaa6de202b578173b4e346ca58bee386a1eba62504baf4a9",
      "signature": {
        "s": "0x3bb2f4bfc22665b4d72927a1bcf550b553ef80ca40fa24687eea321d6463f146",
        "r": "0xf7f4c6ac208d9d09843abfc6fb682d86fddeb878c5b10de7df0d6e72dc289bec",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd689d66c0e21d4253a4d81fc890bdbcc4d92b45c408912ed49f0ad9f13fc1f18",
      "signature": {
        "s": "0x67251730a535665c5588c5fb818cbdedaca8ebe699899fafd865705b2cc26e7a",
        "r": "0xe3b383b135d90783f83457d92348d4753eb16fa30184ed7e6dcd07340d28a55b",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6760",
    "total": "6760"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6760",
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
            "amount": "554947"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "6"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmYTc1NjA4Ny05YjI4LTViMTItYjE2Ni1lOTM4NDNiYzkyNjcifQ==",
    "nonce": 835,
    "balances": {
      "current": "10000001528831926",
      "previous": "10000001528838692"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xca83b1d8e0e344083b7ddac86b69178f28feace3",
    "nonce": 23,
    "balances": {
      "current": "6760",
      "previous": "0"
    }
  },
  "blockNumber": "10114513",
  "created": "2020-05-22T08:04:57.550Z",
  "updated": "2020-05-22T08:04:57.617Z",
  "id": "5ec787a9e5756b00111b8082"
}
```
* *stageAmount*: `6760`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000001a6800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001a680000000000000000000000000000000000000000000000000000000000001a68cab97053ad73203ebaa6de202b578173b4e346ca58bee386a1eba62504baf4a9f7f4c6ac208d9d09843abfc6fb682d86fddeb878c5b10de7df0d6e72dc289bec3bb2f4bfc22665b4d72927a1bcf550b553ef80ca40fa24687eea321d6463f146000000000000000000000000000000000000000000000000000000000000001cd689d66c0e21d4253a4d81fc890bdbcc4d92b45c408912ed49f0ad9f13fc1f18e3b383b135d90783f83457d92348d4753eb16fa30184ed7e6dcd07340d28a55b67251730a535665c5588c5fb818cbdedaca8ebe699899fafd865705b2cc26e7a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000034300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cae11fb6000000000000000000000000000000000000000000000000002386f2cae13a2400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000877c300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d595463314e6a41344e793035596a49344c5456694d544974596a45324e69316c4f544d344e444e69597a6b794e6a636966513d3d0000000000000000000000000000000000000000000000000000000000000017000000000000000000000000ca83b1d8e0e344083b7ddac86b69178f28feace30000000000000000000000000000000000000000000000000000000000001a68000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcab97053ad73203ebaa6de202b578173b4e346ca58bee386a1eba62504baf4a9",
      "signature": {
        "s": "0x3bb2f4bfc22665b4d72927a1bcf550b553ef80ca40fa24687eea321d6463f146",
        "r": "0xf7f4c6ac208d9d09843abfc6fb682d86fddeb878c5b10de7df0d6e72dc289bec",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd689d66c0e21d4253a4d81fc890bdbcc4d92b45c408912ed49f0ad9f13fc1f18",
      "signature": {
        "s": "0x67251730a535665c5588c5fb818cbdedaca8ebe699899fafd865705b2cc26e7a",
        "r": "0xe3b383b135d90783f83457d92348d4753eb16fa30184ed7e6dcd07340d28a55b",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6760",
    "total": "6760"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6760",
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
            "amount": "554947"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "6"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmYTc1NjA4Ny05YjI4LTViMTItYjE2Ni1lOTM4NDNiYzkyNjcifQ==",
    "nonce": 835,
    "balances": {
      "current": "10000001528831926",
      "previous": "10000001528838692"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xca83b1d8e0e344083b7ddac86b69178f28feace3",
    "nonce": 23,
    "balances": {
      "current": "6760",
      "previous": "0"
    }
  },
  "blockNumber": "10114513",
  "created": "2020-05-22T08:04:57.550Z",
  "updated": "2020-05-22T08:04:57.617Z",
  "id": "5ec787a9e5756b00111b8082"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000001a680000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6760`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``