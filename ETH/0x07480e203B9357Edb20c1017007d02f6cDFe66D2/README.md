# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x07480e203B9357Edb20c1017007d02f6cDFe66D2`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000041eb00000000000000000000000000000000000000000000000000000000000041eb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000041eb00000000000000000000000000000000000000000000000000000000000041ebc53d816d7d60482c63c0a4eca42ff3a20385c38f4f5e4ba023485f8a85178f2d7a48eedfb211fe0b5b32d7c21254f24e76629294016c9649cc049f7dae9488542ef53bd8099d643f0bf86c7f36080f66c14193211a662fe891721abed8d70ae8000000000000000000000000000000000000000000000000000000000000001b096d494920d945ce708ba125f50403ee546b67bef0a81565a4ba558f108c17a9e2b967f160446e3cce21d0f36193befc97fd4f42a6dcf7b37a0087109d7715172a17dc1be3fe6e847de7fe86181b22da5385f1a7fda2312ca96527ae412c9000000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000050200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7b55e3d000000000000000000000000000000000000000000000000002386f2c7b5a03800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000946f700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d6a5977597a457959533034597a4d344c5455314e6a5174596a51774e79316d4d4455774d57553559544d334e44636966513d3d000000000000000000000000000000000000000000000000000000000000000d00000000000000000000000007480e203b9357edb20c1017007d02f6cdfe66d200000000000000000000000000000000000000000000000000000000000041eb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc53d816d7d60482c63c0a4eca42ff3a20385c38f4f5e4ba023485f8a85178f2d",
      "signature": {
        "s": "0x2ef53bd8099d643f0bf86c7f36080f66c14193211a662fe891721abed8d70ae8",
        "r": "0x7a48eedfb211fe0b5b32d7c21254f24e76629294016c9649cc049f7dae948854",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x096d494920d945ce708ba125f50403ee546b67bef0a81565a4ba558f108c17a9",
      "signature": {
        "s": "0x2a17dc1be3fe6e847de7fe86181b22da5385f1a7fda2312ca96527ae412c9000",
        "r": "0xe2b967f160446e3cce21d0f36193befc97fd4f42a6dcf7b37a0087109d771517",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "16875",
    "total": "16875"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16875",
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
            "amount": "607991"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "16"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkMjYwYzEyYS04YzM4LTU1NjQtYjQwNy1mMDUwMWU5YTM3NDcifQ==",
    "nonce": 1282,
    "balances": {
      "current": "10000001475632701",
      "previous": "10000001475649592"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x07480e203b9357edb20c1017007d02f6cdfe66d2",
    "nonce": 13,
    "balances": {
      "current": "16875",
      "previous": "0"
    }
  },
  "blockNumber": "10114523",
  "created": "2020-05-22T08:08:11.028Z",
  "updated": "2020-05-22T08:08:11.101Z",
  "id": "5ec7886bb0c6090011d5aa75"
}
```
* *stageAmount*: `16875`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000041eb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000041eb00000000000000000000000000000000000000000000000000000000000041ebc53d816d7d60482c63c0a4eca42ff3a20385c38f4f5e4ba023485f8a85178f2d7a48eedfb211fe0b5b32d7c21254f24e76629294016c9649cc049f7dae9488542ef53bd8099d643f0bf86c7f36080f66c14193211a662fe891721abed8d70ae8000000000000000000000000000000000000000000000000000000000000001b096d494920d945ce708ba125f50403ee546b67bef0a81565a4ba558f108c17a9e2b967f160446e3cce21d0f36193befc97fd4f42a6dcf7b37a0087109d7715172a17dc1be3fe6e847de7fe86181b22da5385f1a7fda2312ca96527ae412c9000000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000050200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7b55e3d000000000000000000000000000000000000000000000000002386f2c7b5a03800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000946f700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d6a5977597a457959533034597a4d344c5455314e6a5174596a51774e79316d4d4455774d57553559544d334e44636966513d3d000000000000000000000000000000000000000000000000000000000000000d00000000000000000000000007480e203b9357edb20c1017007d02f6cdfe66d200000000000000000000000000000000000000000000000000000000000041eb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc53d816d7d60482c63c0a4eca42ff3a20385c38f4f5e4ba023485f8a85178f2d",
      "signature": {
        "s": "0x2ef53bd8099d643f0bf86c7f36080f66c14193211a662fe891721abed8d70ae8",
        "r": "0x7a48eedfb211fe0b5b32d7c21254f24e76629294016c9649cc049f7dae948854",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x096d494920d945ce708ba125f50403ee546b67bef0a81565a4ba558f108c17a9",
      "signature": {
        "s": "0x2a17dc1be3fe6e847de7fe86181b22da5385f1a7fda2312ca96527ae412c9000",
        "r": "0xe2b967f160446e3cce21d0f36193befc97fd4f42a6dcf7b37a0087109d771517",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "16875",
    "total": "16875"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16875",
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
            "amount": "607991"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "16"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkMjYwYzEyYS04YzM4LTU1NjQtYjQwNy1mMDUwMWU5YTM3NDcifQ==",
    "nonce": 1282,
    "balances": {
      "current": "10000001475632701",
      "previous": "10000001475649592"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x07480e203b9357edb20c1017007d02f6cdfe66d2",
    "nonce": 13,
    "balances": {
      "current": "16875",
      "previous": "0"
    }
  },
  "blockNumber": "10114523",
  "created": "2020-05-22T08:08:11.028Z",
  "updated": "2020-05-22T08:08:11.101Z",
  "id": "5ec7886bb0c6090011d5aa75"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000041eb0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `16875`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``