# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xD3B23dA91B9061a1c1Cf1c45855466F95A25Fb3B`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000bef411c2e0000000000000000000000000000000000000000000000000000000bef411c2e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000bef411c2e0000000000000000000000000000000000000000000000000000000bef411c2e73523c335e5727eb12783864a63b7d50a8362dc502e8558f318ca8f4f7200c45e05606c849c45c3674e325bb3ca3e73edeb9261d9e46eb54270a26b17571c033032396f958cfff4558a8dbbadf481a55c6eabaaddc3e5006915ad1e25c5a8b21000000000000000000000000000000000000000000000000000000000000001cda3bbad8db01d9081f3a95ccf7751ee483785a573778171c5ef6e9dc18489a625e2b4e9252c58f2af9ef1a449c9f15560004a4905773bf7d368100aaa20193924eb466b97d97a66e188ee12b43ee1e4408578e38163fff9b69b64c35eacc0bbc000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56610000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000148a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e2ee62b4ef2c2000000000000000000000000000000000000000000000000002e2ef21d9e341500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000030e2525000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000441eacbd8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694930597a4e69596a5a6d595331694d6a63794c545578596d5974596d4e6d5969316a59544d795a5467795a4745325a57456966513d3d000000000000000000000000000000000000000000000000000000000000001a000000000000000000000000d3b23da91b9061a1c1cf1c45855466f95a25fb3b0000000000000000000000000000000000000000000000000000000bef411c2e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x73523c335e5727eb12783864a63b7d50a8362dc502e8558f318ca8f4f7200c45",
      "signature": {
        "s": "0x032396f958cfff4558a8dbbadf481a55c6eabaaddc3e5006915ad1e25c5a8b21",
        "r": "0xe05606c849c45c3674e325bb3ca3e73edeb9261d9e46eb54270a26b17571c033",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xda3bbad8db01d9081f3a95ccf7751ee483785a573778171c5ef6e9dc18489a62",
      "signature": {
        "s": "0x4eb466b97d97a66e188ee12b43ee1e4408578e38163fff9b69b64c35eacc0bbc",
        "r": "0x5e2b4e9252c58f2af9ef1a449c9f15560004a4905773bf7d368100aaa2019392",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "51258661934",
    "total": "51258661934"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "51258661934",
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
            "amount": "18285775832"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "51258661"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0YzNiYjZmYS1iMjcyLTUxYmYtYmNmYi1jYTMyZTgyZGE2ZWEifQ==",
    "nonce": 5258,
    "balances": {
      "current": "12999415032640194",
      "previous": "12999466342560789"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd3b23da91b9061a1c1cf1c45855466f95a25fb3b",
    "nonce": 26,
    "balances": {
      "current": "51258661934",
      "previous": "0"
    }
  },
  "blockNumber": "10114657",
  "created": "2020-05-22T08:39:44.368Z",
  "updated": "2020-05-22T08:39:45.442Z",
  "id": "5ec78fd0005df800101bc914"
}
```
* *stageAmount*: `51258661934`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000bef411c2e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000bef411c2e0000000000000000000000000000000000000000000000000000000bef411c2e73523c335e5727eb12783864a63b7d50a8362dc502e8558f318ca8f4f7200c45e05606c849c45c3674e325bb3ca3e73edeb9261d9e46eb54270a26b17571c033032396f958cfff4558a8dbbadf481a55c6eabaaddc3e5006915ad1e25c5a8b21000000000000000000000000000000000000000000000000000000000000001cda3bbad8db01d9081f3a95ccf7751ee483785a573778171c5ef6e9dc18489a625e2b4e9252c58f2af9ef1a449c9f15560004a4905773bf7d368100aaa20193924eb466b97d97a66e188ee12b43ee1e4408578e38163fff9b69b64c35eacc0bbc000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56610000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000148a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e2ee62b4ef2c2000000000000000000000000000000000000000000000000002e2ef21d9e341500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000030e2525000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000441eacbd8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694930597a4e69596a5a6d595331694d6a63794c545578596d5974596d4e6d5969316a59544d795a5467795a4745325a57456966513d3d000000000000000000000000000000000000000000000000000000000000001a000000000000000000000000d3b23da91b9061a1c1cf1c45855466f95a25fb3b0000000000000000000000000000000000000000000000000000000bef411c2e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x73523c335e5727eb12783864a63b7d50a8362dc502e8558f318ca8f4f7200c45",
      "signature": {
        "s": "0x032396f958cfff4558a8dbbadf481a55c6eabaaddc3e5006915ad1e25c5a8b21",
        "r": "0xe05606c849c45c3674e325bb3ca3e73edeb9261d9e46eb54270a26b17571c033",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xda3bbad8db01d9081f3a95ccf7751ee483785a573778171c5ef6e9dc18489a62",
      "signature": {
        "s": "0x4eb466b97d97a66e188ee12b43ee1e4408578e38163fff9b69b64c35eacc0bbc",
        "r": "0x5e2b4e9252c58f2af9ef1a449c9f15560004a4905773bf7d368100aaa2019392",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "51258661934",
    "total": "51258661934"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "51258661934",
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
            "amount": "18285775832"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "51258661"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0YzNiYjZmYS1iMjcyLTUxYmYtYmNmYi1jYTMyZTgyZGE2ZWEifQ==",
    "nonce": 5258,
    "balances": {
      "current": "12999415032640194",
      "previous": "12999466342560789"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd3b23da91b9061a1c1cf1c45855466f95a25fb3b",
    "nonce": 26,
    "balances": {
      "current": "51258661934",
      "previous": "0"
    }
  },
  "blockNumber": "10114657",
  "created": "2020-05-22T08:39:44.368Z",
  "updated": "2020-05-22T08:39:45.442Z",
  "id": "5ec78fd0005df800101bc914"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000bef411c2e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `51258661934`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`