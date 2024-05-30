# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8496Dc3f4DC5A3C58CB02A9d79C2f2f3e339457A`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000152100000000000000000000000000000000000000000000000000000000000015210000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000152100000000000000000000000000000000000000000000000000000000000015214deed63b69fdbb8b6b06522656833753587fb79601558e5c897f1a95ecf2acd4a853b0c5641a337bb60b051192514a9ee219cf003777eda9768c1219f5744e32121e2ba79bc138aad3e7f6ba954c1d9979ffe4259a13a0db527fdc3217d832b5000000000000000000000000000000000000000000000000000000000000001ba5d8979f8fc74b8f5bc758cd784de63850394cb804613b1c750643198f7f44871d46d81db2fc5b9e80d0f45eba230039dfecadf0f76f8edbfc6cd309598e3846001d88a9c8558d2060e995480b412e4c4ac7f9486b037c2c3db438450b1c3d7a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d9000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004af00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7fc1d54000000000000000000000000000000000000000000000000002386f2c7fc327a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000050000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000934f800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d575a694e7a6b784e7931694f545a6a4c5455304f44497459574d35595330324d325933595442684e7a6b344d44496966513d3d00000000000000000000000000000000000000000000000000000000000000080000000000000000000000008496dc3f4dc5a3c58cb02a9d79c2f2f3e339457a0000000000000000000000000000000000000000000000000000000000001521000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4deed63b69fdbb8b6b06522656833753587fb79601558e5c897f1a95ecf2acd4",
      "signature": {
        "s": "0x121e2ba79bc138aad3e7f6ba954c1d9979ffe4259a13a0db527fdc3217d832b5",
        "r": "0xa853b0c5641a337bb60b051192514a9ee219cf003777eda9768c1219f5744e32",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa5d8979f8fc74b8f5bc758cd784de63850394cb804613b1c750643198f7f4487",
      "signature": {
        "s": "0x001d88a9c8558d2060e995480b412e4c4ac7f9486b037c2c3db438450b1c3d7a",
        "r": "0x1d46d81db2fc5b9e80d0f45eba230039dfecadf0f76f8edbfc6cd309598e3846",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5409",
    "total": "5409"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5409",
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
            "amount": "603384"
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
    "data": "eyJyZWYiOiJjMWZiNzkxNy1iOTZjLTU0ODItYWM5YS02M2Y3YTBhNzk4MDIifQ==",
    "nonce": 1199,
    "balances": {
      "current": "10000001480269140",
      "previous": "10000001480274554"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8496dc3f4dc5a3c58cb02a9d79c2f2f3e339457a",
    "nonce": 8,
    "balances": {
      "current": "5409",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:32.830Z",
  "updated": "2020-05-22T08:07:32.901Z",
  "id": "5ec78844b0c6090011d5aa58"
}
```
* *stageAmount*: `5409`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000015210000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000152100000000000000000000000000000000000000000000000000000000000015214deed63b69fdbb8b6b06522656833753587fb79601558e5c897f1a95ecf2acd4a853b0c5641a337bb60b051192514a9ee219cf003777eda9768c1219f5744e32121e2ba79bc138aad3e7f6ba954c1d9979ffe4259a13a0db527fdc3217d832b5000000000000000000000000000000000000000000000000000000000000001ba5d8979f8fc74b8f5bc758cd784de63850394cb804613b1c750643198f7f44871d46d81db2fc5b9e80d0f45eba230039dfecadf0f76f8edbfc6cd309598e3846001d88a9c8558d2060e995480b412e4c4ac7f9486b037c2c3db438450b1c3d7a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d9000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004af00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7fc1d54000000000000000000000000000000000000000000000000002386f2c7fc327a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000050000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000934f800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d575a694e7a6b784e7931694f545a6a4c5455304f44497459574d35595330324d325933595442684e7a6b344d44496966513d3d00000000000000000000000000000000000000000000000000000000000000080000000000000000000000008496dc3f4dc5a3c58cb02a9d79c2f2f3e339457a0000000000000000000000000000000000000000000000000000000000001521000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4deed63b69fdbb8b6b06522656833753587fb79601558e5c897f1a95ecf2acd4",
      "signature": {
        "s": "0x121e2ba79bc138aad3e7f6ba954c1d9979ffe4259a13a0db527fdc3217d832b5",
        "r": "0xa853b0c5641a337bb60b051192514a9ee219cf003777eda9768c1219f5744e32",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa5d8979f8fc74b8f5bc758cd784de63850394cb804613b1c750643198f7f4487",
      "signature": {
        "s": "0x001d88a9c8558d2060e995480b412e4c4ac7f9486b037c2c3db438450b1c3d7a",
        "r": "0x1d46d81db2fc5b9e80d0f45eba230039dfecadf0f76f8edbfc6cd309598e3846",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5409",
    "total": "5409"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5409",
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
            "amount": "603384"
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
    "data": "eyJyZWYiOiJjMWZiNzkxNy1iOTZjLTU0ODItYWM5YS02M2Y3YTBhNzk4MDIifQ==",
    "nonce": 1199,
    "balances": {
      "current": "10000001480269140",
      "previous": "10000001480274554"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8496dc3f4dc5a3c58cb02a9d79c2f2f3e339457a",
    "nonce": 8,
    "balances": {
      "current": "5409",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:32.830Z",
  "updated": "2020-05-22T08:07:32.901Z",
  "id": "5ec78844b0c6090011d5aa58"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000015210000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5409`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``