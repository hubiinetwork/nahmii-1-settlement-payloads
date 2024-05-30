# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1687e425fC02446c84eff7b491f8856bE1FeD9a6`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000e2328f6030d284db270000000000000000000000000000000000000000000000000000002c11adde070000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000002c11adde07000000000000000000000000000000000000000000000074ae23146d122024f2266a39d2a38c38f5a20c53cd513686ece7290664bf8b7118d5774f13e3d2ffb2f7ad5ea57b502f92517d975a26db5206606f0480b0b2bd0f5101fd3dbeebcab1028df34401017981fce890e9b9c015e9791d72ba37d299447e7b8c50dbc6d167000000000000000000000000000000000000000000000000000000000000001cea5fc9aa9fbb0e919fd47ac8a7c7537b2a3585832a60ee1b7aa3f3cc62c23137fffcea9216e8c4bbbd0574eab6171b0793b9c17818dd6e5d07581892f68f20ed18568da002d807c86838116a65cec882c2ad215d7df73eabc0b78a3a2199db59000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af45000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000074d6608da1f2cf4707d50000000000000000000000000000000000000000000074d6608da21eec3d01fc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000b481c200000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ce8095d8c2736770880000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5932466d5954466d4f4330344f5451304c5455774e546374596d56684d6930324d544934595749324e444a6a4d32596966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000001687e425fc02446c84eff7b491f8856be1fed9a60000000000000000000000000000000000000000000000e2328f6030d284db270000000000000000000000000000000000000000000000e2328f6004c0d6fd2000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x266a39d2a38c38f5a20c53cd513686ece7290664bf8b7118d5774f13e3d2ffb2",
      "signature": {
        "s": "0x028df34401017981fce890e9b9c015e9791d72ba37d299447e7b8c50dbc6d167",
        "r": "0xf7ad5ea57b502f92517d975a26db5206606f0480b0b2bd0f5101fd3dbeebcab1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xea5fc9aa9fbb0e919fd47ac8a7c7537b2a3585832a60ee1b7aa3f3cc62c23137",
      "signature": {
        "s": "0x18568da002d807c86838116a65cec882c2ad215d7df73eabc0b78a3a2199db59",
        "r": "0xfffcea9216e8c4bbbd0574eab6171b0793b9c17818dd6e5d07581892f68f20ed",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "189275168263",
    "total": "2152370207995780408562"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "189275168263",
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
            "amount": "27421127243670449778824"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "189275168"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzY2FmYTFmOC04OTQ0LTUwNTctYmVhMi02MTI4YWI2NDJjM2YifQ==",
    "nonce": 110405,
    "balances": {
      "current": "551749072639716277815253",
      "previous": "551749072639905742258684"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1687e425fc02446c84eff7b491f8856be1fed9a6",
    "nonce": 46,
    "balances": {
      "current": "4172607397044731304743",
      "previous": "4172607396855456136480"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:53:07.220Z",
  "updated": "2022-05-04T08:53:07.284Z",
  "id": "62723ef37832e20011830ba9"
}
```
* *stageAmount*: `4172607397044731304743`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000002c11adde070000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000002c11adde07000000000000000000000000000000000000000000000074ae23146d122024f2266a39d2a38c38f5a20c53cd513686ece7290664bf8b7118d5774f13e3d2ffb2f7ad5ea57b502f92517d975a26db5206606f0480b0b2bd0f5101fd3dbeebcab1028df34401017981fce890e9b9c015e9791d72ba37d299447e7b8c50dbc6d167000000000000000000000000000000000000000000000000000000000000001cea5fc9aa9fbb0e919fd47ac8a7c7537b2a3585832a60ee1b7aa3f3cc62c23137fffcea9216e8c4bbbd0574eab6171b0793b9c17818dd6e5d07581892f68f20ed18568da002d807c86838116a65cec882c2ad215d7df73eabc0b78a3a2199db59000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af45000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000074d6608da1f2cf4707d50000000000000000000000000000000000000000000074d6608da21eec3d01fc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000b481c200000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ce8095d8c2736770880000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5932466d5954466d4f4330344f5451304c5455774e546374596d56684d6930324d544934595749324e444a6a4d32596966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000001687e425fc02446c84eff7b491f8856be1fed9a60000000000000000000000000000000000000000000000e2328f6030d284db270000000000000000000000000000000000000000000000e2328f6004c0d6fd2000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x266a39d2a38c38f5a20c53cd513686ece7290664bf8b7118d5774f13e3d2ffb2",
      "signature": {
        "s": "0x028df34401017981fce890e9b9c015e9791d72ba37d299447e7b8c50dbc6d167",
        "r": "0xf7ad5ea57b502f92517d975a26db5206606f0480b0b2bd0f5101fd3dbeebcab1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xea5fc9aa9fbb0e919fd47ac8a7c7537b2a3585832a60ee1b7aa3f3cc62c23137",
      "signature": {
        "s": "0x18568da002d807c86838116a65cec882c2ad215d7df73eabc0b78a3a2199db59",
        "r": "0xfffcea9216e8c4bbbd0574eab6171b0793b9c17818dd6e5d07581892f68f20ed",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "189275168263",
    "total": "2152370207995780408562"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "189275168263",
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
            "amount": "27421127243670449778824"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "189275168"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzY2FmYTFmOC04OTQ0LTUwNTctYmVhMi02MTI4YWI2NDJjM2YifQ==",
    "nonce": 110405,
    "balances": {
      "current": "551749072639716277815253",
      "previous": "551749072639905742258684"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1687e425fc02446c84eff7b491f8856be1fed9a6",
    "nonce": 46,
    "balances": {
      "current": "4172607397044731304743",
      "previous": "4172607396855456136480"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:53:07.220Z",
  "updated": "2022-05-04T08:53:07.284Z",
  "id": "62723ef37832e20011830ba9"
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
0x0f200f9b0000000000000000000000000000000000000000000000e2328f6030d284db270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4172607397044731304743`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`