# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x21B4801553c9c1cE21d55E4dC00e40cc77fEcF53`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000070312d000000000000000000000000000000000000000000000000000000000070312d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000070312d000000000000000000000000000000000000000000000000000000000070312d91d84af2e12022fdbfa82e1f1ad9177a9da7af5ffa7c2da15009539336b491f9b9892ecac6895faf329e8b85d83123293235e76374361213f7a7349c69c91e010e3c26c980cab979e26cce7f1108f14d0ef07ec7294f3da56d28f70c22cb0fc2000000000000000000000000000000000000000000000000000000000000001c7f3ef6428803d7a004ef7e60171639d89ae071e1190bb327a7f5769ff9b84c57cf660469a4443f61a3f5b273a7e56c4710f9acd51ff204286101b9581509b31e583388cfa46bd81db4e86a1c4bf97afa6389ddbad5dadf190c401bf5f2e6b690000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56850000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000183b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ad6812fbc17000000000000000000000000000000000000000000000000002e1ad681a009fc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000001cb8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000963557786000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d445577596a6c684d6930324e5456694c5455784d446374596d45355953316d4d7a51314f474d79593249324e57516966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000021b4801553c9c1ce21d55e4dc00e40cc77fecf53000000000000000000000000000000000000000000000000000000000070312d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x91d84af2e12022fdbfa82e1f1ad9177a9da7af5ffa7c2da15009539336b491f9",
      "signature": {
        "s": "0x0e3c26c980cab979e26cce7f1108f14d0ef07ec7294f3da56d28f70c22cb0fc2",
        "r": "0xb9892ecac6895faf329e8b85d83123293235e76374361213f7a7349c69c91e01",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x7f3ef6428803d7a004ef7e60171639d89ae071e1190bb327a7f5769ff9b84c57",
      "signature": {
        "s": "0x583388cfa46bd81db4e86a1c4bf97afa6389ddbad5dadf190c401bf5f2e6b690",
        "r": "0xcf660469a4443f61a3f5b273a7e56c4710f9acd51ff204286101b9581509b31e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7352621",
    "total": "7352621"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7352621",
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
            "amount": "40321251206"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "7352"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMDUwYjlhMi02NTViLTUxMDctYmE5YS1mMzQ1OGMyY2I2NWQifQ==",
    "nonce": 6203,
    "balances": {
      "current": "12977357521402903",
      "previous": "12977357528762876"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x21b4801553c9c1ce21d55e4dc00e40cc77fecf53",
    "nonce": 22,
    "balances": {
      "current": "7352621",
      "previous": "0"
    }
  },
  "blockNumber": "10114693",
  "created": "2020-05-22T08:47:18.731Z",
  "updated": "2020-05-22T08:47:18.798Z",
  "id": "5ec79196b0c6090011d5b0dd"
}
```
* *stageAmount*: `7352621`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000070312d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000070312d000000000000000000000000000000000000000000000000000000000070312d91d84af2e12022fdbfa82e1f1ad9177a9da7af5ffa7c2da15009539336b491f9b9892ecac6895faf329e8b85d83123293235e76374361213f7a7349c69c91e010e3c26c980cab979e26cce7f1108f14d0ef07ec7294f3da56d28f70c22cb0fc2000000000000000000000000000000000000000000000000000000000000001c7f3ef6428803d7a004ef7e60171639d89ae071e1190bb327a7f5769ff9b84c57cf660469a4443f61a3f5b273a7e56c4710f9acd51ff204286101b9581509b31e583388cfa46bd81db4e86a1c4bf97afa6389ddbad5dadf190c401bf5f2e6b690000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56850000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000183b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ad6812fbc17000000000000000000000000000000000000000000000000002e1ad681a009fc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000001cb8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000963557786000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d445577596a6c684d6930324e5456694c5455784d446374596d45355953316d4d7a51314f474d79593249324e57516966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000021b4801553c9c1ce21d55e4dc00e40cc77fecf53000000000000000000000000000000000000000000000000000000000070312d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x91d84af2e12022fdbfa82e1f1ad9177a9da7af5ffa7c2da15009539336b491f9",
      "signature": {
        "s": "0x0e3c26c980cab979e26cce7f1108f14d0ef07ec7294f3da56d28f70c22cb0fc2",
        "r": "0xb9892ecac6895faf329e8b85d83123293235e76374361213f7a7349c69c91e01",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x7f3ef6428803d7a004ef7e60171639d89ae071e1190bb327a7f5769ff9b84c57",
      "signature": {
        "s": "0x583388cfa46bd81db4e86a1c4bf97afa6389ddbad5dadf190c401bf5f2e6b690",
        "r": "0xcf660469a4443f61a3f5b273a7e56c4710f9acd51ff204286101b9581509b31e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7352621",
    "total": "7352621"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7352621",
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
            "amount": "40321251206"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "7352"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMDUwYjlhMi02NTViLTUxMDctYmE5YS1mMzQ1OGMyY2I2NWQifQ==",
    "nonce": 6203,
    "balances": {
      "current": "12977357521402903",
      "previous": "12977357528762876"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x21b4801553c9c1ce21d55e4dc00e40cc77fecf53",
    "nonce": 22,
    "balances": {
      "current": "7352621",
      "previous": "0"
    }
  },
  "blockNumber": "10114693",
  "created": "2020-05-22T08:47:18.731Z",
  "updated": "2020-05-22T08:47:18.798Z",
  "id": "5ec79196b0c6090011d5b0dd"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000070312d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `7352621`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`