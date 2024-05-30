# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x812DED039dB8026dF8b86B1f43991CD3CD51E237`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000003e56c000000000000000000000000000000000000000000000000000000000003e56c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000003e56c000000000000000000000000000000000000000000000000000000000003e56c0f445c0541927cdcfa779f9a7cdb7a18aaacf1957d4547c2478bde58084481234e2bebbe02fb8e0ab584ca2e4d36547e74e95bb5f0100e26c543aaf10813a7640c77b45d3c5948148c935bb71f5660423e24694e12fd0de370c03b937f2de342000000000000000000000000000000000000000000000000000000000000001b27cca521685250d69cdbcfcc96cf1650c12fa694bb922161689a70b5399d3b326cc36e8d64cce53aba4ae23061311e79356188c00e291085aff1bbbb1f36f7bd25a39df47aa2a4578d9a153be05e3cda28afff4e027f7f08b426dd27775ef65f000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55bc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000aa00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d157fea3000000000000000000000000000000000000000000000000002386f2d15be50e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000ff00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000006d15200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d6d4d344e546777595330795a4467794c5455344f4459744f4751774e433030596a4e694d7a59345954466b4e7a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000018000000000000000000000000812ded039db8026df8b86b1f43991cd3cd51e237000000000000000000000000000000000000000000000000000000000003e56c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0f445c0541927cdcfa779f9a7cdb7a18aaacf1957d4547c2478bde5808448123",
      "signature": {
        "s": "0x0c77b45d3c5948148c935bb71f5660423e24694e12fd0de370c03b937f2de342",
        "r": "0x4e2bebbe02fb8e0ab584ca2e4d36547e74e95bb5f0100e26c543aaf10813a764",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x27cca521685250d69cdbcfcc96cf1650c12fa694bb922161689a70b5399d3b32",
      "signature": {
        "s": "0x25a39df47aa2a4578d9a153be05e3cda28afff4e027f7f08b426dd27775ef65f",
        "r": "0x6cc36e8d64cce53aba4ae23061311e79356188c00e291085aff1bbbb1f36f7bd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "255340",
    "total": "255340"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "255340",
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
            "amount": "446802"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "255"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MmM4NTgwYS0yZDgyLTU4ODYtOGQwNC00YjNiMzY4YTFkNzMifQ==",
    "nonce": 170,
    "balances": {
      "current": "10000001637285539",
      "previous": "10000001637541134"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x812ded039db8026df8b86b1f43991cd3cd51e237",
    "nonce": 24,
    "balances": {
      "current": "255340",
      "previous": "0"
    }
  },
  "blockNumber": "10114492",
  "created": "2020-05-22T08:00:10.951Z",
  "updated": "2020-05-22T08:00:11.044Z",
  "id": "5ec7868ae5756b00111b7fa7"
}
```
* *stageAmount*: `255340`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000003e56c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000003e56c000000000000000000000000000000000000000000000000000000000003e56c0f445c0541927cdcfa779f9a7cdb7a18aaacf1957d4547c2478bde58084481234e2bebbe02fb8e0ab584ca2e4d36547e74e95bb5f0100e26c543aaf10813a7640c77b45d3c5948148c935bb71f5660423e24694e12fd0de370c03b937f2de342000000000000000000000000000000000000000000000000000000000000001b27cca521685250d69cdbcfcc96cf1650c12fa694bb922161689a70b5399d3b326cc36e8d64cce53aba4ae23061311e79356188c00e291085aff1bbbb1f36f7bd25a39df47aa2a4578d9a153be05e3cda28afff4e027f7f08b426dd27775ef65f000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55bc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000aa00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d157fea3000000000000000000000000000000000000000000000000002386f2d15be50e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000ff00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000006d15200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d6d4d344e546777595330795a4467794c5455344f4459744f4751774e433030596a4e694d7a59345954466b4e7a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000018000000000000000000000000812ded039db8026df8b86b1f43991cd3cd51e237000000000000000000000000000000000000000000000000000000000003e56c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0f445c0541927cdcfa779f9a7cdb7a18aaacf1957d4547c2478bde5808448123",
      "signature": {
        "s": "0x0c77b45d3c5948148c935bb71f5660423e24694e12fd0de370c03b937f2de342",
        "r": "0x4e2bebbe02fb8e0ab584ca2e4d36547e74e95bb5f0100e26c543aaf10813a764",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x27cca521685250d69cdbcfcc96cf1650c12fa694bb922161689a70b5399d3b32",
      "signature": {
        "s": "0x25a39df47aa2a4578d9a153be05e3cda28afff4e027f7f08b426dd27775ef65f",
        "r": "0x6cc36e8d64cce53aba4ae23061311e79356188c00e291085aff1bbbb1f36f7bd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "255340",
    "total": "255340"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "255340",
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
            "amount": "446802"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "255"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MmM4NTgwYS0yZDgyLTU4ODYtOGQwNC00YjNiMzY4YTFkNzMifQ==",
    "nonce": 170,
    "balances": {
      "current": "10000001637285539",
      "previous": "10000001637541134"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x812ded039db8026df8b86b1f43991cd3cd51e237",
    "nonce": 24,
    "balances": {
      "current": "255340",
      "previous": "0"
    }
  },
  "blockNumber": "10114492",
  "created": "2020-05-22T08:00:10.951Z",
  "updated": "2020-05-22T08:00:11.044Z",
  "id": "5ec7868ae5756b00111b7fa7"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000003e56c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `255340`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``