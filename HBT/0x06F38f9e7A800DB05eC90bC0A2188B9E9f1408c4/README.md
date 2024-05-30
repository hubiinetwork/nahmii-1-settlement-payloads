# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x06F38f9e7A800DB05eC90bC0A2188B9E9f1408c4`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000035da5d310000000000000000000000000000000000000000000000000000000035da5d31000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000035da5d310000000000000000000000000000000000000000000000000000000035da5d31bc838eaf5129359e577196b9fff99e7e272ad5f660e7a0e6979a44f0c3b29dd98938498d6247c02adb327aa83a9b89a62d0d153ffe2f27496c211f42882983871463a60ca9c32cd96c48709a1204852c531089ad25cb348ae83bf35f14c22944000000000000000000000000000000000000000000000000000000000000001bc1f1fb89cc7848c2b53b087f4c5f4286a2eda588e5737789193aa5ea6809e68b5ede88d6dcbc6c297e682f7675b999f93445b095b348060f8a40bf61dc91652229c96e32ba404d8f98b37ac000687aa1f3c7c9bfe0abbb8baf36b03e0327747a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56680000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000156100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d61e856f9a3000000000000000000000000000000000000000000000000002e1d621e3f202300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000dc94f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008bcbdc6a0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949795a5759305a445a6a4e5330344d44417a4c5455354e32557459546b324e4330334e6a49344f574a6d4e4464694d54416966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000006f38f9e7a800db05ec90bc0a2188b9e9f1408c40000000000000000000000000000000000000000000000000000000035da5d31000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbc838eaf5129359e577196b9fff99e7e272ad5f660e7a0e6979a44f0c3b29dd9",
      "signature": {
        "s": "0x1463a60ca9c32cd96c48709a1204852c531089ad25cb348ae83bf35f14c22944",
        "r": "0x8938498d6247c02adb327aa83a9b89a62d0d153ffe2f27496c211f4288298387",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc1f1fb89cc7848c2b53b087f4c5f4286a2eda588e5737789193aa5ea6809e68b",
      "signature": {
        "s": "0x29c96e32ba404d8f98b37ac000687aa1f3c7c9bfe0abbb8baf36b03e0327747a",
        "r": "0x5ede88d6dcbc6c297e682f7675b999f93445b095b348060f8a40bf61dc916522",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "903503153",
    "total": "903503153"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "903503153",
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
            "amount": "37526292128"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "903503"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyZWY0ZDZjNS04MDAzLTU5N2UtYTk2NC03NjI4OWJmNDdiMTAifQ==",
    "nonce": 5473,
    "balances": {
      "current": "12980155275737507",
      "previous": "12980156180144163"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x06f38f9e7a800db05ec90bc0a2188b9e9f1408c4",
    "nonce": 22,
    "balances": {
      "current": "903503153",
      "previous": "0"
    }
  },
  "blockNumber": "10114664",
  "created": "2020-05-22T08:41:23.014Z",
  "updated": "2020-05-22T08:41:23.082Z",
  "id": "5ec79033b0c6090011d5afdf"
}
```
* *stageAmount*: `903503153`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000035da5d31000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000035da5d310000000000000000000000000000000000000000000000000000000035da5d31bc838eaf5129359e577196b9fff99e7e272ad5f660e7a0e6979a44f0c3b29dd98938498d6247c02adb327aa83a9b89a62d0d153ffe2f27496c211f42882983871463a60ca9c32cd96c48709a1204852c531089ad25cb348ae83bf35f14c22944000000000000000000000000000000000000000000000000000000000000001bc1f1fb89cc7848c2b53b087f4c5f4286a2eda588e5737789193aa5ea6809e68b5ede88d6dcbc6c297e682f7675b999f93445b095b348060f8a40bf61dc91652229c96e32ba404d8f98b37ac000687aa1f3c7c9bfe0abbb8baf36b03e0327747a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56680000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000156100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d61e856f9a3000000000000000000000000000000000000000000000000002e1d621e3f202300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000dc94f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008bcbdc6a0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949795a5759305a445a6a4e5330344d44417a4c5455354e32557459546b324e4330334e6a49344f574a6d4e4464694d54416966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000006f38f9e7a800db05ec90bc0a2188b9e9f1408c40000000000000000000000000000000000000000000000000000000035da5d31000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbc838eaf5129359e577196b9fff99e7e272ad5f660e7a0e6979a44f0c3b29dd9",
      "signature": {
        "s": "0x1463a60ca9c32cd96c48709a1204852c531089ad25cb348ae83bf35f14c22944",
        "r": "0x8938498d6247c02adb327aa83a9b89a62d0d153ffe2f27496c211f4288298387",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc1f1fb89cc7848c2b53b087f4c5f4286a2eda588e5737789193aa5ea6809e68b",
      "signature": {
        "s": "0x29c96e32ba404d8f98b37ac000687aa1f3c7c9bfe0abbb8baf36b03e0327747a",
        "r": "0x5ede88d6dcbc6c297e682f7675b999f93445b095b348060f8a40bf61dc916522",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "903503153",
    "total": "903503153"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "903503153",
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
            "amount": "37526292128"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "903503"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyZWY0ZDZjNS04MDAzLTU5N2UtYTk2NC03NjI4OWJmNDdiMTAifQ==",
    "nonce": 5473,
    "balances": {
      "current": "12980155275737507",
      "previous": "12980156180144163"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x06f38f9e7a800db05ec90bc0a2188b9e9f1408c4",
    "nonce": 22,
    "balances": {
      "current": "903503153",
      "previous": "0"
    }
  },
  "blockNumber": "10114664",
  "created": "2020-05-22T08:41:23.014Z",
  "updated": "2020-05-22T08:41:23.082Z",
  "id": "5ec79033b0c6090011d5afdf"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000035da5d31000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `903503153`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`