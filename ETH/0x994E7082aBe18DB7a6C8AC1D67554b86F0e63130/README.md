# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x994E7082aBe18DB7a6C8AC1D67554b86F0e63130`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000e170000000000000000000000000000000000000000000000000000000000000e1700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000e170000000000000000000000000000000000000000000000000000000000000e17ac894e43707a89b0cacd91c0113a49368c584d247578349c85abde35e99e021ad739eb4c2de5988fc46aa51f6f21e299d6572d052b1df896d27fb7621d0e682c621265186fd24f50b44b3df9d0d356a5b6a1230975527368aeffd2fe0c9dce97000000000000000000000000000000000000000000000000000000000000001b2a25bd3b18545c0a0c2556bcfc3b473ba04363f91edd606c32ccdc7d703d4ac29aa564bff7adbce0b177b300c1170c2ca128d1c637d424c311b3a3815a1402e63c4c758f2b5c5cdd732070d6d6eb3958f8986f8d4bdbdfa9cc1631175afc0a31000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d4000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000003a400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caad7b96000000000000000000000000000000000000000000000000002386f2caad89b000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000030000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000884d500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e444d774e3245785a5330785a546b774c54566a595759744f545a694d5330335a6a5578593249304e6a5a6d5a57556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000994e7082abe18db7a6c8ac1d67554b86f0e631300000000000000000000000000000000000000000000000000000000000000e17000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xac894e43707a89b0cacd91c0113a49368c584d247578349c85abde35e99e021a",
      "signature": {
        "s": "0x621265186fd24f50b44b3df9d0d356a5b6a1230975527368aeffd2fe0c9dce97",
        "r": "0xd739eb4c2de5988fc46aa51f6f21e299d6572d052b1df896d27fb7621d0e682c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2a25bd3b18545c0a0c2556bcfc3b473ba04363f91edd606c32ccdc7d703d4ac2",
      "signature": {
        "s": "0x3c4c758f2b5c5cdd732070d6d6eb3958f8986f8d4bdbdfa9cc1631175afc0a31",
        "r": "0x9aa564bff7adbce0b177b300c1170c2ca128d1c637d424c311b3a3815a1402e6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3607",
    "total": "3607"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3607",
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
            "amount": "558293"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "3"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4NDMwN2ExZS0xZTkwLTVjYWYtOTZiMS03ZjUxY2I0NjZmZWUifQ==",
    "nonce": 932,
    "balances": {
      "current": "10000001525447574",
      "previous": "10000001525451184"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x994e7082abe18db7a6c8ac1d67554b86f0e63130",
    "nonce": 20,
    "balances": {
      "current": "3607",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:05:32.602Z",
  "updated": "2020-05-22T08:05:32.692Z",
  "id": "5ec787cc005df800101bc350"
}
```
* *stageAmount*: `3607`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000e1700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000e170000000000000000000000000000000000000000000000000000000000000e17ac894e43707a89b0cacd91c0113a49368c584d247578349c85abde35e99e021ad739eb4c2de5988fc46aa51f6f21e299d6572d052b1df896d27fb7621d0e682c621265186fd24f50b44b3df9d0d356a5b6a1230975527368aeffd2fe0c9dce97000000000000000000000000000000000000000000000000000000000000001b2a25bd3b18545c0a0c2556bcfc3b473ba04363f91edd606c32ccdc7d703d4ac29aa564bff7adbce0b177b300c1170c2ca128d1c637d424c311b3a3815a1402e63c4c758f2b5c5cdd732070d6d6eb3958f8986f8d4bdbdfa9cc1631175afc0a31000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d4000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000003a400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caad7b96000000000000000000000000000000000000000000000000002386f2caad89b000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000030000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000884d500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e444d774e3245785a5330785a546b774c54566a595759744f545a694d5330335a6a5578593249304e6a5a6d5a57556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000994e7082abe18db7a6c8ac1d67554b86f0e631300000000000000000000000000000000000000000000000000000000000000e17000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xac894e43707a89b0cacd91c0113a49368c584d247578349c85abde35e99e021a",
      "signature": {
        "s": "0x621265186fd24f50b44b3df9d0d356a5b6a1230975527368aeffd2fe0c9dce97",
        "r": "0xd739eb4c2de5988fc46aa51f6f21e299d6572d052b1df896d27fb7621d0e682c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2a25bd3b18545c0a0c2556bcfc3b473ba04363f91edd606c32ccdc7d703d4ac2",
      "signature": {
        "s": "0x3c4c758f2b5c5cdd732070d6d6eb3958f8986f8d4bdbdfa9cc1631175afc0a31",
        "r": "0x9aa564bff7adbce0b177b300c1170c2ca128d1c637d424c311b3a3815a1402e6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3607",
    "total": "3607"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3607",
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
            "amount": "558293"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "3"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4NDMwN2ExZS0xZTkwLTVjYWYtOTZiMS03ZjUxY2I0NjZmZWUifQ==",
    "nonce": 932,
    "balances": {
      "current": "10000001525447574",
      "previous": "10000001525451184"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x994e7082abe18db7a6c8ac1d67554b86f0e63130",
    "nonce": 20,
    "balances": {
      "current": "3607",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:05:32.602Z",
  "updated": "2020-05-22T08:05:32.692Z",
  "id": "5ec787cc005df800101bc350"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000e170000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3607`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``