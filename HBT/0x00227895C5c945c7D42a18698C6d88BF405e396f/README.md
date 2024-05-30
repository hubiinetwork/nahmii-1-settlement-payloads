# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x00227895C5c945c7D42a18698C6d88BF405e396f`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000003f1158d0000000000000000000000000000000000000000000000000000000003f1158d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000003f1158d0000000000000000000000000000000000000000000000000000000003f1158d58c26046acad8690b6784509ef7f2187a82fa0931fdff47578e4062d5e90262f2d13d85c2242bf8f38dfe6c9a218029700708503d1073f9e21937f987b9aadc26fbe15afaaabe28077f5d27bb463f8ca72dad0a067efde17e2bbe1dafa5f64af000000000000000000000000000000000000000000000000000000000000001bd083385bdb9080a240200fed2b36f913bbda7b714e9f63a85c464d47e4ffdabe9807eed52103e9c6ec3b5870b1d7acfb193d057519ac36919a343eb3f2263df96cf60dfe9ae0b8181a20a1a497d36744491eec7faf573bd2599197cedfb28344000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a0900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17213227f41e000000000000000000000000000000000000000000000000002e1721361a0bfe00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000010253000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a561d3547000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6959575a6b4e475a684d7930354d5441314c54553459324d7459546330596930784e4463344e6d4a6b4d544e6c596a416966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000000227895c5c945c7d42a18698c6d88bf405e396f0000000000000000000000000000000000000000000000000000000003f1158d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x58c26046acad8690b6784509ef7f2187a82fa0931fdff47578e4062d5e90262f",
      "signature": {
        "s": "0x6fbe15afaaabe28077f5d27bb463f8ca72dad0a067efde17e2bbe1dafa5f64af",
        "r": "0x2d13d85c2242bf8f38dfe6c9a218029700708503d1073f9e21937f987b9aadc2",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd083385bdb9080a240200fed2b36f913bbda7b714e9f63a85c464d47e4ffdabe",
      "signature": {
        "s": "0x6cf60dfe9ae0b8181a20a1a497d36744491eec7faf573bd2599197cedfb28344",
        "r": "0x9807eed52103e9c6ec3b5870b1d7acfb193d057519ac36919a343eb3f2263df9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "66131341",
    "total": "66131341"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "66131341",
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
            "amount": "44394427719"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "66131"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiYWZkNGZhMy05MTA1LTU4Y2MtYTc0Yi0xNDc4NmJkMTNlYjAifQ==",
    "nonce": 6665,
    "balances": {
      "current": "12973280271528990",
      "previous": "12973280337726462"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x00227895c5c945c7d42a18698c6d88bf405e396f",
    "nonce": 22,
    "balances": {
      "current": "66131341",
      "previous": "0"
    }
  },
  "blockNumber": "10114712",
  "created": "2020-05-22T08:50:53.047Z",
  "updated": "2020-05-22T08:50:53.132Z",
  "id": "5ec7926db0c6090011d5b177"
}
```
* *stageAmount*: `66131341`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000003f1158d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000003f1158d0000000000000000000000000000000000000000000000000000000003f1158d58c26046acad8690b6784509ef7f2187a82fa0931fdff47578e4062d5e90262f2d13d85c2242bf8f38dfe6c9a218029700708503d1073f9e21937f987b9aadc26fbe15afaaabe28077f5d27bb463f8ca72dad0a067efde17e2bbe1dafa5f64af000000000000000000000000000000000000000000000000000000000000001bd083385bdb9080a240200fed2b36f913bbda7b714e9f63a85c464d47e4ffdabe9807eed52103e9c6ec3b5870b1d7acfb193d057519ac36919a343eb3f2263df96cf60dfe9ae0b8181a20a1a497d36744491eec7faf573bd2599197cedfb28344000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a0900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17213227f41e000000000000000000000000000000000000000000000000002e1721361a0bfe00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000010253000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a561d3547000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6959575a6b4e475a684d7930354d5441314c54553459324d7459546330596930784e4463344e6d4a6b4d544e6c596a416966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000000227895c5c945c7d42a18698c6d88bf405e396f0000000000000000000000000000000000000000000000000000000003f1158d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x58c26046acad8690b6784509ef7f2187a82fa0931fdff47578e4062d5e90262f",
      "signature": {
        "s": "0x6fbe15afaaabe28077f5d27bb463f8ca72dad0a067efde17e2bbe1dafa5f64af",
        "r": "0x2d13d85c2242bf8f38dfe6c9a218029700708503d1073f9e21937f987b9aadc2",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd083385bdb9080a240200fed2b36f913bbda7b714e9f63a85c464d47e4ffdabe",
      "signature": {
        "s": "0x6cf60dfe9ae0b8181a20a1a497d36744491eec7faf573bd2599197cedfb28344",
        "r": "0x9807eed52103e9c6ec3b5870b1d7acfb193d057519ac36919a343eb3f2263df9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "66131341",
    "total": "66131341"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "66131341",
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
            "amount": "44394427719"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "66131"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiYWZkNGZhMy05MTA1LTU4Y2MtYTc0Yi0xNDc4NmJkMTNlYjAifQ==",
    "nonce": 6665,
    "balances": {
      "current": "12973280271528990",
      "previous": "12973280337726462"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x00227895c5c945c7d42a18698c6d88bf405e396f",
    "nonce": 22,
    "balances": {
      "current": "66131341",
      "previous": "0"
    }
  },
  "blockNumber": "10114712",
  "created": "2020-05-22T08:50:53.047Z",
  "updated": "2020-05-22T08:50:53.132Z",
  "id": "5ec7926db0c6090011d5b177"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000003f1158d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `66131341`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`