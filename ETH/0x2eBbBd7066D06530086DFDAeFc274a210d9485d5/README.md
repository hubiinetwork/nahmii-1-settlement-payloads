# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2eBbBd7066D06530086DFDAeFc274a210d9485d5`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000011e400000000000000000000000000000000000000000000000000000000000011e4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000011e400000000000000000000000000000000000000000000000000000000000011e4dcdc083af55e0bce4eedfcb1a0b2c7a93c27255d747c913fcc6d93954513fc99055b7afd1ac533038785e9b3edf22f7afe8b9ce7a04cb136ed3a04e523225a971cd2a7a76c3be8d9dccbda5dd5de5c38f9d232a43d1050102fffdbfe8b7b455d000000000000000000000000000000000000000000000000000000000000001b2f082f26c89f6d6eee15a7fe83a63d9d387a4a1d5fd5fb2fffcf95fca4ff91b5fc1e712feb6ec12a3e066e747054ff0cc2bfbba9689b3ffcecda63df0af540003a5a5746daf0624c47918622f80a0cde2951c07e6d4d7dcbc2bd1f68b36ff74a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000072100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c42f1831000000000000000000000000000000000000000000000000002386f2c42f2a1900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a2d0700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344f475a6b59325930596930774d4456684c5456694e4759744f5755355a4330304e6a646d4e7a6c684f4455354d44676966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000002ebbbd7066d06530086dfdaefc274a210d9485d500000000000000000000000000000000000000000000000000000000000011e4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdcdc083af55e0bce4eedfcb1a0b2c7a93c27255d747c913fcc6d93954513fc99",
      "signature": {
        "s": "0x1cd2a7a76c3be8d9dccbda5dd5de5c38f9d232a43d1050102fffdbfe8b7b455d",
        "r": "0x055b7afd1ac533038785e9b3edf22f7afe8b9ce7a04cb136ed3a04e523225a97",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2f082f26c89f6d6eee15a7fe83a63d9d387a4a1d5fd5fb2fffcf95fca4ff91b5",
      "signature": {
        "s": "0x3a5a5746daf0624c47918622f80a0cde2951c07e6d4d7dcbc2bd1f68b36ff74a",
        "r": "0xfc1e712feb6ec12a3e066e747054ff0cc2bfbba9689b3ffcecda63df0af54000",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4580",
    "total": "4580"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4580",
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
            "amount": "666887"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "4"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4OGZkY2Y0Yi0wMDVhLTViNGYtOWU5ZC00NjdmNzlhODU5MDgifQ==",
    "nonce": 1825,
    "balances": {
      "current": "10000001416501297",
      "previous": "10000001416505881"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2ebbbd7066d06530086dfdaefc274a210d9485d5",
    "nonce": 20,
    "balances": {
      "current": "4580",
      "previous": "0"
    }
  },
  "blockNumber": "10114541",
  "created": "2020-05-22T08:12:22.589Z",
  "updated": "2020-05-22T08:12:22.658Z",
  "id": "5ec78966005df800101bc487"
}
```
* *stageAmount*: `4580`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000011e4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000011e400000000000000000000000000000000000000000000000000000000000011e4dcdc083af55e0bce4eedfcb1a0b2c7a93c27255d747c913fcc6d93954513fc99055b7afd1ac533038785e9b3edf22f7afe8b9ce7a04cb136ed3a04e523225a971cd2a7a76c3be8d9dccbda5dd5de5c38f9d232a43d1050102fffdbfe8b7b455d000000000000000000000000000000000000000000000000000000000000001b2f082f26c89f6d6eee15a7fe83a63d9d387a4a1d5fd5fb2fffcf95fca4ff91b5fc1e712feb6ec12a3e066e747054ff0cc2bfbba9689b3ffcecda63df0af540003a5a5746daf0624c47918622f80a0cde2951c07e6d4d7dcbc2bd1f68b36ff74a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000072100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c42f1831000000000000000000000000000000000000000000000000002386f2c42f2a1900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a2d0700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344f475a6b59325930596930774d4456684c5456694e4759744f5755355a4330304e6a646d4e7a6c684f4455354d44676966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000002ebbbd7066d06530086dfdaefc274a210d9485d500000000000000000000000000000000000000000000000000000000000011e4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdcdc083af55e0bce4eedfcb1a0b2c7a93c27255d747c913fcc6d93954513fc99",
      "signature": {
        "s": "0x1cd2a7a76c3be8d9dccbda5dd5de5c38f9d232a43d1050102fffdbfe8b7b455d",
        "r": "0x055b7afd1ac533038785e9b3edf22f7afe8b9ce7a04cb136ed3a04e523225a97",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2f082f26c89f6d6eee15a7fe83a63d9d387a4a1d5fd5fb2fffcf95fca4ff91b5",
      "signature": {
        "s": "0x3a5a5746daf0624c47918622f80a0cde2951c07e6d4d7dcbc2bd1f68b36ff74a",
        "r": "0xfc1e712feb6ec12a3e066e747054ff0cc2bfbba9689b3ffcecda63df0af54000",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4580",
    "total": "4580"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4580",
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
            "amount": "666887"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "4"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4OGZkY2Y0Yi0wMDVhLTViNGYtOWU5ZC00NjdmNzlhODU5MDgifQ==",
    "nonce": 1825,
    "balances": {
      "current": "10000001416501297",
      "previous": "10000001416505881"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2ebbbd7066d06530086dfdaefc274a210d9485d5",
    "nonce": 20,
    "balances": {
      "current": "4580",
      "previous": "0"
    }
  },
  "blockNumber": "10114541",
  "created": "2020-05-22T08:12:22.589Z",
  "updated": "2020-05-22T08:12:22.658Z",
  "id": "5ec78966005df800101bc487"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000011e40000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4580`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``