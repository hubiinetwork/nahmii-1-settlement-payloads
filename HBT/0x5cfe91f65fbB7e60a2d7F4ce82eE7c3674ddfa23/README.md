# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5cfe91f65fbB7e60a2d7F4ce82eE7c3674ddfa23`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000002b981000000000000000000000000000000000000000000000000000000000002b981000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002b981000000000000000000000000000000000000000000000000000000000002b981679c455ed409a5767e3409c42099f6769233b97c4aaff6ad7ac19bb8f3e99171e7d75037e803ee10a3e54c3cbc16f6e9732fdeec2aa9c97f162fd07995979e99527e82fcaf7aec446cf558982601e92d750b3835e21ce43a87722396fdf1ca24000000000000000000000000000000000000000000000000000000000000001bb29185a36b20023928ebc47538d22df1cf3ad33565330d071726d3adfce034eb61e51bac360b0dd001ee96efe3c6d7acab53d906fc4b72a1183c80e0c2a73bf643c38f4664a3ec938c5f954d820aaa14056c7ebd875f0c803bbfe4f26f9785bf000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56710000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000164900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1c635003f3fc000000000000000000000000000000000000000000000000002e1c635006ae2f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000b2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008fdda3ee5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a54466a4e5755304d5331695a4449354c5455314d5745744f5459344e43316d5a6a686c4d6a52695a5463785a47456966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000005cfe91f65fbb7e60a2d7f4ce82ee7c3674ddfa23000000000000000000000000000000000000000000000000000000000002b981000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x679c455ed409a5767e3409c42099f6769233b97c4aaff6ad7ac19bb8f3e99171",
      "signature": {
        "s": "0x527e82fcaf7aec446cf558982601e92d750b3835e21ce43a87722396fdf1ca24",
        "r": "0xe7d75037e803ee10a3e54c3cbc16f6e9732fdeec2aa9c97f162fd07995979e99",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb29185a36b20023928ebc47538d22df1cf3ad33565330d071726d3adfce034eb",
      "signature": {
        "s": "0x43c38f4664a3ec938c5f954d820aaa14056c7ebd875f0c803bbfe4f26f9785bf",
        "r": "0x61e51bac360b0dd001ee96efe3c6d7acab53d906fc4b72a1183c80e0c2a73bf6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "178561",
    "total": "178561"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "178561",
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
            "amount": "38618676965"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "178"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1ZTFjNWU0MS1iZDI5LTU1MWEtOTY4NC1mZjhlMjRiZTcxZGEifQ==",
    "nonce": 5705,
    "balances": {
      "current": "12979061798466556",
      "previous": "12979061798645295"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5cfe91f65fbb7e60a2d7f4ce82ee7c3674ddfa23",
    "nonce": 22,
    "balances": {
      "current": "178561",
      "previous": "0"
    }
  },
  "blockNumber": "10114673",
  "created": "2020-05-22T08:43:10.040Z",
  "updated": "2020-05-22T08:43:10.121Z",
  "id": "5ec7909e005df800101bc9a7"
}
```
* *stageAmount*: `178561`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000002b981000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002b981000000000000000000000000000000000000000000000000000000000002b981679c455ed409a5767e3409c42099f6769233b97c4aaff6ad7ac19bb8f3e99171e7d75037e803ee10a3e54c3cbc16f6e9732fdeec2aa9c97f162fd07995979e99527e82fcaf7aec446cf558982601e92d750b3835e21ce43a87722396fdf1ca24000000000000000000000000000000000000000000000000000000000000001bb29185a36b20023928ebc47538d22df1cf3ad33565330d071726d3adfce034eb61e51bac360b0dd001ee96efe3c6d7acab53d906fc4b72a1183c80e0c2a73bf643c38f4664a3ec938c5f954d820aaa14056c7ebd875f0c803bbfe4f26f9785bf000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56710000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000164900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1c635003f3fc000000000000000000000000000000000000000000000000002e1c635006ae2f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000b2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008fdda3ee5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a54466a4e5755304d5331695a4449354c5455314d5745744f5459344e43316d5a6a686c4d6a52695a5463785a47456966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000005cfe91f65fbb7e60a2d7f4ce82ee7c3674ddfa23000000000000000000000000000000000000000000000000000000000002b981000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x679c455ed409a5767e3409c42099f6769233b97c4aaff6ad7ac19bb8f3e99171",
      "signature": {
        "s": "0x527e82fcaf7aec446cf558982601e92d750b3835e21ce43a87722396fdf1ca24",
        "r": "0xe7d75037e803ee10a3e54c3cbc16f6e9732fdeec2aa9c97f162fd07995979e99",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb29185a36b20023928ebc47538d22df1cf3ad33565330d071726d3adfce034eb",
      "signature": {
        "s": "0x43c38f4664a3ec938c5f954d820aaa14056c7ebd875f0c803bbfe4f26f9785bf",
        "r": "0x61e51bac360b0dd001ee96efe3c6d7acab53d906fc4b72a1183c80e0c2a73bf6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "178561",
    "total": "178561"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "178561",
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
            "amount": "38618676965"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "178"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1ZTFjNWU0MS1iZDI5LTU1MWEtOTY4NC1mZjhlMjRiZTcxZGEifQ==",
    "nonce": 5705,
    "balances": {
      "current": "12979061798466556",
      "previous": "12979061798645295"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5cfe91f65fbb7e60a2d7f4ce82ee7c3674ddfa23",
    "nonce": 22,
    "balances": {
      "current": "178561",
      "previous": "0"
    }
  },
  "blockNumber": "10114673",
  "created": "2020-05-22T08:43:10.040Z",
  "updated": "2020-05-22T08:43:10.121Z",
  "id": "5ec7909e005df800101bc9a7"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000002b981000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `178561`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`