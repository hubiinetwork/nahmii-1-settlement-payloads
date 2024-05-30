# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x95EE72df6025469499Af16e6d79E7db35F567aD1`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000fe1687d800000000000000000000000000000000000000000000000000000000fe1687d8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000fe1687d800000000000000000000000000000000000000000000000000000000fe1687d8f1fab0144825c7b3b8f6eaa74ae1fd6515d29a4424c7f32aa839bc63da6afcf60aa8d4e57a3c60811d92932eac4163eb99519423941d04710b09a6a74047feec21a9ff5ce2029622c9931f66048df18b53472352894bd835ca75fc8d54791285000000000000000000000000000000000000000000000000000000000000001bf5b10c18f4ae6ff534700329f5bb2de1cd6f43893049f6f5d64ad650f5f5bdc03cb7f07817bd7931ea6b01c62c8c3fcd17a997603bdd1ada7055a3e7678c125e70813e2b229eb75d7a45f7f8989b8beeed1ca47b006bd51dea17a837a3500a78000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56a200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b1500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15c34219b069000000000000000000000000000000000000000000000000002e15c44071442a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000410be9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000aaf9bd06a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e32497a4e6d49354e43316c59324d304c545532597a6774596a4a6a4d53316d4d446c684e5463774d44637759324d6966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000095ee72df6025469499af16e6d79e7db35f567ad100000000000000000000000000000000000000000000000000000000fe1687d8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf1fab0144825c7b3b8f6eaa74ae1fd6515d29a4424c7f32aa839bc63da6afcf6",
      "signature": {
        "s": "0x21a9ff5ce2029622c9931f66048df18b53472352894bd835ca75fc8d54791285",
        "r": "0x0aa8d4e57a3c60811d92932eac4163eb99519423941d04710b09a6a74047feec",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf5b10c18f4ae6ff534700329f5bb2de1cd6f43893049f6f5d64ad650f5f5bdc0",
      "signature": {
        "s": "0x70813e2b229eb75d7a45f7f8989b8beeed1ca47b006bd51dea17a837a3500a78",
        "r": "0x3cb7f07817bd7931ea6b01c62c8c3fcd17a997603bdd1ada7055a3e7678c125e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4262889432",
    "total": "4262889432"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4262889432",
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
            "amount": "45895897194"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "4262889"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlN2IzNmI5NC1lY2M0LTU2YzgtYjJjMS1mMDlhNTcwMDcwY2MifQ==",
    "nonce": 6933,
    "balances": {
      "current": "12971777300476009",
      "previous": "12971781567628330"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x95ee72df6025469499af16e6d79e7db35f567ad1",
    "nonce": 22,
    "balances": {
      "current": "4262889432",
      "previous": "0"
    }
  },
  "blockNumber": "10114722",
  "created": "2020-05-22T08:52:50.973Z",
  "updated": "2020-05-22T08:52:51.040Z",
  "id": "5ec792e2b0c6090011d5b1d9"
}
```
* *stageAmount*: `4262889432`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000fe1687d8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000fe1687d800000000000000000000000000000000000000000000000000000000fe1687d8f1fab0144825c7b3b8f6eaa74ae1fd6515d29a4424c7f32aa839bc63da6afcf60aa8d4e57a3c60811d92932eac4163eb99519423941d04710b09a6a74047feec21a9ff5ce2029622c9931f66048df18b53472352894bd835ca75fc8d54791285000000000000000000000000000000000000000000000000000000000000001bf5b10c18f4ae6ff534700329f5bb2de1cd6f43893049f6f5d64ad650f5f5bdc03cb7f07817bd7931ea6b01c62c8c3fcd17a997603bdd1ada7055a3e7678c125e70813e2b229eb75d7a45f7f8989b8beeed1ca47b006bd51dea17a837a3500a78000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56a200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b1500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15c34219b069000000000000000000000000000000000000000000000000002e15c44071442a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000410be9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000aaf9bd06a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e32497a4e6d49354e43316c59324d304c545532597a6774596a4a6a4d53316d4d446c684e5463774d44637759324d6966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000095ee72df6025469499af16e6d79e7db35f567ad100000000000000000000000000000000000000000000000000000000fe1687d8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf1fab0144825c7b3b8f6eaa74ae1fd6515d29a4424c7f32aa839bc63da6afcf6",
      "signature": {
        "s": "0x21a9ff5ce2029622c9931f66048df18b53472352894bd835ca75fc8d54791285",
        "r": "0x0aa8d4e57a3c60811d92932eac4163eb99519423941d04710b09a6a74047feec",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf5b10c18f4ae6ff534700329f5bb2de1cd6f43893049f6f5d64ad650f5f5bdc0",
      "signature": {
        "s": "0x70813e2b229eb75d7a45f7f8989b8beeed1ca47b006bd51dea17a837a3500a78",
        "r": "0x3cb7f07817bd7931ea6b01c62c8c3fcd17a997603bdd1ada7055a3e7678c125e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4262889432",
    "total": "4262889432"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4262889432",
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
            "amount": "45895897194"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "4262889"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlN2IzNmI5NC1lY2M0LTU2YzgtYjJjMS1mMDlhNTcwMDcwY2MifQ==",
    "nonce": 6933,
    "balances": {
      "current": "12971777300476009",
      "previous": "12971781567628330"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x95ee72df6025469499af16e6d79e7db35f567ad1",
    "nonce": 22,
    "balances": {
      "current": "4262889432",
      "previous": "0"
    }
  },
  "blockNumber": "10114722",
  "created": "2020-05-22T08:52:50.973Z",
  "updated": "2020-05-22T08:52:51.040Z",
  "id": "5ec792e2b0c6090011d5b1d9"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000fe1687d8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4262889432`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`