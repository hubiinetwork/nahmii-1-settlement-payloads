# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xE70360ba351F900a82ACaf7bd837A6E112c5c389`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000303d27c0b69284800000000000000000000000000000000000000000000000000124c8d559206a50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000124c8d559206a500000000000000000000000000000000000000000000000002017d1618946b268a97720f1216b8d8200c3c20a654eddeacedbe8000686cf795c098435a605e3de62e4acfcffa7f56bcaa182eabe415ca5db50dd2bb3986722ce5fa15f330a93459c177f4ddca5ecf3d4595dbe69e909ecd27d1380d30aa78e89e89917da2ab54000000000000000000000000000000000000000000000000000000000000001b02e81751535accc00c17a0293bd6a70e6b594537e898db0a82bbc0d4d6b3b8ae3e1e692e0c8ff6712c899c3ffad589930e9717f019f863858f63ddc22a3008552065409324a9fb9c11bb8862c9d755197e5ed7f4175270d5c2bfb6225e4df31b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abe3000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009c1817cbe3e30db52564000000000000000000000000000000000000000000009c1817de351fa21565e500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000004af3ece39dc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4766da1f6e4e465370000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d6d45324f4445795a69316b4e475a684c5455344f475174596a41795a4330344f4759774e5442684d4759774f44636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000e70360ba351f900a82acaf7bd837a6e112c5c3890000000000000000000000000000000000000000000000000303d27c0b69284800000000000000000000000000000000000000000000000002f185eeb5d721a300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8a97720f1216b8d8200c3c20a654eddeacedbe8000686cf795c098435a605e3d",
      "signature": {
        "s": "0x59c177f4ddca5ecf3d4595dbe69e909ecd27d1380d30aa78e89e89917da2ab54",
        "r": "0xe62e4acfcffa7f56bcaa182eabe415ca5db50dd2bb3986722ce5fa15f330a934",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x02e81751535accc00c17a0293bd6a70e6b594537e898db0a82bbc0d4d6b3b8ae",
      "signature": {
        "s": "0x2065409324a9fb9c11bb8862c9d755197e5ed7f4175270d5c2bfb6225e4df31b",
        "r": "0x3e1e692e0c8ff6712c899c3ffad589930e9717f019f863858f63ddc22a300855",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5150719490524837",
    "total": "144534196907698982"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5150719490524837",
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
            "amount": "27235927907746009343287"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5150719490524"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0MmE2ODEyZi1kNGZhLTU4OGQtYjAyZC04OGYwNTBhMGYwODcifQ==",
    "nonce": 109539,
    "balances": {
      "current": "737133607900081154237796",
      "previous": "737133613055951364253157"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe70360ba351f900a82acaf7bd837a6e112c5c389",
    "nonce": 46,
    "balances": {
      "current": "217248637253134408",
      "previous": "212097917762609571"
    }
  },
  "blockNumber": "14709943",
  "created": "2022-05-04T08:48:37.301Z",
  "updated": "2022-05-04T08:48:37.400Z",
  "id": "62723de5bbd75600116d0431"
}
```
* *stageAmount*: `217248637253134408`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000124c8d559206a50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000124c8d559206a500000000000000000000000000000000000000000000000002017d1618946b268a97720f1216b8d8200c3c20a654eddeacedbe8000686cf795c098435a605e3de62e4acfcffa7f56bcaa182eabe415ca5db50dd2bb3986722ce5fa15f330a93459c177f4ddca5ecf3d4595dbe69e909ecd27d1380d30aa78e89e89917da2ab54000000000000000000000000000000000000000000000000000000000000001b02e81751535accc00c17a0293bd6a70e6b594537e898db0a82bbc0d4d6b3b8ae3e1e692e0c8ff6712c899c3ffad589930e9717f019f863858f63ddc22a3008552065409324a9fb9c11bb8862c9d755197e5ed7f4175270d5c2bfb6225e4df31b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abe3000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009c1817cbe3e30db52564000000000000000000000000000000000000000000009c1817de351fa21565e500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000004af3ece39dc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4766da1f6e4e465370000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d6d45324f4445795a69316b4e475a684c5455344f475174596a41795a4330344f4759774e5442684d4759774f44636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000e70360ba351f900a82acaf7bd837a6e112c5c3890000000000000000000000000000000000000000000000000303d27c0b69284800000000000000000000000000000000000000000000000002f185eeb5d721a300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8a97720f1216b8d8200c3c20a654eddeacedbe8000686cf795c098435a605e3d",
      "signature": {
        "s": "0x59c177f4ddca5ecf3d4595dbe69e909ecd27d1380d30aa78e89e89917da2ab54",
        "r": "0xe62e4acfcffa7f56bcaa182eabe415ca5db50dd2bb3986722ce5fa15f330a934",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x02e81751535accc00c17a0293bd6a70e6b594537e898db0a82bbc0d4d6b3b8ae",
      "signature": {
        "s": "0x2065409324a9fb9c11bb8862c9d755197e5ed7f4175270d5c2bfb6225e4df31b",
        "r": "0x3e1e692e0c8ff6712c899c3ffad589930e9717f019f863858f63ddc22a300855",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5150719490524837",
    "total": "144534196907698982"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5150719490524837",
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
            "amount": "27235927907746009343287"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5150719490524"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0MmE2ODEyZi1kNGZhLTU4OGQtYjAyZC04OGYwNTBhMGYwODcifQ==",
    "nonce": 109539,
    "balances": {
      "current": "737133607900081154237796",
      "previous": "737133613055951364253157"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe70360ba351f900a82acaf7bd837a6e112c5c389",
    "nonce": 46,
    "balances": {
      "current": "217248637253134408",
      "previous": "212097917762609571"
    }
  },
  "blockNumber": "14709943",
  "created": "2022-05-04T08:48:37.301Z",
  "updated": "2022-05-04T08:48:37.400Z",
  "id": "62723de5bbd75600116d0431"
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
0x0f200f9b0000000000000000000000000000000000000000000000000303d27c0b6928480000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `217248637253134408`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`