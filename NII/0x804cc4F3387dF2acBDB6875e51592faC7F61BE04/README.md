# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x804cc4F3387dF2acBDB6875e51592faC7F61BE04`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000017e6fe129a9dfb00000000000000000000000000000000000000000000000000167d3c38015e680000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000167d3c38015e680000000000000000000000000000000000000000000000000017e6fe129a9dfb3f72a40d816d3bd8e747c18cfb50b8e21976859be46af378301aaaf8edf3f7ef04ea062f06a200bfbd4e09da4002697f31fa0980b6a9ac766ec1921182c2ade0172eacd390482a92684546a94f643c8f7cc212fb1e6f68adfae7b84da6877d8d000000000000000000000000000000000000000000000000000000000000001b44a18910a4dab4d830afd802e6b2ba61e325adb40fe64c72436a4b0213f980e1c5ce145af7c0fd2ac5ff8f708f9d2ec785c634d8e556eb8f4a252f62143d16586f79a2da7232533bd9c76ccc4496a60b2213bd74d44683e8baea933891109d08000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000958c2c000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000092e4000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000017bc8671b1ef55b5b5580000000000000000000000000000000000000000000017bc868834ed67e2162500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000005c1da2b02650000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009c694b42efbe75d5da0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e6a526a5932566d4e7930354d546c6b4c5455354e7a6b744f47597a4f53316c4e6d49335954673459574e6c596a556966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000804cc4f3387df2acbdb6875e51592fac7f61be040000000000000000000000000000000000000000000000000017e6fe129a9dfb000000000000000000000000000000000000000000000000000169c1da993f9300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3f72a40d816d3bd8e747c18cfb50b8e21976859be46af378301aaaf8edf3f7ef",
      "signature": {
        "s": "0x172eacd390482a92684546a94f643c8f7cc212fb1e6f68adfae7b84da6877d8d",
        "r": "0x04ea062f06a200bfbd4e09da4002697f31fa0980b6a9ac766ec1921182c2ade0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x44a18910a4dab4d830afd802e6b2ba61e325adb40fe64c72436a4b0213f980e1",
      "signature": {
        "s": "0x6f79a2da7232533bd9c76ccc4496a60b2213bd74d44683e8baea933891109d08",
        "r": "0xc5ce145af7c0fd2ac5ff8f708f9d2ec785c634d8e556eb8f4a252f62143d1658",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6330147078757992",
    "total": "6727903372549627"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6330147078757992",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "2885279307093385795034"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6330147078757"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0NjRjY2VmNy05MTlkLTU5NzktOGYzOS1lNmI3YTg4YWNlYjUifQ==",
    "nonce": 37604,
    "balances": {
      "current": "112092104711774179538264",
      "previous": "112092111048251405375013"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x804cc4f3387df2acbdb6875e51592fac7f61be04",
    "nonce": 2,
    "balances": {
      "current": "6727903372549627",
      "previous": "397756293791635"
    }
  },
  "blockNumber": "9800748",
  "created": "2020-04-03T18:44:52.171Z",
  "updated": "2020-04-03T18:44:52.241Z",
  "id": "5e87842405a0b10011ed5c45"
}
```
* *stageAmount*: `6727903372549627`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000167d3c38015e680000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000167d3c38015e680000000000000000000000000000000000000000000000000017e6fe129a9dfb3f72a40d816d3bd8e747c18cfb50b8e21976859be46af378301aaaf8edf3f7ef04ea062f06a200bfbd4e09da4002697f31fa0980b6a9ac766ec1921182c2ade0172eacd390482a92684546a94f643c8f7cc212fb1e6f68adfae7b84da6877d8d000000000000000000000000000000000000000000000000000000000000001b44a18910a4dab4d830afd802e6b2ba61e325adb40fe64c72436a4b0213f980e1c5ce145af7c0fd2ac5ff8f708f9d2ec785c634d8e556eb8f4a252f62143d16586f79a2da7232533bd9c76ccc4496a60b2213bd74d44683e8baea933891109d08000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000958c2c000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000092e4000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000017bc8671b1ef55b5b5580000000000000000000000000000000000000000000017bc868834ed67e2162500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000005c1da2b02650000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009c694b42efbe75d5da0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e6a526a5932566d4e7930354d546c6b4c5455354e7a6b744f47597a4f53316c4e6d49335954673459574e6c596a556966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000804cc4f3387df2acbdb6875e51592fac7f61be040000000000000000000000000000000000000000000000000017e6fe129a9dfb000000000000000000000000000000000000000000000000000169c1da993f9300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3f72a40d816d3bd8e747c18cfb50b8e21976859be46af378301aaaf8edf3f7ef",
      "signature": {
        "s": "0x172eacd390482a92684546a94f643c8f7cc212fb1e6f68adfae7b84da6877d8d",
        "r": "0x04ea062f06a200bfbd4e09da4002697f31fa0980b6a9ac766ec1921182c2ade0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x44a18910a4dab4d830afd802e6b2ba61e325adb40fe64c72436a4b0213f980e1",
      "signature": {
        "s": "0x6f79a2da7232533bd9c76ccc4496a60b2213bd74d44683e8baea933891109d08",
        "r": "0xc5ce145af7c0fd2ac5ff8f708f9d2ec785c634d8e556eb8f4a252f62143d1658",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6330147078757992",
    "total": "6727903372549627"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6330147078757992",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "2885279307093385795034"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6330147078757"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0NjRjY2VmNy05MTlkLTU5NzktOGYzOS1lNmI3YTg4YWNlYjUifQ==",
    "nonce": 37604,
    "balances": {
      "current": "112092104711774179538264",
      "previous": "112092111048251405375013"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x804cc4f3387df2acbdb6875e51592fac7f61be04",
    "nonce": 2,
    "balances": {
      "current": "6727903372549627",
      "previous": "397756293791635"
    }
  },
  "blockNumber": "9800748",
  "created": "2020-04-03T18:44:52.171Z",
  "updated": "2020-04-03T18:44:52.241Z",
  "id": "5e87842405a0b10011ed5c45"
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
0x0f200f9b0000000000000000000000000000000000000000000000000017e6fe129a9dfb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6727903372549627`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`