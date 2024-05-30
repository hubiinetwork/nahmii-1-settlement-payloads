# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xa5a701DD1B3591b81824dcF5f051aaF03854921d`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000304960000000000000000000000000000000000000000000000000000000000030496000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000003049600000000000000000000000000000000000000000000000000000000000304969f6d98b7a53737309b3cf24ce855a50018adb78605ab4d188529e0cd595d48853ecfa21d2b195c367851281972fb13444230b5dfe367e089d08dd31240a5f0f1058f4ca4c4a9a4282f46967887b606063afabaae70777dbc7255feac117b20ad000000000000000000000000000000000000000000000000000000000000001b0801b91e6c6ad52c7657c27e11caea122ae03edff2ba2a1c78ce2d8a47ade1a3253eee4d0640fce6f4cd523a8db67860e2d976fc155434034e9c5f00f3b9abc523548457b1d53782f60dd311c517081fcc3a63589af86a137e06df4bc84d74be000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000192900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e180f5dc1db5b000000000000000000000000000000000000000000000000002e180f5dc4e0b600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000c5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a193412a6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694932597a466a4f446c6a4e79307a4f474d324c54566c5a444d74595441774f4330314f544a6b5a4749344d5468695a54416966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000a5a701dd1b3591b81824dcf5f051aaf03854921d0000000000000000000000000000000000000000000000000000000000030496000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9f6d98b7a53737309b3cf24ce855a50018adb78605ab4d188529e0cd595d4885",
      "signature": {
        "s": "0x058f4ca4c4a9a4282f46967887b606063afabaae70777dbc7255feac117b20ad",
        "r": "0x3ecfa21d2b195c367851281972fb13444230b5dfe367e089d08dd31240a5f0f1",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0801b91e6c6ad52c7657c27e11caea122ae03edff2ba2a1c78ce2d8a47ade1a3",
      "signature": {
        "s": "0x23548457b1d53782f60dd311c517081fcc3a63589af86a137e06df4bc84d74be",
        "r": "0x253eee4d0640fce6f4cd523a8db67860e2d976fc155434034e9c5f00f3b9abc5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "197782",
    "total": "197782"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "197782",
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
            "amount": "43372516006"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "197"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2YzFjODljNy0zOGM2LTVlZDMtYTAwOC01OTJkZGI4MThiZTAifQ==",
    "nonce": 6441,
    "balances": {
      "current": "12974303205251931",
      "previous": "12974303205449910"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa5a701dd1b3591b81824dcf5f051aaf03854921d",
    "nonce": 22,
    "balances": {
      "current": "197782",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:12.182Z",
  "updated": "2020-05-22T08:49:12.248Z",
  "id": "5ec79208005df800101bcaa3"
}
```
* *stageAmount*: `197782`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000030496000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000003049600000000000000000000000000000000000000000000000000000000000304969f6d98b7a53737309b3cf24ce855a50018adb78605ab4d188529e0cd595d48853ecfa21d2b195c367851281972fb13444230b5dfe367e089d08dd31240a5f0f1058f4ca4c4a9a4282f46967887b606063afabaae70777dbc7255feac117b20ad000000000000000000000000000000000000000000000000000000000000001b0801b91e6c6ad52c7657c27e11caea122ae03edff2ba2a1c78ce2d8a47ade1a3253eee4d0640fce6f4cd523a8db67860e2d976fc155434034e9c5f00f3b9abc523548457b1d53782f60dd311c517081fcc3a63589af86a137e06df4bc84d74be000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000192900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e180f5dc1db5b000000000000000000000000000000000000000000000000002e180f5dc4e0b600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000c5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a193412a6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694932597a466a4f446c6a4e79307a4f474d324c54566c5a444d74595441774f4330314f544a6b5a4749344d5468695a54416966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000a5a701dd1b3591b81824dcf5f051aaf03854921d0000000000000000000000000000000000000000000000000000000000030496000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9f6d98b7a53737309b3cf24ce855a50018adb78605ab4d188529e0cd595d4885",
      "signature": {
        "s": "0x058f4ca4c4a9a4282f46967887b606063afabaae70777dbc7255feac117b20ad",
        "r": "0x3ecfa21d2b195c367851281972fb13444230b5dfe367e089d08dd31240a5f0f1",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0801b91e6c6ad52c7657c27e11caea122ae03edff2ba2a1c78ce2d8a47ade1a3",
      "signature": {
        "s": "0x23548457b1d53782f60dd311c517081fcc3a63589af86a137e06df4bc84d74be",
        "r": "0x253eee4d0640fce6f4cd523a8db67860e2d976fc155434034e9c5f00f3b9abc5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "197782",
    "total": "197782"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "197782",
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
            "amount": "43372516006"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "197"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2YzFjODljNy0zOGM2LTVlZDMtYTAwOC01OTJkZGI4MThiZTAifQ==",
    "nonce": 6441,
    "balances": {
      "current": "12974303205251931",
      "previous": "12974303205449910"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa5a701dd1b3591b81824dcf5f051aaf03854921d",
    "nonce": 22,
    "balances": {
      "current": "197782",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:12.182Z",
  "updated": "2020-05-22T08:49:12.248Z",
  "id": "5ec79208005df800101bcaa3"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000030496000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `197782`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`