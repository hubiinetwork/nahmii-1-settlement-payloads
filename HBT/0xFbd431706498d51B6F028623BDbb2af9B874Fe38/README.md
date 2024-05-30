# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xFbd431706498d51B6F028623BDbb2af9B874Fe38`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000001550f96c619879000000000000000000000000000000000000000000000000000000018fba9879000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000018fba9879000000000000000000000000000000000000000000000000000000018fba9879104c92d958d928ed3f8d2ca0a490b8bffc7356e00f31344b3b8b75c3448999b7b15319a182be0fd624a0089fa718c76854b8baed6d64d61d8092d7739568f70170818c0cb3396934b6de55bbf6ce18d51d0cbaf7ad39ccd61bd2a875c2474e86000000000000000000000000000000000000000000000000000000000000001c0fafc241330e1c066f5f7b80df3f4c6db7690d3c88f56d31c3cb64b51675c59edb46e170ad9bbbc63a0b59ea726cbefef7e7402b655cdcf72b59040b3453dea1040580c127980765aee2f4442c8a101d2076edd6f4280402bb22edde7a9e7c28000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5661000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014b100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e23f4c23ad290000000000000000000000000000000000000000000000000002e23f6525bbfaa00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000006654a1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000070e5c9f4c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e7a4d354d7a5668597930335a5441794c5455344f4755744f5745304f4330344e6d466c4e57513159574a6d4d57496966513d3d000000000000000000000000000000000000000000000000000000000000001b000000000000000000000000fbd431706498d51b6f028623bdbb2af9b874fe38000000000000000000000000000000000000000000000000001550f96c619879000000000000000000000000000000000000000000000000001550f7dca7000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x104c92d958d928ed3f8d2ca0a490b8bffc7356e00f31344b3b8b75c3448999b7",
      "signature": {
        "s": "0x70818c0cb3396934b6de55bbf6ce18d51d0cbaf7ad39ccd61bd2a875c2474e86",
        "r": "0xb15319a182be0fd624a0089fa718c76854b8baed6d64d61d8092d7739568f701",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0fafc241330e1c066f5f7b80df3f4c6db7690d3c88f56d31c3cb64b51675c59e",
      "signature": {
        "s": "0x040580c127980765aee2f4442c8a101d2076edd6f4280402bb22edde7a9e7c28",
        "r": "0xdb46e170ad9bbbc63a0b59ea726cbefef7e7402b655cdcf72b59040b3453dea1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6706337913",
    "total": "6706337913"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6706337913",
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
            "amount": "30305722188"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6706337"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzNzM5MzVhYy03ZTAyLTU4OGUtOWE0OC04NmFlNWQ1YWJmMWIifQ==",
    "nonce": 5297,
    "balances": {
      "current": "12987383066317456",
      "previous": "12987389779361706"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfbd431706498d51b6f028623bdbb2af9b874fe38",
    "nonce": 27,
    "balances": {
      "current": "6000006706337913",
      "previous": "6000000000000000"
    }
  },
  "blockNumber": "10114657",
  "created": "2020-05-22T08:39:56.375Z",
  "updated": "2020-05-22T08:39:56.863Z",
  "id": "5ec78fdce5756b00111b863d"
}
```
* *stageAmount*: `6000006706337913`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000018fba9879000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000018fba9879000000000000000000000000000000000000000000000000000000018fba9879104c92d958d928ed3f8d2ca0a490b8bffc7356e00f31344b3b8b75c3448999b7b15319a182be0fd624a0089fa718c76854b8baed6d64d61d8092d7739568f70170818c0cb3396934b6de55bbf6ce18d51d0cbaf7ad39ccd61bd2a875c2474e86000000000000000000000000000000000000000000000000000000000000001c0fafc241330e1c066f5f7b80df3f4c6db7690d3c88f56d31c3cb64b51675c59edb46e170ad9bbbc63a0b59ea726cbefef7e7402b655cdcf72b59040b3453dea1040580c127980765aee2f4442c8a101d2076edd6f4280402bb22edde7a9e7c28000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5661000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014b100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e23f4c23ad290000000000000000000000000000000000000000000000000002e23f6525bbfaa00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000006654a1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000070e5c9f4c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e7a4d354d7a5668597930335a5441794c5455344f4755744f5745304f4330344e6d466c4e57513159574a6d4d57496966513d3d000000000000000000000000000000000000000000000000000000000000001b000000000000000000000000fbd431706498d51b6f028623bdbb2af9b874fe38000000000000000000000000000000000000000000000000001550f96c619879000000000000000000000000000000000000000000000000001550f7dca7000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x104c92d958d928ed3f8d2ca0a490b8bffc7356e00f31344b3b8b75c3448999b7",
      "signature": {
        "s": "0x70818c0cb3396934b6de55bbf6ce18d51d0cbaf7ad39ccd61bd2a875c2474e86",
        "r": "0xb15319a182be0fd624a0089fa718c76854b8baed6d64d61d8092d7739568f701",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0fafc241330e1c066f5f7b80df3f4c6db7690d3c88f56d31c3cb64b51675c59e",
      "signature": {
        "s": "0x040580c127980765aee2f4442c8a101d2076edd6f4280402bb22edde7a9e7c28",
        "r": "0xdb46e170ad9bbbc63a0b59ea726cbefef7e7402b655cdcf72b59040b3453dea1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6706337913",
    "total": "6706337913"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6706337913",
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
            "amount": "30305722188"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6706337"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzNzM5MzVhYy03ZTAyLTU4OGUtOWE0OC04NmFlNWQ1YWJmMWIifQ==",
    "nonce": 5297,
    "balances": {
      "current": "12987383066317456",
      "previous": "12987389779361706"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfbd431706498d51b6f028623bdbb2af9b874fe38",
    "nonce": 27,
    "balances": {
      "current": "6000006706337913",
      "previous": "6000000000000000"
    }
  },
  "blockNumber": "10114657",
  "created": "2020-05-22T08:39:56.375Z",
  "updated": "2020-05-22T08:39:56.863Z",
  "id": "5ec78fdce5756b00111b863d"
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
0x0f200f9b000000000000000000000000000000000000000000000000001550f96c619879000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6000006706337913`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`