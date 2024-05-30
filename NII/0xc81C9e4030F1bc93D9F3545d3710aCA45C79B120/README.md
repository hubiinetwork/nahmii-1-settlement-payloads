# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xc81C9e4030F1bc93D9F3545d3710aCA45C79B120`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000414cc1532ec41431580000000000000000000000000000000000000000000000018c55dac4d1832e510000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000018c55dac4d1832e5100000000000000000000000000000000000000000000002b718e4a27a821f0bae64c8257d44c5f47f36885be3a2547e88a4306bdad20d74c5f538c75021c1d51972feb040cc952472b63cf073426c23676a57e89c5bf181ed55ff50f3c88f2b223a2b34e45ec3fba64ff46c422c9f3414446d3d1543db093d77a0f84ee3bb9f4000000000000000000000000000000000000000000000000000000000000001c6236b392f11d87d0e80b568382144f9025168bf30d4110d603721a36164a44ddce3aea1a3fef7425c43f82efa7ef381450204dd5286726e569d604eebbc46c8333a04ef39224f471226ad69dc2025fdf3e170190922d97d5f412f81f59eb33fd000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b67c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030b2481293db51e77a400000000000000000000000000000000000000000000030b3d4cde4dc3d39e4c500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000065763c19cf3c340000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dfedd0060a56a151a90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d324d785a4455335a6930334d546c6c4c54566b4e574d74596d59324e4330334e7a55304d6a6b334e4459334f44516966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000c81c9e4030f1bc93d9f3545d3710aca45c79b1200000000000000000000000000000000000000000000000414cc1532ec414315800000000000000000000000000000000000000000000003fc06b7869f291030700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe64c8257d44c5f47f36885be3a2547e88a4306bdad20d74c5f538c75021c1d51",
      "signature": {
        "s": "0x23a2b34e45ec3fba64ff46c422c9f3414446d3d1543db093d77a0f84ee3bb9f4",
        "r": "0x972feb040cc952472b63cf073426c23676a57e89c5bf181ed55ff50f3c88f2b2",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6236b392f11d87d0e80b568382144f9025168bf30d4110d603721a36164a44dd",
      "signature": {
        "s": "0x33a04ef39224f471226ad69dc2025fdf3e170190922d97d5f412f81f59eb33fd",
        "r": "0xce3aea1a3fef7425c43f82efa7ef381450204dd5286726e569d604eebbc46c83",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "28558973150903348817",
    "total": "801392554276674465978"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "28558973150903348817",
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
            "amount": "27742592546009073668521"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "28558973150903348"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0M2MxZDU3Zi03MTllLTVkNWMtYmY2NC03NzU0Mjk3NDY3ODQifQ==",
    "nonce": 112252,
    "balances": {
      "current": "229962304998753763293760",
      "previous": "229990892530877817545925"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc81c9e4030f1bc93d9f3545d3710aca45c79b120",
    "nonce": 46,
    "balances": {
      "current": "1204569158068831793496",
      "previous": "1176010184917928444679"
    }
  },
  "blockNumber": "14709990",
  "created": "2022-05-04T09:02:47.594Z",
  "updated": "2022-05-04T09:02:47.681Z",
  "id": "627241373592fd001130b74b"
}
```
* *stageAmount*: `1204569158068831793496`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000018c55dac4d1832e510000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000018c55dac4d1832e5100000000000000000000000000000000000000000000002b718e4a27a821f0bae64c8257d44c5f47f36885be3a2547e88a4306bdad20d74c5f538c75021c1d51972feb040cc952472b63cf073426c23676a57e89c5bf181ed55ff50f3c88f2b223a2b34e45ec3fba64ff46c422c9f3414446d3d1543db093d77a0f84ee3bb9f4000000000000000000000000000000000000000000000000000000000000001c6236b392f11d87d0e80b568382144f9025168bf30d4110d603721a36164a44ddce3aea1a3fef7425c43f82efa7ef381450204dd5286726e569d604eebbc46c8333a04ef39224f471226ad69dc2025fdf3e170190922d97d5f412f81f59eb33fd000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b67c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030b2481293db51e77a400000000000000000000000000000000000000000000030b3d4cde4dc3d39e4c500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000065763c19cf3c340000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dfedd0060a56a151a90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d324d785a4455335a6930334d546c6c4c54566b4e574d74596d59324e4330334e7a55304d6a6b334e4459334f44516966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000c81c9e4030f1bc93d9f3545d3710aca45c79b1200000000000000000000000000000000000000000000000414cc1532ec414315800000000000000000000000000000000000000000000003fc06b7869f291030700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe64c8257d44c5f47f36885be3a2547e88a4306bdad20d74c5f538c75021c1d51",
      "signature": {
        "s": "0x23a2b34e45ec3fba64ff46c422c9f3414446d3d1543db093d77a0f84ee3bb9f4",
        "r": "0x972feb040cc952472b63cf073426c23676a57e89c5bf181ed55ff50f3c88f2b2",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6236b392f11d87d0e80b568382144f9025168bf30d4110d603721a36164a44dd",
      "signature": {
        "s": "0x33a04ef39224f471226ad69dc2025fdf3e170190922d97d5f412f81f59eb33fd",
        "r": "0xce3aea1a3fef7425c43f82efa7ef381450204dd5286726e569d604eebbc46c83",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "28558973150903348817",
    "total": "801392554276674465978"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "28558973150903348817",
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
            "amount": "27742592546009073668521"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "28558973150903348"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0M2MxZDU3Zi03MTllLTVkNWMtYmY2NC03NzU0Mjk3NDY3ODQifQ==",
    "nonce": 112252,
    "balances": {
      "current": "229962304998753763293760",
      "previous": "229990892530877817545925"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc81c9e4030f1bc93d9f3545d3710aca45c79b120",
    "nonce": 46,
    "balances": {
      "current": "1204569158068831793496",
      "previous": "1176010184917928444679"
    }
  },
  "blockNumber": "14709990",
  "created": "2022-05-04T09:02:47.594Z",
  "updated": "2022-05-04T09:02:47.681Z",
  "id": "627241373592fd001130b74b"
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
0x0f200f9b0000000000000000000000000000000000000000000000414cc1532ec41431580000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1204569158068831793496`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`