# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6fCCE26576b1A36A617d81d88E9e323D4B2330C7`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000006a084651000000000000000000000000000000000000000000000000000000006a084651000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000006a084651000000000000000000000000000000000000000000000000000000006a084651771870460b754ba8ee56984380205ab97cbf4cdee6db0e0e21d818ec4d4146984c0452c3ac3d766a5a9f885c97c8384d97eb402821ed6b4b7df163c43e32a17e7eec93301bca4e7a664367a1c931a851a7898ce834a68562cef6c96a22e5fb3e000000000000000000000000000000000000000000000000000000000000001b98ccb43fc824f84335d9ec0a1f243d723e25e3d3b74f664f495deb174ef201aa59d91a1ddfe5515ceb705b2234f59d79810eec842ee72d63a9e745fdbbdb6a065b4129272addfb4bce418836acb0540d6a756538db7e8ea78ec39db21794d97d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569b00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a5700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e16b49b637435000000000000000000000000000000000000000000000000002e16b50586df7500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001b24ef000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a71e2952c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784f474d344f5451324f4330795a6a41794c545578596a67744f574a6b4e4330344f5755785a445a6d4e6a6c6a4d7a636966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000006fcce26576b1a36a617d81d88e9e323d4b2330c7000000000000000000000000000000000000000000000000000000006a084651000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x771870460b754ba8ee56984380205ab97cbf4cdee6db0e0e21d818ec4d414698",
      "signature": {
        "s": "0x7eec93301bca4e7a664367a1c931a851a7898ce834a68562cef6c96a22e5fb3e",
        "r": "0x4c0452c3ac3d766a5a9f885c97c8384d97eb402821ed6b4b7df163c43e32a17e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x98ccb43fc824f84335d9ec0a1f243d723e25e3d3b74f664f495deb174ef201aa",
      "signature": {
        "s": "0x5b4129272addfb4bce418836acb0540d6a756538db7e8ea78ec39db21794d97d",
        "r": "0x59d91a1ddfe5515ceb705b2234f59d79810eec842ee72d63a9e745fdbbdb6a06",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1778927185",
    "total": "1778927185"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1778927185",
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
            "amount": "44860347692"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1778927"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxOGM4OTQ2OC0yZjAyLTUxYjgtOWJkNC04OWUxZDZmNjljMzcifQ==",
    "nonce": 6743,
    "balances": {
      "current": "12972813885600821",
      "previous": "12972815666306933"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6fcce26576b1a36a617d81d88e9e323d4b2330c7",
    "nonce": 22,
    "balances": {
      "current": "1778927185",
      "previous": "0"
    }
  },
  "blockNumber": "10114715",
  "created": "2020-05-22T08:51:22.210Z",
  "updated": "2020-05-22T08:51:22.276Z",
  "id": "5ec7928ab0c6090011d5b191"
}
```
* *stageAmount*: `1778927185`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000006a084651000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000006a084651000000000000000000000000000000000000000000000000000000006a084651771870460b754ba8ee56984380205ab97cbf4cdee6db0e0e21d818ec4d4146984c0452c3ac3d766a5a9f885c97c8384d97eb402821ed6b4b7df163c43e32a17e7eec93301bca4e7a664367a1c931a851a7898ce834a68562cef6c96a22e5fb3e000000000000000000000000000000000000000000000000000000000000001b98ccb43fc824f84335d9ec0a1f243d723e25e3d3b74f664f495deb174ef201aa59d91a1ddfe5515ceb705b2234f59d79810eec842ee72d63a9e745fdbbdb6a065b4129272addfb4bce418836acb0540d6a756538db7e8ea78ec39db21794d97d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569b00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a5700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e16b49b637435000000000000000000000000000000000000000000000000002e16b50586df7500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001b24ef000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a71e2952c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784f474d344f5451324f4330795a6a41794c545578596a67744f574a6b4e4330344f5755785a445a6d4e6a6c6a4d7a636966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000006fcce26576b1a36a617d81d88e9e323d4b2330c7000000000000000000000000000000000000000000000000000000006a084651000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x771870460b754ba8ee56984380205ab97cbf4cdee6db0e0e21d818ec4d414698",
      "signature": {
        "s": "0x7eec93301bca4e7a664367a1c931a851a7898ce834a68562cef6c96a22e5fb3e",
        "r": "0x4c0452c3ac3d766a5a9f885c97c8384d97eb402821ed6b4b7df163c43e32a17e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x98ccb43fc824f84335d9ec0a1f243d723e25e3d3b74f664f495deb174ef201aa",
      "signature": {
        "s": "0x5b4129272addfb4bce418836acb0540d6a756538db7e8ea78ec39db21794d97d",
        "r": "0x59d91a1ddfe5515ceb705b2234f59d79810eec842ee72d63a9e745fdbbdb6a06",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1778927185",
    "total": "1778927185"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1778927185",
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
            "amount": "44860347692"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1778927"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxOGM4OTQ2OC0yZjAyLTUxYjgtOWJkNC04OWUxZDZmNjljMzcifQ==",
    "nonce": 6743,
    "balances": {
      "current": "12972813885600821",
      "previous": "12972815666306933"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6fcce26576b1a36a617d81d88e9e323d4b2330c7",
    "nonce": 22,
    "balances": {
      "current": "1778927185",
      "previous": "0"
    }
  },
  "blockNumber": "10114715",
  "created": "2020-05-22T08:51:22.210Z",
  "updated": "2020-05-22T08:51:22.276Z",
  "id": "5ec7928ab0c6090011d5b191"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000006a084651000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1778927185`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`