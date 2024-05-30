# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7149de929B5F9B6D859C5898e962fEa63bbBd989`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000268b5317d0000000000000000000000000000000000000000000000000000000268b5317d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000268b5317d0000000000000000000000000000000000000000000000000000000268b5317dd9c2961bb4391cb87b8c8fe2ddf9bb5b864b585b46858e8d65d96067a7b990fdc061a790daaccd6399c6b194172ec58e0578e412f7ec9d938bb346afed4ce1d8212e86a6854cd7bbbe7bcb774e997ceb82c5d7cb5304aaf853fae3d8d7e49b5a000000000000000000000000000000000000000000000000000000000000001c09d635c888bab5758e1dda827d83955225ca922b12323c082766792b05ba8c5274b7754ee13b2758191fe414d66d81987932da74162545ec4445a8cd791b549e581f94e1012ac8d9fd619cc8a2c5063a83ccecad5f53be30f741b669f718da97000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56730000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000167300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1bb48ea3e8e4000000000000000000000000000000000000000000000000002e1bb6f7f6faf000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000009de08f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000092a8b9271000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694930597a55325a5468684f4330794d5749344c5456695a6a55744f4756694e4331684f445268597a45784e444e694e6d556966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000007149de929b5f9b6d859c5898e962fea63bbbd9890000000000000000000000000000000000000000000000000000000268b5317d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd9c2961bb4391cb87b8c8fe2ddf9bb5b864b585b46858e8d65d96067a7b990fd",
      "signature": {
        "s": "0x212e86a6854cd7bbbe7bcb774e997ceb82c5d7cb5304aaf853fae3d8d7e49b5a",
        "r": "0xc061a790daaccd6399c6b194172ec58e0578e412f7ec9d938bb346afed4ce1d8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x09d635c888bab5758e1dda827d83955225ca922b12323c082766792b05ba8c52",
      "signature": {
        "s": "0x581f94e1012ac8d9fd619cc8a2c5063a83ccecad5f53be30f741b669f718da97",
        "r": "0x74b7754ee13b2758191fe414d66d81987932da74162545ec4445a8cd791b549e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "10346639741",
    "total": "10346639741"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10346639741",
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
            "amount": "39368495729"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "10346639"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0YzU2ZThhOC0yMWI4LTViZjUtOGViNC1hODRhYzExNDNiNmUifQ==",
    "nonce": 5747,
    "balances": {
      "current": "12978311229860068",
      "previous": "12978321586846448"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7149de929b5f9b6d859c5898e962fea63bbbd989",
    "nonce": 22,
    "balances": {
      "current": "10346639741",
      "previous": "0"
    }
  },
  "blockNumber": "10114675",
  "created": "2020-05-22T08:43:29.014Z",
  "updated": "2020-05-22T08:43:29.084Z",
  "id": "5ec790b1e5756b00111b86c9"
}
```
* *stageAmount*: `10346639741`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000268b5317d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000268b5317d0000000000000000000000000000000000000000000000000000000268b5317dd9c2961bb4391cb87b8c8fe2ddf9bb5b864b585b46858e8d65d96067a7b990fdc061a790daaccd6399c6b194172ec58e0578e412f7ec9d938bb346afed4ce1d8212e86a6854cd7bbbe7bcb774e997ceb82c5d7cb5304aaf853fae3d8d7e49b5a000000000000000000000000000000000000000000000000000000000000001c09d635c888bab5758e1dda827d83955225ca922b12323c082766792b05ba8c5274b7754ee13b2758191fe414d66d81987932da74162545ec4445a8cd791b549e581f94e1012ac8d9fd619cc8a2c5063a83ccecad5f53be30f741b669f718da97000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56730000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000167300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1bb48ea3e8e4000000000000000000000000000000000000000000000000002e1bb6f7f6faf000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000009de08f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000092a8b9271000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694930597a55325a5468684f4330794d5749344c5456695a6a55744f4756694e4331684f445268597a45784e444e694e6d556966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000007149de929b5f9b6d859c5898e962fea63bbbd9890000000000000000000000000000000000000000000000000000000268b5317d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd9c2961bb4391cb87b8c8fe2ddf9bb5b864b585b46858e8d65d96067a7b990fd",
      "signature": {
        "s": "0x212e86a6854cd7bbbe7bcb774e997ceb82c5d7cb5304aaf853fae3d8d7e49b5a",
        "r": "0xc061a790daaccd6399c6b194172ec58e0578e412f7ec9d938bb346afed4ce1d8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x09d635c888bab5758e1dda827d83955225ca922b12323c082766792b05ba8c52",
      "signature": {
        "s": "0x581f94e1012ac8d9fd619cc8a2c5063a83ccecad5f53be30f741b669f718da97",
        "r": "0x74b7754ee13b2758191fe414d66d81987932da74162545ec4445a8cd791b549e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "10346639741",
    "total": "10346639741"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10346639741",
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
            "amount": "39368495729"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "10346639"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0YzU2ZThhOC0yMWI4LTViZjUtOGViNC1hODRhYzExNDNiNmUifQ==",
    "nonce": 5747,
    "balances": {
      "current": "12978311229860068",
      "previous": "12978321586846448"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7149de929b5f9b6d859c5898e962fea63bbbd989",
    "nonce": 22,
    "balances": {
      "current": "10346639741",
      "previous": "0"
    }
  },
  "blockNumber": "10114675",
  "created": "2020-05-22T08:43:29.014Z",
  "updated": "2020-05-22T08:43:29.084Z",
  "id": "5ec790b1e5756b00111b86c9"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000268b5317d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `10346639741`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`