# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xCa253fE65D86E0a1848864184C170FaaC021F862`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006a700000000000000000000000000000000000000000000000000000000000006a7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000006a700000000000000000000000000000000000000000000000000000000000006a7ccf396099971d75cd3e60b2eccf027dd4ea2b0e8e2f6a1f38106822f8fb9606d55d3423b546885493eb5e6b86db14f6c43366ad06aa66dac87a3fbc866ba60d8401c7a4abf8b842a78b9ed01c1ae0519e7b3b3b6062ca30209309661ffe5a039000000000000000000000000000000000000000000000000000000000000001c839e0a79dfbc083a0308984b770e3d51c5b184a72950f3b5867e6a1ac9fee88c1f32dc51d9f7c58987f30e1f15e79ac61351a282bca68b761812cbc247dbb5b82284b83d19bc94a42d1d0b5ee19399fe61ab88113ba16f45b120b90adf5d1542000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56c600000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ed800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0aeb259ccc07000000000000000000000000000000000000000000000000002e0aeb259cd2af00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d75954859000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684e474a6c5a5449324d4330344e445a694c5455354d545574596a51774d43307a4d57526c597a5a694f474d334d44416966513d3d0000000000000000000000000000000000000000000000000000000000000006000000000000000000000000ca253fe65d86e0a1848864184c170faac021f86200000000000000000000000000000000000000000000000000000000000006a7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xccf396099971d75cd3e60b2eccf027dd4ea2b0e8e2f6a1f38106822f8fb9606d",
      "signature": {
        "s": "0x401c7a4abf8b842a78b9ed01c1ae0519e7b3b3b6062ca30209309661ffe5a039",
        "r": "0x55d3423b546885493eb5e6b86db14f6c43366ad06aa66dac87a3fbc866ba60d8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x839e0a79dfbc083a0308984b770e3d51c5b184a72950f3b5867e6a1ac9fee88c",
      "signature": {
        "s": "0x2284b83d19bc94a42d1d0b5ee19399fe61ab88113ba16f45b120b90adf5d1542",
        "r": "0x1f32dc51d9f7c58987f30e1f15e79ac61351a282bca68b761812cbc247dbb5b8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1703",
    "total": "1703"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1703",
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
            "amount": "57807292505"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhNGJlZTI2MC04NDZiLTU5MTUtYjQwMC0zMWRlYzZiOGM3MDAifQ==",
    "nonce": 7896,
    "balances": {
      "current": "12959853993315335",
      "previous": "12959853993317039"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xca253fe65d86e0a1848864184c170faac021f862",
    "nonce": 6,
    "balances": {
      "current": "1703",
      "previous": "0"
    }
  },
  "blockNumber": "10114758",
  "created": "2020-05-22T09:00:23.739Z",
  "updated": "2020-05-22T09:00:23.884Z",
  "id": "5ec794a7005df800101bcc98"
}
```
* *stageAmount*: `1703`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000006a7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000006a700000000000000000000000000000000000000000000000000000000000006a7ccf396099971d75cd3e60b2eccf027dd4ea2b0e8e2f6a1f38106822f8fb9606d55d3423b546885493eb5e6b86db14f6c43366ad06aa66dac87a3fbc866ba60d8401c7a4abf8b842a78b9ed01c1ae0519e7b3b3b6062ca30209309661ffe5a039000000000000000000000000000000000000000000000000000000000000001c839e0a79dfbc083a0308984b770e3d51c5b184a72950f3b5867e6a1ac9fee88c1f32dc51d9f7c58987f30e1f15e79ac61351a282bca68b761812cbc247dbb5b82284b83d19bc94a42d1d0b5ee19399fe61ab88113ba16f45b120b90adf5d1542000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56c600000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ed800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0aeb259ccc07000000000000000000000000000000000000000000000000002e0aeb259cd2af00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d75954859000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684e474a6c5a5449324d4330344e445a694c5455354d545574596a51774d43307a4d57526c597a5a694f474d334d44416966513d3d0000000000000000000000000000000000000000000000000000000000000006000000000000000000000000ca253fe65d86e0a1848864184c170faac021f86200000000000000000000000000000000000000000000000000000000000006a7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xccf396099971d75cd3e60b2eccf027dd4ea2b0e8e2f6a1f38106822f8fb9606d",
      "signature": {
        "s": "0x401c7a4abf8b842a78b9ed01c1ae0519e7b3b3b6062ca30209309661ffe5a039",
        "r": "0x55d3423b546885493eb5e6b86db14f6c43366ad06aa66dac87a3fbc866ba60d8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x839e0a79dfbc083a0308984b770e3d51c5b184a72950f3b5867e6a1ac9fee88c",
      "signature": {
        "s": "0x2284b83d19bc94a42d1d0b5ee19399fe61ab88113ba16f45b120b90adf5d1542",
        "r": "0x1f32dc51d9f7c58987f30e1f15e79ac61351a282bca68b761812cbc247dbb5b8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1703",
    "total": "1703"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1703",
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
            "amount": "57807292505"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhNGJlZTI2MC04NDZiLTU5MTUtYjQwMC0zMWRlYzZiOGM3MDAifQ==",
    "nonce": 7896,
    "balances": {
      "current": "12959853993315335",
      "previous": "12959853993317039"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xca253fe65d86e0a1848864184c170faac021f862",
    "nonce": 6,
    "balances": {
      "current": "1703",
      "previous": "0"
    }
  },
  "blockNumber": "10114758",
  "created": "2020-05-22T09:00:23.739Z",
  "updated": "2020-05-22T09:00:23.884Z",
  "id": "5ec794a7005df800101bcc98"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000006a7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1703`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`