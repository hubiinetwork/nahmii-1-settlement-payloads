# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xC6A69ED0dCFF3a1E40eA8D965ec6A69EE081d532`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000005de77340000000000000000000000000000000000000000000000000000000005de7734000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000005de77340000000000000000000000000000000000000000000000000000000005de7734ad9b1f2425465a6e8a7a0e748c450238e1cf4b6204ea20ed90009758553f4c72d2bbbdb192e3bdf20a3ab21288501d6b0527ddf514adf9a338883a1aa7d16dcd0185acf75e2e44e430616b45767d5cd9c8ac60831643814314a6d2beccc0adc1000000000000000000000000000000000000000000000000000000000000001baaa8f51b7d024b344047676c59226557412522635925d09647fbeb5f8099a95c0fc7d8f903f1a50eb5c81b8061862a6b2700dd776523489cb5a892b657e717434688047438bdbc9b3e44ca06a03f4502aac39b6781014d59a231e95b2ade097a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a569c00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001aaa00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e162fe794fa48000000000000000000000000000000000000000000000000002e162fed74f21d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000180a1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a93d2ad38000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e6d526b4f4749795a4330354e7a55794c5456685a6d5974596d4a6d5a4330334f54637a4e7a55314e6a63325957516966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c6a69ed0dcff3a1e40ea8d965ec6a69ee081d5320000000000000000000000000000000000000000000000000000000005de7734000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xad9b1f2425465a6e8a7a0e748c450238e1cf4b6204ea20ed90009758553f4c72",
      "signature": {
        "s": "0x0185acf75e2e44e430616b45767d5cd9c8ac60831643814314a6d2beccc0adc1",
        "r": "0xd2bbbdb192e3bdf20a3ab21288501d6b0527ddf514adf9a338883a1aa7d16dcd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xaaa8f51b7d024b344047676c59226557412522635925d09647fbeb5f8099a95c",
      "signature": {
        "s": "0x4688047438bdbc9b3e44ca06a03f4502aac39b6781014d59a231e95b2ade097a",
        "r": "0x0fc7d8f903f1a50eb5c81b8061862a6b2700dd776523489cb5a892b657e71743",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "98465588",
    "total": "98465588"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "98465588",
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
            "amount": "45429730616"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "98465"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkNmRkOGIyZC05NzUyLTVhZmYtYmJmZC03OTczNzU1Njc2YWQifQ==",
    "nonce": 6826,
    "balances": {
      "current": "12972243933264456",
      "previous": "12972244031828509"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc6a69ed0dcff3a1e40ea8d965ec6a69ee081d532",
    "nonce": 22,
    "balances": {
      "current": "98465588",
      "previous": "0"
    }
  },
  "blockNumber": "10114716",
  "created": "2020-05-22T08:51:59.092Z",
  "updated": "2020-05-22T08:51:59.157Z",
  "id": "5ec792afb0c6090011d5b1af"
}
```
* *stageAmount*: `98465588`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000005de7734000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000005de77340000000000000000000000000000000000000000000000000000000005de7734ad9b1f2425465a6e8a7a0e748c450238e1cf4b6204ea20ed90009758553f4c72d2bbbdb192e3bdf20a3ab21288501d6b0527ddf514adf9a338883a1aa7d16dcd0185acf75e2e44e430616b45767d5cd9c8ac60831643814314a6d2beccc0adc1000000000000000000000000000000000000000000000000000000000000001baaa8f51b7d024b344047676c59226557412522635925d09647fbeb5f8099a95c0fc7d8f903f1a50eb5c81b8061862a6b2700dd776523489cb5a892b657e717434688047438bdbc9b3e44ca06a03f4502aac39b6781014d59a231e95b2ade097a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a569c00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001aaa00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e162fe794fa48000000000000000000000000000000000000000000000000002e162fed74f21d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000180a1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a93d2ad38000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e6d526b4f4749795a4330354e7a55794c5456685a6d5974596d4a6d5a4330334f54637a4e7a55314e6a63325957516966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c6a69ed0dcff3a1e40ea8d965ec6a69ee081d5320000000000000000000000000000000000000000000000000000000005de7734000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xad9b1f2425465a6e8a7a0e748c450238e1cf4b6204ea20ed90009758553f4c72",
      "signature": {
        "s": "0x0185acf75e2e44e430616b45767d5cd9c8ac60831643814314a6d2beccc0adc1",
        "r": "0xd2bbbdb192e3bdf20a3ab21288501d6b0527ddf514adf9a338883a1aa7d16dcd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xaaa8f51b7d024b344047676c59226557412522635925d09647fbeb5f8099a95c",
      "signature": {
        "s": "0x4688047438bdbc9b3e44ca06a03f4502aac39b6781014d59a231e95b2ade097a",
        "r": "0x0fc7d8f903f1a50eb5c81b8061862a6b2700dd776523489cb5a892b657e71743",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "98465588",
    "total": "98465588"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "98465588",
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
            "amount": "45429730616"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "98465"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkNmRkOGIyZC05NzUyLTVhZmYtYmJmZC03OTczNzU1Njc2YWQifQ==",
    "nonce": 6826,
    "balances": {
      "current": "12972243933264456",
      "previous": "12972244031828509"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc6a69ed0dcff3a1e40ea8d965ec6a69ee081d532",
    "nonce": 22,
    "balances": {
      "current": "98465588",
      "previous": "0"
    }
  },
  "blockNumber": "10114716",
  "created": "2020-05-22T08:51:59.092Z",
  "updated": "2020-05-22T08:51:59.157Z",
  "id": "5ec792afb0c6090011d5b1af"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000005de7734000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `98465588`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`