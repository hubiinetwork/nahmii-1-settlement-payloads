# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x73549461C538A43F008bb49cB89d6b3FFA14dbb9`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000006ca60000000000000000000000000000000000000000000000000000000000006ca600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000006ca60000000000000000000000000000000000000000000000000000000000006ca6ad3e2b8cc7db4a7f43a0a9822e0d8815011d2acbb57234b667125f32f631287b7e512dbc5746e5d38da712d10b7b297a5787d4b45a7e4b64c75358e25594842770899abe34916e2e50da473db1e8b7d8eb606eb9ee9830c06e1a485e875573a7000000000000000000000000000000000000000000000000000000000000001cb544470ad4d155213d66f6c838c1c64247a8671e8236fe0b61c851a6b7106e003f5514468c5c7807dacd9c42ea920d60dd54631b013baff6221d1c685503f4a812d67534a554ceaeea38735974537dec5083cbe745e7c43b8b97896d8989784a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000046200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c838e35c000000000000000000000000000000000000000000000000002386f2c839501d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009258300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d546b784d544d794f43316c4d6a466b4c54566d5a545974595449334e693168597a646c4d5441314e7a6b784f54416966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000073549461c538a43f008bb49cb89d6b3ffa14dbb90000000000000000000000000000000000000000000000000000000000006ca6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xad3e2b8cc7db4a7f43a0a9822e0d8815011d2acbb57234b667125f32f631287b",
      "signature": {
        "s": "0x70899abe34916e2e50da473db1e8b7d8eb606eb9ee9830c06e1a485e875573a7",
        "r": "0x7e512dbc5746e5d38da712d10b7b297a5787d4b45a7e4b64c75358e255948427",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb544470ad4d155213d66f6c838c1c64247a8671e8236fe0b61c851a6b7106e00",
      "signature": {
        "s": "0x12d67534a554ceaeea38735974537dec5083cbe745e7c43b8b97896d8989784a",
        "r": "0x3f5514468c5c7807dacd9c42ea920d60dd54631b013baff6221d1c685503f4a8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "27814",
    "total": "27814"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "27814",
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
            "amount": "599427"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "27"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMTkxMTMyOC1lMjFkLTVmZTYtYTI3Ni1hYzdlMTA1NzkxOTAifQ==",
    "nonce": 1122,
    "balances": {
      "current": "10000001484251996",
      "previous": "10000001484279837"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x73549461c538a43f008bb49cb89d6b3ffa14dbb9",
    "nonce": 20,
    "balances": {
      "current": "27814",
      "previous": "0"
    }
  },
  "blockNumber": "10114519",
  "created": "2020-05-22T08:06:57.734Z",
  "updated": "2020-05-22T08:06:57.811Z",
  "id": "5ec78821e5756b00111b80de"
}
```
* *stageAmount*: `27814`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000006ca600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000006ca60000000000000000000000000000000000000000000000000000000000006ca6ad3e2b8cc7db4a7f43a0a9822e0d8815011d2acbb57234b667125f32f631287b7e512dbc5746e5d38da712d10b7b297a5787d4b45a7e4b64c75358e25594842770899abe34916e2e50da473db1e8b7d8eb606eb9ee9830c06e1a485e875573a7000000000000000000000000000000000000000000000000000000000000001cb544470ad4d155213d66f6c838c1c64247a8671e8236fe0b61c851a6b7106e003f5514468c5c7807dacd9c42ea920d60dd54631b013baff6221d1c685503f4a812d67534a554ceaeea38735974537dec5083cbe745e7c43b8b97896d8989784a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000046200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c838e35c000000000000000000000000000000000000000000000000002386f2c839501d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009258300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d546b784d544d794f43316c4d6a466b4c54566d5a545974595449334e693168597a646c4d5441314e7a6b784f54416966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000073549461c538a43f008bb49cb89d6b3ffa14dbb90000000000000000000000000000000000000000000000000000000000006ca6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xad3e2b8cc7db4a7f43a0a9822e0d8815011d2acbb57234b667125f32f631287b",
      "signature": {
        "s": "0x70899abe34916e2e50da473db1e8b7d8eb606eb9ee9830c06e1a485e875573a7",
        "r": "0x7e512dbc5746e5d38da712d10b7b297a5787d4b45a7e4b64c75358e255948427",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb544470ad4d155213d66f6c838c1c64247a8671e8236fe0b61c851a6b7106e00",
      "signature": {
        "s": "0x12d67534a554ceaeea38735974537dec5083cbe745e7c43b8b97896d8989784a",
        "r": "0x3f5514468c5c7807dacd9c42ea920d60dd54631b013baff6221d1c685503f4a8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "27814",
    "total": "27814"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "27814",
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
            "amount": "599427"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "27"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMTkxMTMyOC1lMjFkLTVmZTYtYTI3Ni1hYzdlMTA1NzkxOTAifQ==",
    "nonce": 1122,
    "balances": {
      "current": "10000001484251996",
      "previous": "10000001484279837"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x73549461c538a43f008bb49cb89d6b3ffa14dbb9",
    "nonce": 20,
    "balances": {
      "current": "27814",
      "previous": "0"
    }
  },
  "blockNumber": "10114519",
  "created": "2020-05-22T08:06:57.734Z",
  "updated": "2020-05-22T08:06:57.811Z",
  "id": "5ec78821e5756b00111b80de"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000006ca60000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `27814`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``