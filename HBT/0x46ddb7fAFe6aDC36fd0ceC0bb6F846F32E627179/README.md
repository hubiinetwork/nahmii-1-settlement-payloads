# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x46ddb7fAFe6aDC36fd0ceC0bb6F846F32E627179`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000557e0ec000000000000000000000000000000000000000000000000000000000557e0ec000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000557e0ec000000000000000000000000000000000000000000000000000000000557e0ec4c74a3a0bddb10512163fdae3d746148445f49efd9fb54592c4dcc47d1a7bb4aa83d0b74219d94f34e21ab7f61ac21c30a356870525b22fa20f94a3c1e76887c5b704cc10a4ecc314d7f632928d7b5779586c84aea05df8cf3281c0392bf98ce000000000000000000000000000000000000000000000000000000000000001be37e83223ac2b029b7e3b374c662a532d9ed295f281f2eec792428212e6331f26672a4142dfa76d5c1431ce4605dcf5f9c07a03925c37c3f18e2da7bc3b052857aa5468d0e4100feab3bbe57e2d4d83f91f50f75a863c86084628d4d3815ddd4000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56c500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ecf00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0aeb2c1c0e7a000000000000000000000000000000000000000000000000002e0aeb31754d9300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000015e2d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d75939efe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c596a686a4d57557a4e5330774e6a4e6b4c5455354e6a637459545a685953316c4d6a6c6b59544a6b4e3255344d44556966513d3d000000000000000000000000000000000000000000000000000000000000000700000000000000000000000046ddb7fafe6adc36fd0cec0bb6f846f32e627179000000000000000000000000000000000000000000000000000000000557e0ec000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4c74a3a0bddb10512163fdae3d746148445f49efd9fb54592c4dcc47d1a7bb4a",
      "signature": {
        "s": "0x5b704cc10a4ecc314d7f632928d7b5779586c84aea05df8cf3281c0392bf98ce",
        "r": "0xa83d0b74219d94f34e21ab7f61ac21c30a356870525b22fa20f94a3c1e76887c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe37e83223ac2b029b7e3b374c662a532d9ed295f281f2eec792428212e6331f2",
      "signature": {
        "s": "0x7aa5468d0e4100feab3bbe57e2d4d83f91f50f75a863c86084628d4d3815ddd4",
        "r": "0x6672a4142dfa76d5c1431ce4605dcf5f9c07a03925c37c3f18e2da7bc3b05285",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "89645292",
    "total": "89645292"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "89645292",
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
            "amount": "57807183614"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "89645"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlYjhjMWUzNS0wNjNkLTU5NjctYTZhYS1lMjlkYTJkN2U4MDUifQ==",
    "nonce": 7887,
    "balances": {
      "current": "12959854102318714",
      "previous": "12959854192053651"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x46ddb7fafe6adc36fd0cec0bb6f846f32e627179",
    "nonce": 7,
    "balances": {
      "current": "89645292",
      "previous": "0"
    }
  },
  "blockNumber": "10114757",
  "created": "2020-05-22T09:00:19.876Z",
  "updated": "2020-05-22T09:00:20.008Z",
  "id": "5ec794a3e5756b00111b8972"
}
```
* *stageAmount*: `89645292`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000557e0ec000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000557e0ec000000000000000000000000000000000000000000000000000000000557e0ec4c74a3a0bddb10512163fdae3d746148445f49efd9fb54592c4dcc47d1a7bb4aa83d0b74219d94f34e21ab7f61ac21c30a356870525b22fa20f94a3c1e76887c5b704cc10a4ecc314d7f632928d7b5779586c84aea05df8cf3281c0392bf98ce000000000000000000000000000000000000000000000000000000000000001be37e83223ac2b029b7e3b374c662a532d9ed295f281f2eec792428212e6331f26672a4142dfa76d5c1431ce4605dcf5f9c07a03925c37c3f18e2da7bc3b052857aa5468d0e4100feab3bbe57e2d4d83f91f50f75a863c86084628d4d3815ddd4000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56c500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ecf00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0aeb2c1c0e7a000000000000000000000000000000000000000000000000002e0aeb31754d9300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000015e2d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d75939efe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c596a686a4d57557a4e5330774e6a4e6b4c5455354e6a637459545a685953316c4d6a6c6b59544a6b4e3255344d44556966513d3d000000000000000000000000000000000000000000000000000000000000000700000000000000000000000046ddb7fafe6adc36fd0cec0bb6f846f32e627179000000000000000000000000000000000000000000000000000000000557e0ec000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4c74a3a0bddb10512163fdae3d746148445f49efd9fb54592c4dcc47d1a7bb4a",
      "signature": {
        "s": "0x5b704cc10a4ecc314d7f632928d7b5779586c84aea05df8cf3281c0392bf98ce",
        "r": "0xa83d0b74219d94f34e21ab7f61ac21c30a356870525b22fa20f94a3c1e76887c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe37e83223ac2b029b7e3b374c662a532d9ed295f281f2eec792428212e6331f2",
      "signature": {
        "s": "0x7aa5468d0e4100feab3bbe57e2d4d83f91f50f75a863c86084628d4d3815ddd4",
        "r": "0x6672a4142dfa76d5c1431ce4605dcf5f9c07a03925c37c3f18e2da7bc3b05285",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "89645292",
    "total": "89645292"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "89645292",
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
            "amount": "57807183614"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "89645"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlYjhjMWUzNS0wNjNkLTU5NjctYTZhYS1lMjlkYTJkN2U4MDUifQ==",
    "nonce": 7887,
    "balances": {
      "current": "12959854102318714",
      "previous": "12959854192053651"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x46ddb7fafe6adc36fd0cec0bb6f846f32e627179",
    "nonce": 7,
    "balances": {
      "current": "89645292",
      "previous": "0"
    }
  },
  "blockNumber": "10114757",
  "created": "2020-05-22T09:00:19.876Z",
  "updated": "2020-05-22T09:00:20.008Z",
  "id": "5ec794a3e5756b00111b8972"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000557e0ec000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `89645292`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`