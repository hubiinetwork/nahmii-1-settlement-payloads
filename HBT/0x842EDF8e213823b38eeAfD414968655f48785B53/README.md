# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x842EDF8e213823b38eeAfD414968655f48785B53`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000004ed52916000000000000000000000000000000000000000000000000000000004ed52916000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004ed52916000000000000000000000000000000000000000000000000000000004ed52916a0f29e4c48a5011a05c8d379723993dc73b5db6dcbcfbeec52a53c05046ebf060879f4f4c061b6c469ec8fc3d737c6d2f914377757a7b3b036e6f1dbe5ef15fe4f710dd3c97e8e7bec4c01c8e15d0c1397778914b5b6c6d9f17ac2a950ec634a000000000000000000000000000000000000000000000000000000000000001cc82543730bff6b0e5d994495812f08d545e00d733c94a0688fe7077e51c2acf2ef95b991e5d366a672807095d83a95bb85d361a65517ab242cb8b59701fd68b90695132c7af6eec1437a4b4ccd1d57ab9916df51db84017b0e32a30e8e645f7e000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ac00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c2000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e13a132cdc87a000000000000000000000000000000000000000000000000002e13a181b71ff000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000142e60000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b3b42a21d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a475a6b596a4668597930354f474e684c54566b59574d7459574d304e6931685a575977596d46685a4459355a6d496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000842edf8e213823b38eeafd414968655f48785b53000000000000000000000000000000000000000000000000000000004ed52916000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa0f29e4c48a5011a05c8d379723993dc73b5db6dcbcfbeec52a53c05046ebf06",
      "signature": {
        "s": "0x4f710dd3c97e8e7bec4c01c8e15d0c1397778914b5b6c6d9f17ac2a950ec634a",
        "r": "0x0879f4f4c061b6c469ec8fc3d737c6d2f914377757a7b3b036e6f1dbe5ef15fe",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc82543730bff6b0e5d994495812f08d545e00d733c94a0688fe7077e51c2acf2",
      "signature": {
        "s": "0x0695132c7af6eec1437a4b4ccd1d57ab9916df51db84017b0e32a30e8e645f7e",
        "r": "0xef95b991e5d366a672807095d83a95bb85d361a65517ab242cb8b59701fd68b9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1322592534",
    "total": "1322592534"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1322592534",
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
            "amount": "48238862877"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1322592"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2ZGZkYjFhYy05OGNhLTVkYWMtYWM0Ni1hZWYwYmFhZDY5ZmIifQ==",
    "nonce": 7200,
    "balances": {
      "current": "12969431991699578",
      "previous": "12969433315614704"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x842edf8e213823b38eeafd414968655f48785b53",
    "nonce": 22,
    "balances": {
      "current": "1322592534",
      "previous": "0"
    }
  },
  "blockNumber": "10114732",
  "created": "2020-05-22T08:54:57.608Z",
  "updated": "2020-05-22T08:54:57.758Z",
  "id": "5ec79361e5756b00111b889d"
}
```
* *stageAmount*: `1322592534`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000004ed52916000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004ed52916000000000000000000000000000000000000000000000000000000004ed52916a0f29e4c48a5011a05c8d379723993dc73b5db6dcbcfbeec52a53c05046ebf060879f4f4c061b6c469ec8fc3d737c6d2f914377757a7b3b036e6f1dbe5ef15fe4f710dd3c97e8e7bec4c01c8e15d0c1397778914b5b6c6d9f17ac2a950ec634a000000000000000000000000000000000000000000000000000000000000001cc82543730bff6b0e5d994495812f08d545e00d733c94a0688fe7077e51c2acf2ef95b991e5d366a672807095d83a95bb85d361a65517ab242cb8b59701fd68b90695132c7af6eec1437a4b4ccd1d57ab9916df51db84017b0e32a30e8e645f7e000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ac00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c2000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e13a132cdc87a000000000000000000000000000000000000000000000000002e13a181b71ff000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000142e60000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b3b42a21d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a475a6b596a4668597930354f474e684c54566b59574d7459574d304e6931685a575977596d46685a4459355a6d496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000842edf8e213823b38eeafd414968655f48785b53000000000000000000000000000000000000000000000000000000004ed52916000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa0f29e4c48a5011a05c8d379723993dc73b5db6dcbcfbeec52a53c05046ebf06",
      "signature": {
        "s": "0x4f710dd3c97e8e7bec4c01c8e15d0c1397778914b5b6c6d9f17ac2a950ec634a",
        "r": "0x0879f4f4c061b6c469ec8fc3d737c6d2f914377757a7b3b036e6f1dbe5ef15fe",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc82543730bff6b0e5d994495812f08d545e00d733c94a0688fe7077e51c2acf2",
      "signature": {
        "s": "0x0695132c7af6eec1437a4b4ccd1d57ab9916df51db84017b0e32a30e8e645f7e",
        "r": "0xef95b991e5d366a672807095d83a95bb85d361a65517ab242cb8b59701fd68b9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1322592534",
    "total": "1322592534"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1322592534",
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
            "amount": "48238862877"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1322592"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2ZGZkYjFhYy05OGNhLTVkYWMtYWM0Ni1hZWYwYmFhZDY5ZmIifQ==",
    "nonce": 7200,
    "balances": {
      "current": "12969431991699578",
      "previous": "12969433315614704"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x842edf8e213823b38eeafd414968655f48785b53",
    "nonce": 22,
    "balances": {
      "current": "1322592534",
      "previous": "0"
    }
  },
  "blockNumber": "10114732",
  "created": "2020-05-22T08:54:57.608Z",
  "updated": "2020-05-22T08:54:57.758Z",
  "id": "5ec79361e5756b00111b889d"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000004ed52916000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1322592534`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`