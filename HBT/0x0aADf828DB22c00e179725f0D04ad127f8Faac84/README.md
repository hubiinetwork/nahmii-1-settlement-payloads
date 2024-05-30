# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0aADf828DB22c00e179725f0D04ad127f8Faac84`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000001a42e082000000000000000000000000000000000000000000000000000000001a42e082000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001a42e082000000000000000000000000000000000000000000000000000000001a42e0826d11bd3866bec68e86bcfa39f842ba466c9cc7403c95c6ceff5361489f9ff19eb8748992998de52ca35dfa0637fd17e2cd5caca50c79b17a322acba9f4f7d5d24c818bff67408a1015be670c27e448d6c16631a68f8abea1b9d9bea8fbbd0f87000000000000000000000000000000000000000000000000000000000000001c6830dac91e28a99e378721cfaece358dba93d1c358a5deba6e5718662226a2e93c1203b79048d80ec5ec6c228a9633d7e6a9d54cc53fd98e6ee62f04a6c12a290a4595c2fe3dbb170e74807276a56842e3551109fbc699be828a88547ad6b566000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569c00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ab000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e162edca4a852000000000000000000000000000000000000000000000000002e162ef6ee41e200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000006b90e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a9416f1d4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e7a49354f54426a5a5331694e6a4a6a4c54566b4d4449744f4755334e5330335a5745314f574e6c4d6a4e684f54516966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000000aadf828db22c00e179725f0d04ad127f8faac84000000000000000000000000000000000000000000000000000000001a42e082000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6d11bd3866bec68e86bcfa39f842ba466c9cc7403c95c6ceff5361489f9ff19e",
      "signature": {
        "s": "0x4c818bff67408a1015be670c27e448d6c16631a68f8abea1b9d9bea8fbbd0f87",
        "r": "0xb8748992998de52ca35dfa0637fd17e2cd5caca50c79b17a322acba9f4f7d5d2",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6830dac91e28a99e378721cfaece358dba93d1c358a5deba6e5718662226a2e9",
      "signature": {
        "s": "0x0a4595c2fe3dbb170e74807276a56842e3551109fbc699be828a88547ad6b566",
        "r": "0x3c1203b79048d80ec5ec6c228a9633d7e6a9d54cc53fd98e6ee62f04a6c12a29",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "440590466",
    "total": "440590466"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "440590466",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "45434204628"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "440590"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4NzI5OTBjZS1iNjJjLTVkMDItOGU3NS03ZWE1OWNlMjNhOTQifQ==",
    "nonce": 6832,
    "balances": {
      "current": "12972239454775378",
      "previous": "12972239895806434"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0aadf828db22c00e179725f0d04ad127f8faac84",
    "nonce": 22,
    "balances": {
      "current": "440590466",
      "previous": "0"
    }
  },
  "blockNumber": "10114716",
  "created": "2020-05-22T08:52:00.135Z",
  "updated": "2020-05-22T08:52:00.207Z",
  "id": "5ec792b0b0c6090011d5b1b0"
}
```
* *stageAmount*: `440590466`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000001a42e082000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001a42e082000000000000000000000000000000000000000000000000000000001a42e0826d11bd3866bec68e86bcfa39f842ba466c9cc7403c95c6ceff5361489f9ff19eb8748992998de52ca35dfa0637fd17e2cd5caca50c79b17a322acba9f4f7d5d24c818bff67408a1015be670c27e448d6c16631a68f8abea1b9d9bea8fbbd0f87000000000000000000000000000000000000000000000000000000000000001c6830dac91e28a99e378721cfaece358dba93d1c358a5deba6e5718662226a2e93c1203b79048d80ec5ec6c228a9633d7e6a9d54cc53fd98e6ee62f04a6c12a290a4595c2fe3dbb170e74807276a56842e3551109fbc699be828a88547ad6b566000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569c00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ab000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e162edca4a852000000000000000000000000000000000000000000000000002e162ef6ee41e200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000006b90e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a9416f1d4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e7a49354f54426a5a5331694e6a4a6a4c54566b4d4449744f4755334e5330335a5745314f574e6c4d6a4e684f54516966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000000aadf828db22c00e179725f0d04ad127f8faac84000000000000000000000000000000000000000000000000000000001a42e082000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6d11bd3866bec68e86bcfa39f842ba466c9cc7403c95c6ceff5361489f9ff19e",
      "signature": {
        "s": "0x4c818bff67408a1015be670c27e448d6c16631a68f8abea1b9d9bea8fbbd0f87",
        "r": "0xb8748992998de52ca35dfa0637fd17e2cd5caca50c79b17a322acba9f4f7d5d2",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6830dac91e28a99e378721cfaece358dba93d1c358a5deba6e5718662226a2e9",
      "signature": {
        "s": "0x0a4595c2fe3dbb170e74807276a56842e3551109fbc699be828a88547ad6b566",
        "r": "0x3c1203b79048d80ec5ec6c228a9633d7e6a9d54cc53fd98e6ee62f04a6c12a29",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "440590466",
    "total": "440590466"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "440590466",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "45434204628"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "440590"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4NzI5OTBjZS1iNjJjLTVkMDItOGU3NS03ZWE1OWNlMjNhOTQifQ==",
    "nonce": 6832,
    "balances": {
      "current": "12972239454775378",
      "previous": "12972239895806434"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0aadf828db22c00e179725f0d04ad127f8faac84",
    "nonce": 22,
    "balances": {
      "current": "440590466",
      "previous": "0"
    }
  },
  "blockNumber": "10114716",
  "created": "2020-05-22T08:52:00.135Z",
  "updated": "2020-05-22T08:52:00.207Z",
  "id": "5ec792b0b0c6090011d5b1b0"
}
```
* *standard*: `ERC20`
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b000000000000000000000000000000000000000000000000000000001a42e082000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `440590466`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`