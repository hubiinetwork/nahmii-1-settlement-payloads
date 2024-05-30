# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x08f63df12A8d6C5AD5425fE8433C5E4de9413C9C`.

The ordered steps of contract function invocations are included below and in
the corresponding [steps.json](./steps.json). Please read [the general recipe
for settling Nahmii 1 balance](../../README.md) before starting on the first
step of settlement.

## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a))
#### Method name
*stopChallenge*
#### Method payload
```
0xc19df1e40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
### Step 2
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000002a77349affc314e440000000000000000000000000000000000000000000000001604c50a7b2c8df80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000001604c50a7b2c8df800000000000000000000000000000000000000000000000269dd3cf7a04eb8dd89c31bce5519d6447590157d4dcdc5c070222ce85552325242a26eac0f560f6e5bce53167383eea1a5600b665d6d54d8a50211d59a11ad1ce60bedd4faf2b5b572b8e2e59e68e686c46f5577a07dc1c60a5e0c60c17b1af39e3fb37f15190e39000000000000000000000000000000000000000000000000000000000000001b6bdca0f04f8e6454d1665cd884fa194fdf3b8f0ffea0b6e93b43dbea69e83b37b217f0ff0707f8f89e799ea11a65d2cac8b150a159cb2a30ba02d7cee6597a552dc8b20b7e9accf6e6f7ff770d11dfe1e0529b1dd39a2328adc84a49e173627c000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074de0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b485000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000395d3ab05624f216554f00000000000000000000000000000000000000000000395d50babe32c3e9969e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000005a30356a6b3570000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ddb654576dbfd6370f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e544d354e6d49355a6930775a6a59354c54566b4f545574595456684d79316c4d7a63304d44426c4d4745345932496966513d3d000000000000000000000000000000000000000000000000000000000000002300000000000000000000000008f63df12a8d6c5ad5425fe8433c5e4de9413c9c000000000000000000000000000000000000000000000002a77349affc314e44000000000000000000000000000000000000000000000002916e84a58104c04c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x89c31bce5519d6447590157d4dcdc5c070222ce85552325242a26eac0f560f6e",
      "signature": {
        "s": "0x72b8e2e59e68e686c46f5577a07dc1c60a5e0c60c17b1af39e3fb37f15190e39",
        "r": "0x5bce53167383eea1a5600b665d6d54d8a50211d59a11ad1ce60bedd4faf2b5b5",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6bdca0f04f8e6454d1665cd884fa194fdf3b8f0ffea0b6e93b43dbea69e83b37",
      "signature": {
        "s": "0x2dc8b20b7e9accf6e6f7ff770d11dfe1e0529b1dd39a2328adc84a49e173627c",
        "r": "0xb217f0ff0707f8f89e799ea11a65d2cac8b150a159cb2a30ba02d7cee6597a55",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1586609617548119544",
    "total": "44521808525498693853"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1586609617548119544",
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
            "amount": "27701701076779865093903"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1586609617548119"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0NTM5NmI5Zi0wZjY5LTVkOTUtYTVhMy1lMzc0MDBlMGE4Y2IifQ==",
    "nonce": 111749,
    "balances": {
      "current": "270894665697191546737999",
      "previous": "270896253893418712405662"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x08f63df12a8d6c5ad5425fe8433c5e4de9413c9c",
    "nonce": 35,
    "balances": {
      "current": "48959556994273988164",
      "previous": "47372947376725868620"
    }
  },
  "blockNumber": "14709982",
  "created": "2022-05-04T08:59:56.759Z",
  "updated": "2022-05-04T08:59:56.898Z",
  "id": "6272408cbbd75600116d070a"
}
```
* *stageAmount*: `48959556994273988164`
### Step 3
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000001604c50a7b2c8df80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000001604c50a7b2c8df800000000000000000000000000000000000000000000000269dd3cf7a04eb8dd89c31bce5519d6447590157d4dcdc5c070222ce85552325242a26eac0f560f6e5bce53167383eea1a5600b665d6d54d8a50211d59a11ad1ce60bedd4faf2b5b572b8e2e59e68e686c46f5577a07dc1c60a5e0c60c17b1af39e3fb37f15190e39000000000000000000000000000000000000000000000000000000000000001b6bdca0f04f8e6454d1665cd884fa194fdf3b8f0ffea0b6e93b43dbea69e83b37b217f0ff0707f8f89e799ea11a65d2cac8b150a159cb2a30ba02d7cee6597a552dc8b20b7e9accf6e6f7ff770d11dfe1e0529b1dd39a2328adc84a49e173627c000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074de0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b485000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000395d3ab05624f216554f00000000000000000000000000000000000000000000395d50babe32c3e9969e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000005a30356a6b3570000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ddb654576dbfd6370f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e544d354e6d49355a6930775a6a59354c54566b4f545574595456684d79316c4d7a63304d44426c4d4745345932496966513d3d000000000000000000000000000000000000000000000000000000000000002300000000000000000000000008f63df12a8d6c5ad5425fe8433c5e4de9413c9c000000000000000000000000000000000000000000000002a77349affc314e44000000000000000000000000000000000000000000000002916e84a58104c04c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x89c31bce5519d6447590157d4dcdc5c070222ce85552325242a26eac0f560f6e",
      "signature": {
        "s": "0x72b8e2e59e68e686c46f5577a07dc1c60a5e0c60c17b1af39e3fb37f15190e39",
        "r": "0x5bce53167383eea1a5600b665d6d54d8a50211d59a11ad1ce60bedd4faf2b5b5",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6bdca0f04f8e6454d1665cd884fa194fdf3b8f0ffea0b6e93b43dbea69e83b37",
      "signature": {
        "s": "0x2dc8b20b7e9accf6e6f7ff770d11dfe1e0529b1dd39a2328adc84a49e173627c",
        "r": "0xb217f0ff0707f8f89e799ea11a65d2cac8b150a159cb2a30ba02d7cee6597a55",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1586609617548119544",
    "total": "44521808525498693853"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1586609617548119544",
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
            "amount": "27701701076779865093903"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1586609617548119"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0NTM5NmI5Zi0wZjY5LTVkOTUtYTVhMy1lMzc0MDBlMGE4Y2IifQ==",
    "nonce": 111749,
    "balances": {
      "current": "270894665697191546737999",
      "previous": "270896253893418712405662"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x08f63df12a8d6c5ad5425fe8433c5e4de9413c9c",
    "nonce": 35,
    "balances": {
      "current": "48959556994273988164",
      "previous": "47372947376725868620"
    }
  },
  "blockNumber": "14709982",
  "created": "2022-05-04T08:59:56.759Z",
  "updated": "2022-05-04T08:59:56.898Z",
  "id": "6272408cbbd75600116d070a"
}
```
* *standard*: `ERC20`
### Step 4
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b000000000000000000000000000000000000000000000002a77349affc314e440000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `48959556994273988164`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`