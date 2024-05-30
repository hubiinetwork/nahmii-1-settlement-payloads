# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xA5918ECdD8e44307a3C8B26Aae71A781a8e087A7`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000027f166e12e08353000000000000000000000000000000000000000000000000000f62e870b260a70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000f62e870b260a700000000000000000000000000000000000000000000000001afc19265203017362c3a1310daf43d0727642b6d95a8fd88dd8561bc799f3cdd633cfe6dec54bc74ccbc75df5328740ba12765804b7655a449cc8d43682cbc5d53c45d72b26d5562b2527cb1fe24304478c4fb12e383f60f6126d8a52387e8373d5358baaa7399000000000000000000000000000000000000000000000000000000000000001b00b1c77fc9617e4764331bf59d889652c45c3a07d3afa8dbf62fc305eb49264cb4b3db955a1b47d96b2bbc45ef0a94d02bb70fdaa5c1de5f55f756c77888fed5376a1f061ffdeb183324c286bc906ece9b9039e0c1bf42cfa0816c894c2febcd000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abef000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009c17d4e76e677f6007cd000000000000000000000000000000000000000000009c17d4f6d5404c5837e800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000003f05c45cf740000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4767ebd7249493e590000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d475a694e5456684f4331695a4455354c5455785a574d744f475a6a4e7930324d4455314e5452694d6a4d784e44556966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000a5918ecdd8e44307a3c8b26aae71a781a8e087a7000000000000000000000000000000000000000000000000027f166e12e08353000000000000000000000000000000000000000000000000026fb385a22e22ac00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x362c3a1310daf43d0727642b6d95a8fd88dd8561bc799f3cdd633cfe6dec54bc",
      "signature": {
        "s": "0x62b2527cb1fe24304478c4fb12e383f60f6126d8a52387e8373d5358baaa7399",
        "r": "0x74ccbc75df5328740ba12765804b7655a449cc8d43682cbc5d53c45d72b26d55",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x00b1c77fc9617e4764331bf59d889652c45c3a07d3afa8dbf62fc305eb49264c",
      "signature": {
        "s": "0x376a1f061ffdeb183324c286bc906ece9b9039e0c1bf42cfa0816c894c2febcd",
        "r": "0xb4b3db955a1b47d96b2bbc45ef0a94d02bb70fdaa5c1de5f55f756c77888fed5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4330875113332903",
    "total": "121528549468286999"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4330875113332903",
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
            "amount": "27235932723037392682585"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4330875113332"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3MGZiNTVhOC1iZDU5LTUxZWMtOGZjNy02MDU1NTRiMjMxNDUifQ==",
    "nonce": 109551,
    "balances": {
      "current": "737128787793406431594445",
      "previous": "737128792128612420040680"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa5918ecdd8e44307a3c8b26aae71a781a8e087a7",
    "nonce": 46,
    "balances": {
      "current": "179887172137026387",
      "previous": "175556297023693484"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:48:41.125Z",
  "updated": "2022-05-04T08:48:41.199Z",
  "id": "62723de9bbd75600116d0437"
}
```
* *stageAmount*: `179887172137026387`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000f62e870b260a70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000f62e870b260a700000000000000000000000000000000000000000000000001afc19265203017362c3a1310daf43d0727642b6d95a8fd88dd8561bc799f3cdd633cfe6dec54bc74ccbc75df5328740ba12765804b7655a449cc8d43682cbc5d53c45d72b26d5562b2527cb1fe24304478c4fb12e383f60f6126d8a52387e8373d5358baaa7399000000000000000000000000000000000000000000000000000000000000001b00b1c77fc9617e4764331bf59d889652c45c3a07d3afa8dbf62fc305eb49264cb4b3db955a1b47d96b2bbc45ef0a94d02bb70fdaa5c1de5f55f756c77888fed5376a1f061ffdeb183324c286bc906ece9b9039e0c1bf42cfa0816c894c2febcd000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abef000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009c17d4e76e677f6007cd000000000000000000000000000000000000000000009c17d4f6d5404c5837e800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000003f05c45cf740000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4767ebd7249493e590000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d475a694e5456684f4331695a4455354c5455785a574d744f475a6a4e7930324d4455314e5452694d6a4d784e44556966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000a5918ecdd8e44307a3c8b26aae71a781a8e087a7000000000000000000000000000000000000000000000000027f166e12e08353000000000000000000000000000000000000000000000000026fb385a22e22ac00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x362c3a1310daf43d0727642b6d95a8fd88dd8561bc799f3cdd633cfe6dec54bc",
      "signature": {
        "s": "0x62b2527cb1fe24304478c4fb12e383f60f6126d8a52387e8373d5358baaa7399",
        "r": "0x74ccbc75df5328740ba12765804b7655a449cc8d43682cbc5d53c45d72b26d55",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x00b1c77fc9617e4764331bf59d889652c45c3a07d3afa8dbf62fc305eb49264c",
      "signature": {
        "s": "0x376a1f061ffdeb183324c286bc906ece9b9039e0c1bf42cfa0816c894c2febcd",
        "r": "0xb4b3db955a1b47d96b2bbc45ef0a94d02bb70fdaa5c1de5f55f756c77888fed5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4330875113332903",
    "total": "121528549468286999"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4330875113332903",
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
            "amount": "27235932723037392682585"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4330875113332"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3MGZiNTVhOC1iZDU5LTUxZWMtOGZjNy02MDU1NTRiMjMxNDUifQ==",
    "nonce": 109551,
    "balances": {
      "current": "737128787793406431594445",
      "previous": "737128792128612420040680"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa5918ecdd8e44307a3c8b26aae71a781a8e087a7",
    "nonce": 46,
    "balances": {
      "current": "179887172137026387",
      "previous": "175556297023693484"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:48:41.125Z",
  "updated": "2022-05-04T08:48:41.199Z",
  "id": "62723de9bbd75600116d0437"
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
0x0f200f9b000000000000000000000000000000000000000000000000027f166e12e083530000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `179887172137026387`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`