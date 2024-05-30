# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4f8C831a5F12629b1eCea05A20eB2A032f34731f`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000052c764b80000000000000000000000000000000000000000000000000000000052c764b8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000052c764b80000000000000000000000000000000000000000000000000000000052c764b8de1f6a9c918da1521adeef67f758ad087bb32c2bedb5c32456f521cf4235178b4112d496469edc2541de9eae5272e2a06c8f202ce0d68106a313d432dc69735218582d47c32ce960aac54ea9b172b78fefc778a8e836da91f1981e97d96a2fd7000000000000000000000000000000000000000000000000000000000000001cc5c2a200b605aab8aab53fd96a6a785a5511090bf28f97486ce3e4570ff1a17557feb1ad9d2a81798105343c5752041f2faf70c2962548323fc517796075bc032fbc99eea0ba66c74e9c8703787c70b4d1ef6d6f57f2ffe9cdf3eb48c948638b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56770000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000173000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b30e0d2ba55000000000000000000000000000000000000000000000000002e1b3133af500c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001530ff000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000094c38a9a9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a544d315a4752684e693033595441304c5455354f5445744f4463354f4330344e54593159324a6c4e6a45795932516966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000004f8c831a5f12629b1ecea05a20eb2a032f34731f0000000000000000000000000000000000000000000000000000000052c764b8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xde1f6a9c918da1521adeef67f758ad087bb32c2bedb5c32456f521cf4235178b",
      "signature": {
        "s": "0x18582d47c32ce960aac54ea9b172b78fefc778a8e836da91f1981e97d96a2fd7",
        "r": "0x4112d496469edc2541de9eae5272e2a06c8f202ce0d68106a313d432dc697352",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc5c2a200b605aab8aab53fd96a6a785a5511090bf28f97486ce3e4570ff1a175",
      "signature": {
        "s": "0x2fbc99eea0ba66c74e9c8703787c70b4d1ef6d6f57f2ffe9cdf3eb48c948638b",
        "r": "0x57feb1ad9d2a81798105343c5752041f2faf70c2962548323fc517796075bc03",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1388799160",
    "total": "1388799160"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1388799160",
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
            "amount": "39933487529"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1388799"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxZTM1ZGRhNi03YTA0LTU5OTEtODc5OC04NTY1Y2JlNjEyY2QifQ==",
    "nonce": 5936,
    "balances": {
      "current": "12977745672976981",
      "previous": "12977747063164940"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4f8c831a5f12629b1ecea05a20eb2a032f34731f",
    "nonce": 22,
    "balances": {
      "current": "1388799160",
      "previous": "0"
    }
  },
  "blockNumber": "10114679",
  "created": "2020-05-22T08:45:08.968Z",
  "updated": "2020-05-22T08:45:09.051Z",
  "id": "5ec79114b0c6090011d5b079"
}
```
* *stageAmount*: `1388799160`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000052c764b8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000052c764b80000000000000000000000000000000000000000000000000000000052c764b8de1f6a9c918da1521adeef67f758ad087bb32c2bedb5c32456f521cf4235178b4112d496469edc2541de9eae5272e2a06c8f202ce0d68106a313d432dc69735218582d47c32ce960aac54ea9b172b78fefc778a8e836da91f1981e97d96a2fd7000000000000000000000000000000000000000000000000000000000000001cc5c2a200b605aab8aab53fd96a6a785a5511090bf28f97486ce3e4570ff1a17557feb1ad9d2a81798105343c5752041f2faf70c2962548323fc517796075bc032fbc99eea0ba66c74e9c8703787c70b4d1ef6d6f57f2ffe9cdf3eb48c948638b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56770000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000173000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b30e0d2ba55000000000000000000000000000000000000000000000000002e1b3133af500c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001530ff000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000094c38a9a9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a544d315a4752684e693033595441304c5455354f5445744f4463354f4330344e54593159324a6c4e6a45795932516966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000004f8c831a5f12629b1ecea05a20eb2a032f34731f0000000000000000000000000000000000000000000000000000000052c764b8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xde1f6a9c918da1521adeef67f758ad087bb32c2bedb5c32456f521cf4235178b",
      "signature": {
        "s": "0x18582d47c32ce960aac54ea9b172b78fefc778a8e836da91f1981e97d96a2fd7",
        "r": "0x4112d496469edc2541de9eae5272e2a06c8f202ce0d68106a313d432dc697352",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc5c2a200b605aab8aab53fd96a6a785a5511090bf28f97486ce3e4570ff1a175",
      "signature": {
        "s": "0x2fbc99eea0ba66c74e9c8703787c70b4d1ef6d6f57f2ffe9cdf3eb48c948638b",
        "r": "0x57feb1ad9d2a81798105343c5752041f2faf70c2962548323fc517796075bc03",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1388799160",
    "total": "1388799160"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1388799160",
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
            "amount": "39933487529"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1388799"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxZTM1ZGRhNi03YTA0LTU5OTEtODc5OC04NTY1Y2JlNjEyY2QifQ==",
    "nonce": 5936,
    "balances": {
      "current": "12977745672976981",
      "previous": "12977747063164940"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4f8c831a5f12629b1ecea05a20eb2a032f34731f",
    "nonce": 22,
    "balances": {
      "current": "1388799160",
      "previous": "0"
    }
  },
  "blockNumber": "10114679",
  "created": "2020-05-22T08:45:08.968Z",
  "updated": "2020-05-22T08:45:09.051Z",
  "id": "5ec79114b0c6090011d5b079"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000052c764b8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1388799160`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`