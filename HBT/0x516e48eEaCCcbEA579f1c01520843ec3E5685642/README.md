# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x516e48eEaCCcbEA579f1c01520843ec3E5685642`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000c376c70000000000000000000000000000000000000000000000000000000000c376c7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000c376c70000000000000000000000000000000000000000000000000000000000c376c7998bd71dd985919e2d31c25c7c989877e675e6d1f0bc25ab4496711e5771c8c1bc2c53ac4fbb961614ce96ba7f3d95108b4cfdd24f5e0a4f1250928d77e88a1e796a2a09eddcfa71d9ca7e22dae5a98603d519a38c905a60481def6646d9e043000000000000000000000000000000000000000000000000000000000000001c72ff686f575159795509da60ab348f5d81b12bb6b28fd396e1f89814daea1a79684756a5aecd183fea44a66fb9df6a814953f4cfad20e4b10618d1e6f7d154055ba093a86dcd0fd0ad0018118630ef26045eb65e8e4e7f425e0d1d13f401e4ff000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ab00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001be600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e13f4d3c3353a000000000000000000000000000000000000000000000000002e13f4d486de0a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000003209000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b25df6a5a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694978593259344d7a526a596930354f474a694c545532597a4574596d4e684d6930784d4449795954526c4d44466b5a6a6b6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000516e48eeacccbea579f1c01520843ec3e56856420000000000000000000000000000000000000000000000000000000000c376c7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x998bd71dd985919e2d31c25c7c989877e675e6d1f0bc25ab4496711e5771c8c1",
      "signature": {
        "s": "0x796a2a09eddcfa71d9ca7e22dae5a98603d519a38c905a60481def6646d9e043",
        "r": "0xbc2c53ac4fbb961614ce96ba7f3d95108b4cfdd24f5e0a4f1250928d77e88a1e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x72ff686f575159795509da60ab348f5d81b12bb6b28fd396e1f89814daea1a79",
      "signature": {
        "s": "0x5ba093a86dcd0fd0ad0018118630ef26045eb65e8e4e7f425e0d1d13f401e4ff",
        "r": "0x684756a5aecd183fea44a66fb9df6a814953f4cfad20e4b10618d1e6f7d15405",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "12809927",
    "total": "12809927"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12809927",
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
            "amount": "47880039002"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "12809"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxY2Y4MzRjYi05OGJiLTU2YzEtYmNhMi0xMDIyYTRlMDFkZjkifQ==",
    "nonce": 7142,
    "balances": {
      "current": "12969791174423866",
      "previous": "12969791187246602"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x516e48eeacccbea579f1c01520843ec3e5685642",
    "nonce": 22,
    "balances": {
      "current": "12809927",
      "previous": "0"
    }
  },
  "blockNumber": "10114731",
  "created": "2020-05-22T08:54:31.754Z",
  "updated": "2020-05-22T08:54:31.826Z",
  "id": "5ec79347e5756b00111b8887"
}
```
* *stageAmount*: `12809927`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000c376c7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000c376c70000000000000000000000000000000000000000000000000000000000c376c7998bd71dd985919e2d31c25c7c989877e675e6d1f0bc25ab4496711e5771c8c1bc2c53ac4fbb961614ce96ba7f3d95108b4cfdd24f5e0a4f1250928d77e88a1e796a2a09eddcfa71d9ca7e22dae5a98603d519a38c905a60481def6646d9e043000000000000000000000000000000000000000000000000000000000000001c72ff686f575159795509da60ab348f5d81b12bb6b28fd396e1f89814daea1a79684756a5aecd183fea44a66fb9df6a814953f4cfad20e4b10618d1e6f7d154055ba093a86dcd0fd0ad0018118630ef26045eb65e8e4e7f425e0d1d13f401e4ff000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ab00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001be600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e13f4d3c3353a000000000000000000000000000000000000000000000000002e13f4d486de0a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000003209000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b25df6a5a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694978593259344d7a526a596930354f474a694c545532597a4574596d4e684d6930784d4449795954526c4d44466b5a6a6b6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000516e48eeacccbea579f1c01520843ec3e56856420000000000000000000000000000000000000000000000000000000000c376c7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x998bd71dd985919e2d31c25c7c989877e675e6d1f0bc25ab4496711e5771c8c1",
      "signature": {
        "s": "0x796a2a09eddcfa71d9ca7e22dae5a98603d519a38c905a60481def6646d9e043",
        "r": "0xbc2c53ac4fbb961614ce96ba7f3d95108b4cfdd24f5e0a4f1250928d77e88a1e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x72ff686f575159795509da60ab348f5d81b12bb6b28fd396e1f89814daea1a79",
      "signature": {
        "s": "0x5ba093a86dcd0fd0ad0018118630ef26045eb65e8e4e7f425e0d1d13f401e4ff",
        "r": "0x684756a5aecd183fea44a66fb9df6a814953f4cfad20e4b10618d1e6f7d15405",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "12809927",
    "total": "12809927"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12809927",
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
            "amount": "47880039002"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "12809"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxY2Y4MzRjYi05OGJiLTU2YzEtYmNhMi0xMDIyYTRlMDFkZjkifQ==",
    "nonce": 7142,
    "balances": {
      "current": "12969791174423866",
      "previous": "12969791187246602"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x516e48eeacccbea579f1c01520843ec3e5685642",
    "nonce": 22,
    "balances": {
      "current": "12809927",
      "previous": "0"
    }
  },
  "blockNumber": "10114731",
  "created": "2020-05-22T08:54:31.754Z",
  "updated": "2020-05-22T08:54:31.826Z",
  "id": "5ec79347e5756b00111b8887"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000c376c7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `12809927`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`