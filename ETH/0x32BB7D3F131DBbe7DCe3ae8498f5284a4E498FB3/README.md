# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x32BB7D3F131DBbe7DCe3ae8498f5284a4E498FB3`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000a4a0000000000000000000000000000000000000000000000000000000000000a4a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000a4a0000000000000000000000000000000000000000000000000000000000000a4a5c4764874f3d51a6ba04082717cc8a229419a532272a3b5cc92183700e501c9ae630593d6c3f66514d896bba23bee0da709b3f58bc03a4e88e8a0584daf1e5d95b6ff65b4d2414d9f23d8f7ea8f9e31da198bdb2d7ad9a123babaa11263cc074000000000000000000000000000000000000000000000000000000000000001c5731a5f3cdada5399f69f54863eecf34ba1e378b3699ba03beb284d4ce9426f10482dd5f6e35ff6ef322ad98aa88b1964c5a08d5e8bb567940ef4a0e1dadc0525f8ecafd8e4870a9ede9f3c25f5e6345f18f30392ae5646bb806267f32fe8d20000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f8000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008f700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc56e736000000000000000000000000000000000000000000000000002386f2bc56f18200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2e0c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e7a4933597a5a6d5953307a4f4451774c54566a4e4449744f574533597930354e6a51314e44557a59546c6c4f54636966513d3d000000000000000000000000000000000000000000000000000000000000000300000000000000000000000032bb7d3f131dbbe7dce3ae8498f5284a4e498fb30000000000000000000000000000000000000000000000000000000000000a4a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5c4764874f3d51a6ba04082717cc8a229419a532272a3b5cc92183700e501c9a",
      "signature": {
        "s": "0x5b6ff65b4d2414d9f23d8f7ea8f9e31da198bdb2d7ad9a123babaa11263cc074",
        "r": "0xe630593d6c3f66514d896bba23bee0da709b3f58bc03a4e88e8a0584daf1e5d9",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5731a5f3cdada5399f69f54863eecf34ba1e378b3699ba03beb284d4ce9426f1",
      "signature": {
        "s": "0x5f8ecafd8e4870a9ede9f3c25f5e6345f18f30392ae5646bb806267f32fe8d20",
        "r": "0x0482dd5f6e35ff6ef322ad98aa88b1964c5a08d5e8bb567940ef4a0e1dadc052",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2634",
    "total": "2634"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2634",
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
            "amount": "798220"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4NzI3YzZmYS0zODQwLTVjNDItOWE3Yy05NjQ1NDUzYTllOTcifQ==",
    "nonce": 2295,
    "balances": {
      "current": "10000001284892470",
      "previous": "10000001284895106"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x32bb7d3f131dbbe7dce3ae8498f5284a4e498fb3",
    "nonce": 3,
    "balances": {
      "current": "2634",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:35.637Z",
  "updated": "2020-05-22T08:15:35.702Z",
  "id": "5ec78a27005df800101bc523"
}
```
* *stageAmount*: `2634`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000a4a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000a4a0000000000000000000000000000000000000000000000000000000000000a4a5c4764874f3d51a6ba04082717cc8a229419a532272a3b5cc92183700e501c9ae630593d6c3f66514d896bba23bee0da709b3f58bc03a4e88e8a0584daf1e5d95b6ff65b4d2414d9f23d8f7ea8f9e31da198bdb2d7ad9a123babaa11263cc074000000000000000000000000000000000000000000000000000000000000001c5731a5f3cdada5399f69f54863eecf34ba1e378b3699ba03beb284d4ce9426f10482dd5f6e35ff6ef322ad98aa88b1964c5a08d5e8bb567940ef4a0e1dadc0525f8ecafd8e4870a9ede9f3c25f5e6345f18f30392ae5646bb806267f32fe8d20000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f8000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008f700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc56e736000000000000000000000000000000000000000000000000002386f2bc56f18200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2e0c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e7a4933597a5a6d5953307a4f4451774c54566a4e4449744f574533597930354e6a51314e44557a59546c6c4f54636966513d3d000000000000000000000000000000000000000000000000000000000000000300000000000000000000000032bb7d3f131dbbe7dce3ae8498f5284a4e498fb30000000000000000000000000000000000000000000000000000000000000a4a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5c4764874f3d51a6ba04082717cc8a229419a532272a3b5cc92183700e501c9a",
      "signature": {
        "s": "0x5b6ff65b4d2414d9f23d8f7ea8f9e31da198bdb2d7ad9a123babaa11263cc074",
        "r": "0xe630593d6c3f66514d896bba23bee0da709b3f58bc03a4e88e8a0584daf1e5d9",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5731a5f3cdada5399f69f54863eecf34ba1e378b3699ba03beb284d4ce9426f1",
      "signature": {
        "s": "0x5f8ecafd8e4870a9ede9f3c25f5e6345f18f30392ae5646bb806267f32fe8d20",
        "r": "0x0482dd5f6e35ff6ef322ad98aa88b1964c5a08d5e8bb567940ef4a0e1dadc052",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2634",
    "total": "2634"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2634",
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
            "amount": "798220"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4NzI3YzZmYS0zODQwLTVjNDItOWE3Yy05NjQ1NDUzYTllOTcifQ==",
    "nonce": 2295,
    "balances": {
      "current": "10000001284892470",
      "previous": "10000001284895106"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x32bb7d3f131dbbe7dce3ae8498f5284a4e498fb3",
    "nonce": 3,
    "balances": {
      "current": "2634",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:35.637Z",
  "updated": "2020-05-22T08:15:35.702Z",
  "id": "5ec78a27005df800101bc523"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000a4a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2634`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``