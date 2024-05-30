# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe41B5E6d7328eb3a519EFe0eD8D63c8D1E63AcF5`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000c2bb2735b60fcec6700000000000000000000000000000000000000000000000008b358ada4d9a18e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000008b358ada4d9a18e00000000000000000000000000000000000000000000000c2bb2735b60fcec6790e27e2ae6e78871ea51c6585a9b09bdf39b1d1d757deaee8583245730836eaa4cde21f91d5ac1afa5d1e92da9a15fe0706bc8d5a05b914ddfe0029ab8fe04a42f39b006146f63fccbbe118ee3e3eaf882ec244682730a4632a53788bd6aade5000000000000000000000000000000000000000000000000000000000000001bf5bffd80adc44859d8632d39cd9b94d088b76a643f277a8b56761eac8d490bc3eb07f6986690d93544c9d4a3950af083de56d51ef70f12b734b673aaf09d8e177e9da89ee183acb5428d55649436da170423db6715e1cfda0ed03bcec16415ce000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074df0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b4d6000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000361ca8a1aa7c13dcdb3b00000000000000000000000000000000000000000000361cb1573d5d185d9df800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000023a335fa7212f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005de8b412ce412688ebd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d7a466b4e44686d5a6930794e44426b4c54557a5a5459744f5759305969316a4e7a49314e54686b4e6d4d354d546b6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e41b5e6d7328eb3a519efe0ed8d63c8d1e63acf500000000000000000000000000000000000000000000000c2bb2735b60fcec6700000000000000000000000000000000000000000000000c22ff1aadbc234ad900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x90e27e2ae6e78871ea51c6585a9b09bdf39b1d1d757deaee8583245730836eaa",
      "signature": {
        "s": "0x2f39b006146f63fccbbe118ee3e3eaf882ec244682730a4632a53788bd6aade5",
        "r": "0x4cde21f91d5ac1afa5d1e92da9a15fe0706bc8d5a05b914ddfe0029ab8fe04a4",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf5bffd80adc44859d8632d39cd9b94d088b76a643f277a8b56761eac8d490bc3",
      "signature": {
        "s": "0x7e9da89ee183acb5428d55649436da170423db6715e1cfda0ed03bcec16415ce",
        "r": "0xeb07f6986690d93544c9d4a3950af083de56d51ef70f12b734b673aaf09d8e17",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "626942275952943502",
    "total": "224509634810306423911"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "626942275952943502",
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
            "amount": "27717043949514577710781"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "626942275952943"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0MzFkNDhmZi0yNDBkLTUzZTYtOWY0Yi1jNzI1NThkNmM5MTkifQ==",
    "nonce": 111830,
    "balances": {
      "current": "255536450089744217201467",
      "previous": "255537077658962446097912"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe41b5e6d7328eb3a519efe0ed8d63c8d1e63acf5",
    "nonce": 22,
    "balances": {
      "current": "224509634810306423911",
      "previous": "223882692534353480409"
    }
  },
  "blockNumber": "14709983",
  "created": "2022-05-04T09:00:28.307Z",
  "updated": "2022-05-04T09:00:28.400Z",
  "id": "627240ac3592fd001130b6b6"
}
```
* *stageAmount*: `224509634810306423911`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000008b358ada4d9a18e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000008b358ada4d9a18e00000000000000000000000000000000000000000000000c2bb2735b60fcec6790e27e2ae6e78871ea51c6585a9b09bdf39b1d1d757deaee8583245730836eaa4cde21f91d5ac1afa5d1e92da9a15fe0706bc8d5a05b914ddfe0029ab8fe04a42f39b006146f63fccbbe118ee3e3eaf882ec244682730a4632a53788bd6aade5000000000000000000000000000000000000000000000000000000000000001bf5bffd80adc44859d8632d39cd9b94d088b76a643f277a8b56761eac8d490bc3eb07f6986690d93544c9d4a3950af083de56d51ef70f12b734b673aaf09d8e177e9da89ee183acb5428d55649436da170423db6715e1cfda0ed03bcec16415ce000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074df0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b4d6000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000361ca8a1aa7c13dcdb3b00000000000000000000000000000000000000000000361cb1573d5d185d9df800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000023a335fa7212f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005de8b412ce412688ebd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d7a466b4e44686d5a6930794e44426b4c54557a5a5459744f5759305969316a4e7a49314e54686b4e6d4d354d546b6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e41b5e6d7328eb3a519efe0ed8d63c8d1e63acf500000000000000000000000000000000000000000000000c2bb2735b60fcec6700000000000000000000000000000000000000000000000c22ff1aadbc234ad900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x90e27e2ae6e78871ea51c6585a9b09bdf39b1d1d757deaee8583245730836eaa",
      "signature": {
        "s": "0x2f39b006146f63fccbbe118ee3e3eaf882ec244682730a4632a53788bd6aade5",
        "r": "0x4cde21f91d5ac1afa5d1e92da9a15fe0706bc8d5a05b914ddfe0029ab8fe04a4",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf5bffd80adc44859d8632d39cd9b94d088b76a643f277a8b56761eac8d490bc3",
      "signature": {
        "s": "0x7e9da89ee183acb5428d55649436da170423db6715e1cfda0ed03bcec16415ce",
        "r": "0xeb07f6986690d93544c9d4a3950af083de56d51ef70f12b734b673aaf09d8e17",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "626942275952943502",
    "total": "224509634810306423911"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "626942275952943502",
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
            "amount": "27717043949514577710781"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "626942275952943"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0MzFkNDhmZi0yNDBkLTUzZTYtOWY0Yi1jNzI1NThkNmM5MTkifQ==",
    "nonce": 111830,
    "balances": {
      "current": "255536450089744217201467",
      "previous": "255537077658962446097912"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe41b5e6d7328eb3a519efe0ed8d63c8d1e63acf5",
    "nonce": 22,
    "balances": {
      "current": "224509634810306423911",
      "previous": "223882692534353480409"
    }
  },
  "blockNumber": "14709983",
  "created": "2022-05-04T09:00:28.307Z",
  "updated": "2022-05-04T09:00:28.400Z",
  "id": "627240ac3592fd001130b6b6"
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
0x0f200f9b00000000000000000000000000000000000000000000000c2bb2735b60fcec670000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `224509634810306423911`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`