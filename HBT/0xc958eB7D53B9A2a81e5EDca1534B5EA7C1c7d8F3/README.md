# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xc958eB7D53B9A2a81e5EDca1534B5EA7C1c7d8F3`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000ec7efc8f00000000000000000000000000000000000000000000000000000000ec7efc8f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000ec7efc8f00000000000000000000000000000000000000000000000000000000ec7efc8f1f47ab3794cbd9d1d6f4d7fc19ccde0dac850647b371e8a5a707193e30d931f97e3b5c87586cc6671e8ce3284297d7d4f49e56ab339f7ca7a2d24741015631c74b0f724c9ef37c2c8b1bee7c31cd837d1b08955fb03821c758b92af26a12f60d000000000000000000000000000000000000000000000000000000000000001c614844c77527fd7392a992d607ee172b4a910bc6cd1ad74b60514c981f64717cffcf5b9724bb3912e70592e7f3d917cb08b0e044b6839d59d1a10bf908dc97d244b60565be9d3ab548c0e1c754d96332427481b9aacfba4315548d7d6edc144f000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ced00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e12e91e0fbfed000000000000000000000000000000000000000000000000002e12ea0acb477d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000003c8b01000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b6a56838d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d6a686d4d47526c4e6930344d7a6c6b4c5455774e3249744f4445345a4330305a4759304d47457a597a686a4f544d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c958eb7d53b9a2a81e5edca1534b5ea7c1c7d8f300000000000000000000000000000000000000000000000000000000ec7efc8f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1f47ab3794cbd9d1d6f4d7fc19ccde0dac850647b371e8a5a707193e30d931f9",
      "signature": {
        "s": "0x4b0f724c9ef37c2c8b1bee7c31cd837d1b08955fb03821c758b92af26a12f60d",
        "r": "0x7e3b5c87586cc6671e8ce3284297d7d4f49e56ab339f7ca7a2d24741015631c7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x614844c77527fd7392a992d607ee172b4a910bc6cd1ad74b60514c981f64717c",
      "signature": {
        "s": "0x44b60565be9d3ab548c0e1c754d96332427481b9aacfba4315548d7d6edc144f",
        "r": "0xffcf5b9724bb3912e70592e7f3d917cb08b0e044b6839d59d1a10bf908dc97d2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3967745167",
    "total": "3967745167"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3967745167",
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
            "amount": "49028694925"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3967745"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMjhmMGRlNi04MzlkLTUwN2ItODE4ZC00ZGY0MGEzYzhjOTMifQ==",
    "nonce": 7405,
    "balances": {
      "current": "12968641369718765",
      "previous": "12968645341431677"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc958eb7d53b9a2a81e5edca1534b5ea7c1c7d8f3",
    "nonce": 22,
    "balances": {
      "current": "3967745167",
      "previous": "0"
    }
  },
  "blockNumber": "10114738",
  "created": "2020-05-22T08:56:31.852Z",
  "updated": "2020-05-22T08:56:32.932Z",
  "id": "5ec793bf005df800101bcbf0"
}
```
* *stageAmount*: `3967745167`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000ec7efc8f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000ec7efc8f00000000000000000000000000000000000000000000000000000000ec7efc8f1f47ab3794cbd9d1d6f4d7fc19ccde0dac850647b371e8a5a707193e30d931f97e3b5c87586cc6671e8ce3284297d7d4f49e56ab339f7ca7a2d24741015631c74b0f724c9ef37c2c8b1bee7c31cd837d1b08955fb03821c758b92af26a12f60d000000000000000000000000000000000000000000000000000000000000001c614844c77527fd7392a992d607ee172b4a910bc6cd1ad74b60514c981f64717cffcf5b9724bb3912e70592e7f3d917cb08b0e044b6839d59d1a10bf908dc97d244b60565be9d3ab548c0e1c754d96332427481b9aacfba4315548d7d6edc144f000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ced00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e12e91e0fbfed000000000000000000000000000000000000000000000000002e12ea0acb477d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000003c8b01000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b6a56838d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d6a686d4d47526c4e6930344d7a6c6b4c5455774e3249744f4445345a4330305a4759304d47457a597a686a4f544d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c958eb7d53b9a2a81e5edca1534b5ea7c1c7d8f300000000000000000000000000000000000000000000000000000000ec7efc8f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1f47ab3794cbd9d1d6f4d7fc19ccde0dac850647b371e8a5a707193e30d931f9",
      "signature": {
        "s": "0x4b0f724c9ef37c2c8b1bee7c31cd837d1b08955fb03821c758b92af26a12f60d",
        "r": "0x7e3b5c87586cc6671e8ce3284297d7d4f49e56ab339f7ca7a2d24741015631c7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x614844c77527fd7392a992d607ee172b4a910bc6cd1ad74b60514c981f64717c",
      "signature": {
        "s": "0x44b60565be9d3ab548c0e1c754d96332427481b9aacfba4315548d7d6edc144f",
        "r": "0xffcf5b9724bb3912e70592e7f3d917cb08b0e044b6839d59d1a10bf908dc97d2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3967745167",
    "total": "3967745167"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3967745167",
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
            "amount": "49028694925"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3967745"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMjhmMGRlNi04MzlkLTUwN2ItODE4ZC00ZGY0MGEzYzhjOTMifQ==",
    "nonce": 7405,
    "balances": {
      "current": "12968641369718765",
      "previous": "12968645341431677"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc958eb7d53b9a2a81e5edca1534b5ea7c1c7d8f3",
    "nonce": 22,
    "balances": {
      "current": "3967745167",
      "previous": "0"
    }
  },
  "blockNumber": "10114738",
  "created": "2020-05-22T08:56:31.852Z",
  "updated": "2020-05-22T08:56:32.932Z",
  "id": "5ec793bf005df800101bcbf0"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000ec7efc8f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3967745167`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`