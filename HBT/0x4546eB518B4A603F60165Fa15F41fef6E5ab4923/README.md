# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4546eB518B4A603F60165Fa15F41fef6E5ab4923`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000002550000000000000000000000000000000000000000000000000000000000000255000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000002550000000000000000000000000000000000000000000000000000000000000255a700c89635bf8040105f3d73ce11c7a3f2bde8569b25dd7ca38e9cf819f7a6fc3a25bd6da43bf62aa27c89150f3f5139f33103d8c9bc568593ea409df17f761e56b92a67d67b250a27157f5653f7669e103e91254ee659e1a50ffa56b3e63a90000000000000000000000000000000000000000000000000000000000000001b0cb74ef271b69084a453c881b262a9bf08e226657160c79806da063f8d9c9e0f22d6c466a0fec597f0048113d878c4d4339882f654ae12582765501188f6827552485ab69a6f2f66fd2f3da69a2143f942306827e118ea0f53093b888a8a237a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56670000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000154100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d6d86aa5304000000000000000000000000000000000000000000000000002e1d6d86aa555a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008b9c51bfd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d7a56695a5452694d43316d4d6d52694c5455784e4745745954646d5a5330344e6d4d355a546b355a544d315957456966513d3d00000000000000000000000000000000000000000000000000000000000000150000000000000000000000004546eb518b4a603f60165fa15f41fef6e5ab49230000000000000000000000000000000000000000000000000000000000000255000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa700c89635bf8040105f3d73ce11c7a3f2bde8569b25dd7ca38e9cf819f7a6fc",
      "signature": {
        "s": "0x56b92a67d67b250a27157f5653f7669e103e91254ee659e1a50ffa56b3e63a90",
        "r": "0x3a25bd6da43bf62aa27c89150f3f5139f33103d8c9bc568593ea409df17f761e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0cb74ef271b69084a453c881b262a9bf08e226657160c79806da063f8d9c9e0f",
      "signature": {
        "s": "0x52485ab69a6f2f66fd2f3da69a2143f942306827e118ea0f53093b888a8a237a",
        "r": "0x22d6c466a0fec597f0048113d878c4d4339882f654ae12582765501188f68275",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "597",
    "total": "597"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "597",
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
            "amount": "37476441085"
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
    "data": "eyJyZWYiOiIzMzViZTRiMC1mMmRiLTUxNGEtYTdmZS04NmM5ZTk5ZTM1YWEifQ==",
    "nonce": 5441,
    "balances": {
      "current": "12980205176640260",
      "previous": "12980205176640858"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4546eb518b4a603f60165fa15f41fef6e5ab4923",
    "nonce": 21,
    "balances": {
      "current": "597",
      "previous": "0"
    }
  },
  "blockNumber": "10114663",
  "created": "2020-05-22T08:41:07.906Z",
  "updated": "2020-05-22T08:41:07.979Z",
  "id": "5ec79023005df800101bc956"
}
```
* *stageAmount*: `597`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000255000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000002550000000000000000000000000000000000000000000000000000000000000255a700c89635bf8040105f3d73ce11c7a3f2bde8569b25dd7ca38e9cf819f7a6fc3a25bd6da43bf62aa27c89150f3f5139f33103d8c9bc568593ea409df17f761e56b92a67d67b250a27157f5653f7669e103e91254ee659e1a50ffa56b3e63a90000000000000000000000000000000000000000000000000000000000000001b0cb74ef271b69084a453c881b262a9bf08e226657160c79806da063f8d9c9e0f22d6c466a0fec597f0048113d878c4d4339882f654ae12582765501188f6827552485ab69a6f2f66fd2f3da69a2143f942306827e118ea0f53093b888a8a237a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56670000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000154100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d6d86aa5304000000000000000000000000000000000000000000000000002e1d6d86aa555a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008b9c51bfd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d7a56695a5452694d43316d4d6d52694c5455784e4745745954646d5a5330344e6d4d355a546b355a544d315957456966513d3d00000000000000000000000000000000000000000000000000000000000000150000000000000000000000004546eb518b4a603f60165fa15f41fef6e5ab49230000000000000000000000000000000000000000000000000000000000000255000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa700c89635bf8040105f3d73ce11c7a3f2bde8569b25dd7ca38e9cf819f7a6fc",
      "signature": {
        "s": "0x56b92a67d67b250a27157f5653f7669e103e91254ee659e1a50ffa56b3e63a90",
        "r": "0x3a25bd6da43bf62aa27c89150f3f5139f33103d8c9bc568593ea409df17f761e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0cb74ef271b69084a453c881b262a9bf08e226657160c79806da063f8d9c9e0f",
      "signature": {
        "s": "0x52485ab69a6f2f66fd2f3da69a2143f942306827e118ea0f53093b888a8a237a",
        "r": "0x22d6c466a0fec597f0048113d878c4d4339882f654ae12582765501188f68275",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "597",
    "total": "597"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "597",
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
            "amount": "37476441085"
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
    "data": "eyJyZWYiOiIzMzViZTRiMC1mMmRiLTUxNGEtYTdmZS04NmM5ZTk5ZTM1YWEifQ==",
    "nonce": 5441,
    "balances": {
      "current": "12980205176640260",
      "previous": "12980205176640858"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4546eb518b4a603f60165fa15f41fef6e5ab4923",
    "nonce": 21,
    "balances": {
      "current": "597",
      "previous": "0"
    }
  },
  "blockNumber": "10114663",
  "created": "2020-05-22T08:41:07.906Z",
  "updated": "2020-05-22T08:41:07.979Z",
  "id": "5ec79023005df800101bc956"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000255000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `597`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`