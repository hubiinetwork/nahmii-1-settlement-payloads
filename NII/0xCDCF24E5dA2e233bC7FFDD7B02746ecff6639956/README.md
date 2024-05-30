# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xCDCF24E5dA2e233bC7FFDD7B02746ecff6639956`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de3b44d725ca4cb0000000000000000000000000000000000000000000000fda2c870e3678a00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000fda2c870e3678a00000000000000000000000000000000000000000000000000fda2c870e3678a0000b4564f7b8f12d94d6efb06f0808aeebe878b1600e92b4759deab0c8914f8cd6bdbaf7fb9109c357c3094d491c32d48c16885c2e588beb6bec8ff7a3c1de5cfe166095990347563fd3d474d11ba6eb09891d6529980ea357c1b3cbcb24a44da8e000000000000000000000000000000000000000000000000000000000000001c363b029a98a1b5cd19e2aeea2a9a7272562779d3d0191f9750136e07759340c77cb54ecbc9e343055d8084f4ade9109149a7b132ff8e6f8eb75d0046f80e365347b5fb49b50e4b3bd3e0054f90a9d0c1c70aa89dd57628c7ef21a5f198221f70000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1b9420000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002f000000000000000000000000cdcf24e5da2e233bc7ffdd7b02746ecff66399560000000000000000000000000000000000000000000000000de3b44d725ca4cb0000000000000000000000000000000000000000000000fdf19a6cfbd4a0e4cb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000040ee47cafaba40000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000040ee47cafaba40000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a545a6c4d7a4d304d5331694f574d7a4c545268597a6774596a59784f4330305a6a6868596a4d33597a51795a47556966513d3d0000000000000000000000000000000000000000000000000000000000000007000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000000f6c3759ce0f1a8abe77000000000000000000000000000000000000000000000e6e94915d2bb300be7700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb4564f7b8f12d94d6efb06f0808aeebe878b1600e92b4759deab0c8914f8cd6b",
      "signature": {
        "s": "0x66095990347563fd3d474d11ba6eb09891d6529980ea357c1b3cbcb24a44da8e",
        "r": "0xdbaf7fb9109c357c3094d491c32d48c16885c2e588beb6bec8ff7a3c1de5cfe1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x363b029a98a1b5cd19e2aeea2a9a7272562779d3d0191f9750136e07759340c7",
      "signature": {
        "s": "0x47b5fb49b50e4b3bd3e0054f90a9d0c1c70aa89dd57628c7ef21a5f198221f70",
        "r": "0x7cb54ecbc9e343055d8084f4ade9109149a7b132ff8e6f8eb75d0046f80e3653",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4678756000000000000000",
    "total": "4678756000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4678756000000000000000",
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
            "amount": "4678756000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4678756000000000000"
      }
    },
    "wallet": "0xcdcf24e5da2e233bc7ffdd7b02746ecff6639956",
    "data": "eyJyZWYiOiIxZTZlMzM0MS1iOWMzLTRhYzgtYjYxOC00ZjhhYjM3YzQyZGUifQ==",
    "nonce": 47,
    "balances": {
      "current": "1000841786930537675",
      "previous": "4684435597786930537675"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 7,
    "balances": {
      "current": "72831734048514588196471",
      "previous": "68152978048514588196471"
    }
  },
  "blockNumber": "14793026",
  "created": "2022-05-17T14:28:50.221Z",
  "updated": "2022-05-17T14:28:50.298Z",
  "id": "6283b122bbd75600116d0887"
}
```
* *stageAmount*: `1000841786930537675`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000fda2c870e3678a00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000fda2c870e3678a00000000000000000000000000000000000000000000000000fda2c870e3678a0000b4564f7b8f12d94d6efb06f0808aeebe878b1600e92b4759deab0c8914f8cd6bdbaf7fb9109c357c3094d491c32d48c16885c2e588beb6bec8ff7a3c1de5cfe166095990347563fd3d474d11ba6eb09891d6529980ea357c1b3cbcb24a44da8e000000000000000000000000000000000000000000000000000000000000001c363b029a98a1b5cd19e2aeea2a9a7272562779d3d0191f9750136e07759340c77cb54ecbc9e343055d8084f4ade9109149a7b132ff8e6f8eb75d0046f80e365347b5fb49b50e4b3bd3e0054f90a9d0c1c70aa89dd57628c7ef21a5f198221f70000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1b9420000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002f000000000000000000000000cdcf24e5da2e233bc7ffdd7b02746ecff66399560000000000000000000000000000000000000000000000000de3b44d725ca4cb0000000000000000000000000000000000000000000000fdf19a6cfbd4a0e4cb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000040ee47cafaba40000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000040ee47cafaba40000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a545a6c4d7a4d304d5331694f574d7a4c545268597a6774596a59784f4330305a6a6868596a4d33597a51795a47556966513d3d0000000000000000000000000000000000000000000000000000000000000007000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000000f6c3759ce0f1a8abe77000000000000000000000000000000000000000000000e6e94915d2bb300be7700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb4564f7b8f12d94d6efb06f0808aeebe878b1600e92b4759deab0c8914f8cd6b",
      "signature": {
        "s": "0x66095990347563fd3d474d11ba6eb09891d6529980ea357c1b3cbcb24a44da8e",
        "r": "0xdbaf7fb9109c357c3094d491c32d48c16885c2e588beb6bec8ff7a3c1de5cfe1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x363b029a98a1b5cd19e2aeea2a9a7272562779d3d0191f9750136e07759340c7",
      "signature": {
        "s": "0x47b5fb49b50e4b3bd3e0054f90a9d0c1c70aa89dd57628c7ef21a5f198221f70",
        "r": "0x7cb54ecbc9e343055d8084f4ade9109149a7b132ff8e6f8eb75d0046f80e3653",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4678756000000000000000",
    "total": "4678756000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4678756000000000000000",
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
            "amount": "4678756000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4678756000000000000"
      }
    },
    "wallet": "0xcdcf24e5da2e233bc7ffdd7b02746ecff6639956",
    "data": "eyJyZWYiOiIxZTZlMzM0MS1iOWMzLTRhYzgtYjYxOC00ZjhhYjM3YzQyZGUifQ==",
    "nonce": 47,
    "balances": {
      "current": "1000841786930537675",
      "previous": "4684435597786930537675"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 7,
    "balances": {
      "current": "72831734048514588196471",
      "previous": "68152978048514588196471"
    }
  },
  "blockNumber": "14793026",
  "created": "2022-05-17T14:28:50.221Z",
  "updated": "2022-05-17T14:28:50.298Z",
  "id": "6283b122bbd75600116d0887"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de3b44d725ca4cb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000841786930537675`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`