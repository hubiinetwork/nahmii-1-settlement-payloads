# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x49e82e6BF1CAebF67F3c4472C0c353361d266672`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000037f9c13d7000000000000000000000000000000000000000000000000000000037f9c13d7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000037f9c13d7000000000000000000000000000000000000000000000000000000037f9c13d71de7335bbc895de9c9180fba7e38c3a5ae5859de73a877b18fdadf6e84044e51915a9c5be373b9bb08d722690da75b6c5eab148e385e1ef97fdce43a8d85e2f21c2104e9974cc9ccce8fed1b3871b2cbf97b8197f5180cb1bb9269f0afbb3947000000000000000000000000000000000000000000000000000000000000001c067f88372243cbe1c7bc6d3955347813f326485f774e2560cacc0155c899025bf90f17f714b0752dc5ed2ec894bd3dcfb9b77625cc6d7e0dd65b81136a29481253c4d7aa2b5763b366ea5e1132f412de4c3536dd47d72799a04d20d3e7806391000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5662000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014c000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e234b1233c030000000000000000000000000000000000000000000000000002e234e92b51ab400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000e546ad000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000739c228de000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d32466a4d574a6b4d79316a595745334c54566c5a474d744f4745785a43307a5a6a4a6d596a426c5a4441784d44556966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000049e82e6bf1caebf67f3c4472c0c353361d266672000000000000000000000000000000000000000000000000000000037f9c13d7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1de7335bbc895de9c9180fba7e38c3a5ae5859de73a877b18fdadf6e84044e51",
      "signature": {
        "s": "0x1c2104e9974cc9ccce8fed1b3871b2cbf97b8197f5180cb1bb9269f0afbb3947",
        "r": "0x915a9c5be373b9bb08d722690da75b6c5eab148e385e1ef97fdce43a8d85e2f2",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x067f88372243cbe1c7bc6d3955347813f326485f774e2560cacc0155c899025b",
      "signature": {
        "s": "0x53c4d7aa2b5763b366ea5e1132f412de4c3536dd47d72799a04d20d3e7806391",
        "r": "0xf90f17f714b0752dc5ed2ec894bd3dcfb9b77625cc6d7e0dd65b81136a294812",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15025837015",
    "total": "15025837015"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15025837015",
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
            "amount": "31033796830"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "15025837"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhM2FjMWJkMy1jYWE3LTVlZGMtOGExZC0zZjJmYjBlZDAxMDUifQ==",
    "nonce": 5312,
    "balances": {
      "current": "12986654263590960",
      "previous": "12986669304453812"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x49e82e6bf1caebf67f3c4472c0c353361d266672",
    "nonce": 20,
    "balances": {
      "current": "15025837015",
      "previous": "0"
    }
  },
  "blockNumber": "10114658",
  "created": "2020-05-22T08:40:06.895Z",
  "updated": "2020-05-22T08:40:06.962Z",
  "id": "5ec78fe6005df800101bc926"
}
```
* *stageAmount*: `15025837015`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000037f9c13d7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000037f9c13d7000000000000000000000000000000000000000000000000000000037f9c13d71de7335bbc895de9c9180fba7e38c3a5ae5859de73a877b18fdadf6e84044e51915a9c5be373b9bb08d722690da75b6c5eab148e385e1ef97fdce43a8d85e2f21c2104e9974cc9ccce8fed1b3871b2cbf97b8197f5180cb1bb9269f0afbb3947000000000000000000000000000000000000000000000000000000000000001c067f88372243cbe1c7bc6d3955347813f326485f774e2560cacc0155c899025bf90f17f714b0752dc5ed2ec894bd3dcfb9b77625cc6d7e0dd65b81136a29481253c4d7aa2b5763b366ea5e1132f412de4c3536dd47d72799a04d20d3e7806391000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5662000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014c000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e234b1233c030000000000000000000000000000000000000000000000000002e234e92b51ab400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000e546ad000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000739c228de000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d32466a4d574a6b4d79316a595745334c54566c5a474d744f4745785a43307a5a6a4a6d596a426c5a4441784d44556966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000049e82e6bf1caebf67f3c4472c0c353361d266672000000000000000000000000000000000000000000000000000000037f9c13d7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1de7335bbc895de9c9180fba7e38c3a5ae5859de73a877b18fdadf6e84044e51",
      "signature": {
        "s": "0x1c2104e9974cc9ccce8fed1b3871b2cbf97b8197f5180cb1bb9269f0afbb3947",
        "r": "0x915a9c5be373b9bb08d722690da75b6c5eab148e385e1ef97fdce43a8d85e2f2",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x067f88372243cbe1c7bc6d3955347813f326485f774e2560cacc0155c899025b",
      "signature": {
        "s": "0x53c4d7aa2b5763b366ea5e1132f412de4c3536dd47d72799a04d20d3e7806391",
        "r": "0xf90f17f714b0752dc5ed2ec894bd3dcfb9b77625cc6d7e0dd65b81136a294812",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15025837015",
    "total": "15025837015"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15025837015",
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
            "amount": "31033796830"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "15025837"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhM2FjMWJkMy1jYWE3LTVlZGMtOGExZC0zZjJmYjBlZDAxMDUifQ==",
    "nonce": 5312,
    "balances": {
      "current": "12986654263590960",
      "previous": "12986669304453812"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x49e82e6bf1caebf67f3c4472c0c353361d266672",
    "nonce": 20,
    "balances": {
      "current": "15025837015",
      "previous": "0"
    }
  },
  "blockNumber": "10114658",
  "created": "2020-05-22T08:40:06.895Z",
  "updated": "2020-05-22T08:40:06.962Z",
  "id": "5ec78fe6005df800101bc926"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000037f9c13d7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `15025837015`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`