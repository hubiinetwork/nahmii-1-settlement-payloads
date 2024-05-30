# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xF74151787031d1F691D6CC234CE55b5D7FaA9e5D`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000021360000000000000000000000000000000000000000000000000000000000002136000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000021360000000000000000000000000000000000000000000000000000000000002136d1b6df6a6ba2eea9b9b47c57a23bdf0a5e35f9d6235d83f2716c080a8010a793755207a87e55239108c2666d6c2c674706591da73482974e224f32bc3ad143640ccc741f6ef92f3d60a0cadbf6439215c74f4385aaef1ba2c5493dbb28439ca4000000000000000000000000000000000000000000000000000000000000001b72b65c6285d7f042241620398bee48c38f9190911d3ce2c92e2184510079eb0559c6bf229261ef1746ec0bb126d46344f3f4c262d82057972c7122116a3174c3109265eb1247271215dd7f095b0316c6526c7f4e3f59cdda355e355213dfb65e000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f3000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008a600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc6b5d0a000000000000000000000000000000000000000000000000002386f2bc6b7e4800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c28d400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949305a57517a595751314d69316d4d446b784c5455304d574d744f444a6c4e4330774f4449785a54417a596a45334d6a676966513d3d000000000000000000000000000000000000000000000000000000000000000f000000000000000000000000f74151787031d1f691d6cc234ce55b5d7faa9e5d0000000000000000000000000000000000000000000000000000000000002136000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd1b6df6a6ba2eea9b9b47c57a23bdf0a5e35f9d6235d83f2716c080a8010a793",
      "signature": {
        "s": "0x0ccc741f6ef92f3d60a0cadbf6439215c74f4385aaef1ba2c5493dbb28439ca4",
        "r": "0x755207a87e55239108c2666d6c2c674706591da73482974e224f32bc3ad14364",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x72b65c6285d7f042241620398bee48c38f9190911d3ce2c92e2184510079eb05",
      "signature": {
        "s": "0x109265eb1247271215dd7f095b0316c6526c7f4e3f59cdda355e355213dfb65e",
        "r": "0x59c6bf229261ef1746ec0bb126d46344f3f4c262d82057972c7122116a3174c3",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "8502",
    "total": "8502"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8502",
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
            "amount": "796884"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "8"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0ZWQzYWQ1Mi1mMDkxLTU0MWMtODJlNC0wODIxZTAzYjE3MjgifQ==",
    "nonce": 2214,
    "balances": {
      "current": "10000001286233354",
      "previous": "10000001286241864"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf74151787031d1f691d6cc234ce55b5d7faa9e5d",
    "nonce": 15,
    "balances": {
      "current": "8502",
      "previous": "0"
    }
  },
  "blockNumber": "10114547",
  "created": "2020-05-22T08:15:05.304Z",
  "updated": "2020-05-22T08:15:05.374Z",
  "id": "5ec78a09e5756b00111b8243"
}
```
* *stageAmount*: `8502`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000002136000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000021360000000000000000000000000000000000000000000000000000000000002136d1b6df6a6ba2eea9b9b47c57a23bdf0a5e35f9d6235d83f2716c080a8010a793755207a87e55239108c2666d6c2c674706591da73482974e224f32bc3ad143640ccc741f6ef92f3d60a0cadbf6439215c74f4385aaef1ba2c5493dbb28439ca4000000000000000000000000000000000000000000000000000000000000001b72b65c6285d7f042241620398bee48c38f9190911d3ce2c92e2184510079eb0559c6bf229261ef1746ec0bb126d46344f3f4c262d82057972c7122116a3174c3109265eb1247271215dd7f095b0316c6526c7f4e3f59cdda355e355213dfb65e000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f3000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008a600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc6b5d0a000000000000000000000000000000000000000000000000002386f2bc6b7e4800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c28d400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949305a57517a595751314d69316d4d446b784c5455304d574d744f444a6c4e4330774f4449785a54417a596a45334d6a676966513d3d000000000000000000000000000000000000000000000000000000000000000f000000000000000000000000f74151787031d1f691d6cc234ce55b5d7faa9e5d0000000000000000000000000000000000000000000000000000000000002136000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd1b6df6a6ba2eea9b9b47c57a23bdf0a5e35f9d6235d83f2716c080a8010a793",
      "signature": {
        "s": "0x0ccc741f6ef92f3d60a0cadbf6439215c74f4385aaef1ba2c5493dbb28439ca4",
        "r": "0x755207a87e55239108c2666d6c2c674706591da73482974e224f32bc3ad14364",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x72b65c6285d7f042241620398bee48c38f9190911d3ce2c92e2184510079eb05",
      "signature": {
        "s": "0x109265eb1247271215dd7f095b0316c6526c7f4e3f59cdda355e355213dfb65e",
        "r": "0x59c6bf229261ef1746ec0bb126d46344f3f4c262d82057972c7122116a3174c3",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "8502",
    "total": "8502"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8502",
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
            "amount": "796884"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "8"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0ZWQzYWQ1Mi1mMDkxLTU0MWMtODJlNC0wODIxZTAzYjE3MjgifQ==",
    "nonce": 2214,
    "balances": {
      "current": "10000001286233354",
      "previous": "10000001286241864"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf74151787031d1f691d6cc234ce55b5d7faa9e5d",
    "nonce": 15,
    "balances": {
      "current": "8502",
      "previous": "0"
    }
  },
  "blockNumber": "10114547",
  "created": "2020-05-22T08:15:05.304Z",
  "updated": "2020-05-22T08:15:05.374Z",
  "id": "5ec78a09e5756b00111b8243"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000021360000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `8502`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``