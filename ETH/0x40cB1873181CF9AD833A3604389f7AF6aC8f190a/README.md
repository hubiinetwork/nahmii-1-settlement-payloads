# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x40cB1873181CF9AD833A3604389f7AF6aC8f190a`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000018fa00000000000000000000000000000000000000000000000000000000000018fa000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000018fa00000000000000000000000000000000000000000000000000000000000018fa07411a02d853b0d916bb61dc34b3c91cecbd2db9c40c0c5d9f378217aa5ba88c6349f69b9c0602f780583f6df72b52d1ccbc57316aae718a70ba19e68cfb19a6841b9f8c96de5391e29e23770eb7dce021a48ff10b9aa2fbdcbf72a69bba9f024000000000000000000000000000000000000000000000000000000000000001b92f99f4e9a896e7c67eb8a76180d0d85a06871394569fe8e3e079006c6331e43d62e584f18c02ae2321f0ebfed1fbcdb2a1c81c9de3491a0c12997502dcbaeac1bd69b52051cf1ee457d2f9d6884bd41f0c803bce0f80edba783ed07eb7a6047000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55b90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000007d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d32ae671000000000000000000000000000000000000000000000000002386f2d32c767700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000660000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000659fa00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949795a575a6b4d5755344d43316b4d6a56694c5456684f544174596a597a4f53316c4d7a46695a4463304d5452684e32456966513d3d000000000000000000000000000000000000000000000000000000000000000f00000000000000000000000040cb1873181cf9ad833a3604389f7af6ac8f190a0000000000000000000000000000000000000000000000000000000000018fa0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7411a02d853b0d916bb61dc34b3c91cecbd2db9c40c0c5d9f378217aa5ba88c6",
      "signature": {
        "s": "0x41b9f8c96de5391e29e23770eb7dce021a48ff10b9aa2fbdcbf72a69bba9f024",
        "r": "0x349f69b9c0602f780583f6df72b52d1ccbc57316aae718a70ba19e68cfb19a68",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x92f99f4e9a896e7c67eb8a76180d0d85a06871394569fe8e3e079006c6331e43",
      "signature": {
        "s": "0x1bd69b52051cf1ee457d2f9d6884bd41f0c803bce0f80edba783ed07eb7a6047",
        "r": "0xd62e584f18c02ae2321f0ebfed1fbcdb2a1c81c9de3491a0c12997502dcbaeac",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "102304",
    "total": "102304"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "102304",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "416250"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "102"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyZWZkMWU4MC1kMjViLTVhOTAtYjYzOS1lMzFiZDc0MTRhN2EifQ==",
    "nonce": 125,
    "balances": {
      "current": "10000001667884657",
      "previous": "10000001667987063"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x40cb1873181cf9ad833a3604389f7af6ac8f190a",
    "nonce": 15,
    "balances": {
      "current": "102304",
      "previous": "0"
    }
  },
  "blockNumber": "10114489",
  "created": "2020-05-22T07:59:43.989Z",
  "updated": "2020-05-22T07:59:44.054Z",
  "id": "5ec7866f005df800101bc239"
}
```
* *stageAmount*: `102304`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000018fa000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000018fa00000000000000000000000000000000000000000000000000000000000018fa07411a02d853b0d916bb61dc34b3c91cecbd2db9c40c0c5d9f378217aa5ba88c6349f69b9c0602f780583f6df72b52d1ccbc57316aae718a70ba19e68cfb19a6841b9f8c96de5391e29e23770eb7dce021a48ff10b9aa2fbdcbf72a69bba9f024000000000000000000000000000000000000000000000000000000000000001b92f99f4e9a896e7c67eb8a76180d0d85a06871394569fe8e3e079006c6331e43d62e584f18c02ae2321f0ebfed1fbcdb2a1c81c9de3491a0c12997502dcbaeac1bd69b52051cf1ee457d2f9d6884bd41f0c803bce0f80edba783ed07eb7a6047000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55b90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000007d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d32ae671000000000000000000000000000000000000000000000000002386f2d32c767700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000660000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000659fa00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949795a575a6b4d5755344d43316b4d6a56694c5456684f544174596a597a4f53316c4d7a46695a4463304d5452684e32456966513d3d000000000000000000000000000000000000000000000000000000000000000f00000000000000000000000040cb1873181cf9ad833a3604389f7af6ac8f190a0000000000000000000000000000000000000000000000000000000000018fa0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7411a02d853b0d916bb61dc34b3c91cecbd2db9c40c0c5d9f378217aa5ba88c6",
      "signature": {
        "s": "0x41b9f8c96de5391e29e23770eb7dce021a48ff10b9aa2fbdcbf72a69bba9f024",
        "r": "0x349f69b9c0602f780583f6df72b52d1ccbc57316aae718a70ba19e68cfb19a68",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x92f99f4e9a896e7c67eb8a76180d0d85a06871394569fe8e3e079006c6331e43",
      "signature": {
        "s": "0x1bd69b52051cf1ee457d2f9d6884bd41f0c803bce0f80edba783ed07eb7a6047",
        "r": "0xd62e584f18c02ae2321f0ebfed1fbcdb2a1c81c9de3491a0c12997502dcbaeac",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "102304",
    "total": "102304"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "102304",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "416250"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "102"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyZWZkMWU4MC1kMjViLTVhOTAtYjYzOS1lMzFiZDc0MTRhN2EifQ==",
    "nonce": 125,
    "balances": {
      "current": "10000001667884657",
      "previous": "10000001667987063"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x40cb1873181cf9ad833a3604389f7af6ac8f190a",
    "nonce": 15,
    "balances": {
      "current": "102304",
      "previous": "0"
    }
  },
  "blockNumber": "10114489",
  "created": "2020-05-22T07:59:43.989Z",
  "updated": "2020-05-22T07:59:44.054Z",
  "id": "5ec7866f005df800101bc239"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b0000000000000000000000000000000000000000000000000000000000018fa00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `102304`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``