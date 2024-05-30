# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x29bCe4a9144f6dffd87181808fAda2216588295b`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000088b3dbc8c3470fe30000000000000000000000000000000000000000000000000a94785889cee9fd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000a94785889cee9fd00000000000000000000000000000000000000000000000088b3dbc8c3470fe3c98ff69edf65deb5017db97f1360b3eeee6861b2b14afb67ff49f69dc9edf9ab88c3bbd96964e1bfa35a67f8041442d9fa56b229b543c74f3549e9e59cb82c8f6f23b285ba1305317d3367241f7a279b856b395c045050fe285240ba16789d3d000000000000000000000000000000000000000000000000000000000000001c109ec72f5a07bfd48533e02f3dab619eaf8d6efda68631d6d5d1e25856c4ac39203b79302f2d93ff35fabeea19918ec99ad69abe932375e72e93f015bee0ff3d0db2255fb8636c2da3e40f5484dffa6d53bd85c7f48dad48a82e60cdd2760d4d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b507000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000035360af830e7768b897d000000000000000000000000000000000000000000003536158f5e9e4c4462d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000002b55e4be9ef560000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dec63bb7e1a9b5df8a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d4759304d574d354d533077595745774c54566c4f54557459574934596931685a54646a5a57466d596a45794d474d6966513d3d000000000000000000000000000000000000000000000000000000000000000d00000000000000000000000029bce4a9144f6dffd87181808fada2216588295b00000000000000000000000000000000000000000000000088b3dbc8c3470fe30000000000000000000000000000000000000000000000007e1f6370397825e600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc98ff69edf65deb5017db97f1360b3eeee6861b2b14afb67ff49f69dc9edf9ab",
      "signature": {
        "s": "0x6f23b285ba1305317d3367241f7a279b856b395c045050fe285240ba16789d3d",
        "r": "0x88c3bbd96964e1bfa35a67f8041442d9fa56b229b543c74f3549e9e59cb82c8f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x109ec72f5a07bfd48533e02f3dab619eaf8d6efda68631d6d5d1e25856c4ac39",
      "signature": {
        "s": "0x0db2255fb8636c2da3e40f5484dffa6d53bd85c7f48dad48a82e60cdd2760d4d",
        "r": "0x203b79302f2d93ff35fabeea19918ec99ad69abe932375e72e93f015bee0ff3d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "762366558596950525",
    "total": "9850458465305563107"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "762366558596950525",
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
            "amount": "27721293811534724980618"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "762366558596950"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxMGY0MWM5MS0wYWEwLTVlOTUtYWI4Yi1hZTdjZWFmYjEyMGMifQ==",
    "nonce": 111879,
    "balances": {
      "current": "251282338207576800070013",
      "previous": "251283101336501955617488"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x29bce4a9144f6dffd87181808fada2216588295b",
    "nonce": 13,
    "balances": {
      "current": "9850458465305563107",
      "previous": "9088091906708612582"
    }
  },
  "blockNumber": "14709984",
  "created": "2022-05-04T09:00:46.752Z",
  "updated": "2022-05-04T09:00:46.852Z",
  "id": "627240be3592fd001130b6cb"
}
```
* *stageAmount*: `9850458465305563107`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000a94785889cee9fd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000a94785889cee9fd00000000000000000000000000000000000000000000000088b3dbc8c3470fe3c98ff69edf65deb5017db97f1360b3eeee6861b2b14afb67ff49f69dc9edf9ab88c3bbd96964e1bfa35a67f8041442d9fa56b229b543c74f3549e9e59cb82c8f6f23b285ba1305317d3367241f7a279b856b395c045050fe285240ba16789d3d000000000000000000000000000000000000000000000000000000000000001c109ec72f5a07bfd48533e02f3dab619eaf8d6efda68631d6d5d1e25856c4ac39203b79302f2d93ff35fabeea19918ec99ad69abe932375e72e93f015bee0ff3d0db2255fb8636c2da3e40f5484dffa6d53bd85c7f48dad48a82e60cdd2760d4d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b507000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000035360af830e7768b897d000000000000000000000000000000000000000000003536158f5e9e4c4462d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000002b55e4be9ef560000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dec63bb7e1a9b5df8a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d4759304d574d354d533077595745774c54566c4f54557459574934596931685a54646a5a57466d596a45794d474d6966513d3d000000000000000000000000000000000000000000000000000000000000000d00000000000000000000000029bce4a9144f6dffd87181808fada2216588295b00000000000000000000000000000000000000000000000088b3dbc8c3470fe30000000000000000000000000000000000000000000000007e1f6370397825e600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc98ff69edf65deb5017db97f1360b3eeee6861b2b14afb67ff49f69dc9edf9ab",
      "signature": {
        "s": "0x6f23b285ba1305317d3367241f7a279b856b395c045050fe285240ba16789d3d",
        "r": "0x88c3bbd96964e1bfa35a67f8041442d9fa56b229b543c74f3549e9e59cb82c8f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x109ec72f5a07bfd48533e02f3dab619eaf8d6efda68631d6d5d1e25856c4ac39",
      "signature": {
        "s": "0x0db2255fb8636c2da3e40f5484dffa6d53bd85c7f48dad48a82e60cdd2760d4d",
        "r": "0x203b79302f2d93ff35fabeea19918ec99ad69abe932375e72e93f015bee0ff3d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "762366558596950525",
    "total": "9850458465305563107"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "762366558596950525",
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
            "amount": "27721293811534724980618"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "762366558596950"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxMGY0MWM5MS0wYWEwLTVlOTUtYWI4Yi1hZTdjZWFmYjEyMGMifQ==",
    "nonce": 111879,
    "balances": {
      "current": "251282338207576800070013",
      "previous": "251283101336501955617488"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x29bce4a9144f6dffd87181808fada2216588295b",
    "nonce": 13,
    "balances": {
      "current": "9850458465305563107",
      "previous": "9088091906708612582"
    }
  },
  "blockNumber": "14709984",
  "created": "2022-05-04T09:00:46.752Z",
  "updated": "2022-05-04T09:00:46.852Z",
  "id": "627240be3592fd001130b6cb"
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
0x0f200f9b00000000000000000000000000000000000000000000000088b3dbc8c3470fe30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `9850458465305563107`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`