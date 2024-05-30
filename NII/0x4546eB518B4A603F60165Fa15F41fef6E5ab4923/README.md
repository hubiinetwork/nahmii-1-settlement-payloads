# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4546eB518B4A603F60165Fa15F41fef6E5ab4923`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000112bd4a7c011f0000000000000000000000000000000000000000000000000000068385d52b3e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000068385d52b3e0000000000000000000000000000000000000000000000000000b6c84f85e4039925a74a9d95772f9fa683831970bdd38d745c1633204e28178e8da64c2a5ebb7615ecbb93cc1246391f9fdf09ed670891287bfa4fc48e278ca5e1f87ceb41a95eddfebad4910689cc3cee78f517f87e3eda11b654a7ee3c5d1a494b3056da34000000000000000000000000000000000000000000000000000000000000001c9dadbbeb70948c30f971406750523c1f8d723ac2dd9d72164cd0b69470bea40856ffcec9e7e1bb99a37dc8e16652d5f062fc529c197759b97e6464cedd2e471630258d7cd9156caa9aa1390c54764de38d0feff893acae6f9925d33333604150000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074b60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abb3000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009c1b22e2d2ed33919f79000000000000000000000000000000000000000000009c1b22e2d972644990a500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000001aae2c5ee0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c475a6628e8a5225410000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694932596a59314f4745314f5330344e6a51354c54557a4d6d4574596a6c6c4d69316d4f5464684f444977593251345957516966513d3d000000000000000000000000000000000000000000000000000000000000002d0000000000000000000000004546eb518b4a603f60165fa15f41fef6e5ab4923000000000000000000000000000000000000000000000000000112bd4a7c011f00000000000000000000000000000000000000000000000000010c39c4a6d5e100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9925a74a9d95772f9fa683831970bdd38d745c1633204e28178e8da64c2a5ebb",
      "signature": {
        "s": "0x5eddfebad4910689cc3cee78f517f87e3eda11b654a7ee3c5d1a494b3056da34",
        "r": "0x7615ecbb93cc1246391f9fdf09ed670891287bfa4fc48e278ca5e1f87ceb41a9",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9dadbbeb70948c30f971406750523c1f8d723ac2dd9d72164cd0b69470bea408",
      "signature": {
        "s": "0x30258d7cd9156caa9aa1390c54764de38d0feff893acae6f9925d33333604150",
        "r": "0x56ffcec9e7e1bb99a37dc8e16652d5f062fc529c197759b97e6464cedd2e4716",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "7161955822398",
    "total": "200971443889155"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7161955822398",
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
            "amount": "27235871824508215240001"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7161955822"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2YjY1OGE1OS04NjQ5LTUzMmEtYjllMi1mOTdhODIwY2Q4YWQifQ==",
    "nonce": 109491,
    "balances": {
      "current": "737189747221113051651961",
      "previous": "737189747228282169430181"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4546eb518b4a603f60165fa15f41fef6e5ab4923",
    "nonce": 45,
    "balances": {
      "current": "302079184470303",
      "previous": "294917228647905"
    }
  },
  "blockNumber": "14709942",
  "created": "2022-05-04T08:48:23.354Z",
  "updated": "2022-05-04T08:48:23.481Z",
  "id": "62723dd77832e20011830a7c"
}
```
* *stageAmount*: `302079184470303`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000068385d52b3e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000068385d52b3e0000000000000000000000000000000000000000000000000000b6c84f85e4039925a74a9d95772f9fa683831970bdd38d745c1633204e28178e8da64c2a5ebb7615ecbb93cc1246391f9fdf09ed670891287bfa4fc48e278ca5e1f87ceb41a95eddfebad4910689cc3cee78f517f87e3eda11b654a7ee3c5d1a494b3056da34000000000000000000000000000000000000000000000000000000000000001c9dadbbeb70948c30f971406750523c1f8d723ac2dd9d72164cd0b69470bea40856ffcec9e7e1bb99a37dc8e16652d5f062fc529c197759b97e6464cedd2e471630258d7cd9156caa9aa1390c54764de38d0feff893acae6f9925d33333604150000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074b60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abb3000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009c1b22e2d2ed33919f79000000000000000000000000000000000000000000009c1b22e2d972644990a500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000001aae2c5ee0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c475a6628e8a5225410000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694932596a59314f4745314f5330344e6a51354c54557a4d6d4574596a6c6c4d69316d4f5464684f444977593251345957516966513d3d000000000000000000000000000000000000000000000000000000000000002d0000000000000000000000004546eb518b4a603f60165fa15f41fef6e5ab4923000000000000000000000000000000000000000000000000000112bd4a7c011f00000000000000000000000000000000000000000000000000010c39c4a6d5e100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9925a74a9d95772f9fa683831970bdd38d745c1633204e28178e8da64c2a5ebb",
      "signature": {
        "s": "0x5eddfebad4910689cc3cee78f517f87e3eda11b654a7ee3c5d1a494b3056da34",
        "r": "0x7615ecbb93cc1246391f9fdf09ed670891287bfa4fc48e278ca5e1f87ceb41a9",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9dadbbeb70948c30f971406750523c1f8d723ac2dd9d72164cd0b69470bea408",
      "signature": {
        "s": "0x30258d7cd9156caa9aa1390c54764de38d0feff893acae6f9925d33333604150",
        "r": "0x56ffcec9e7e1bb99a37dc8e16652d5f062fc529c197759b97e6464cedd2e4716",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "7161955822398",
    "total": "200971443889155"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7161955822398",
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
            "amount": "27235871824508215240001"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7161955822"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2YjY1OGE1OS04NjQ5LTUzMmEtYjllMi1mOTdhODIwY2Q4YWQifQ==",
    "nonce": 109491,
    "balances": {
      "current": "737189747221113051651961",
      "previous": "737189747228282169430181"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4546eb518b4a603f60165fa15f41fef6e5ab4923",
    "nonce": 45,
    "balances": {
      "current": "302079184470303",
      "previous": "294917228647905"
    }
  },
  "blockNumber": "14709942",
  "created": "2022-05-04T08:48:23.354Z",
  "updated": "2022-05-04T08:48:23.481Z",
  "id": "62723dd77832e20011830a7c"
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
0x0f200f9b000000000000000000000000000000000000000000000000000112bd4a7c011f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `302079184470303`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`