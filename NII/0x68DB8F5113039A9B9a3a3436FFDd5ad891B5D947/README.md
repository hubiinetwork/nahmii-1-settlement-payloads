# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x68DB8F5113039A9B9a3a3436FFDd5ad891B5D947`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000002447160fcda97c9190000000000000000000000000000000000000000000000000dc2fb26d57f09f3b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000dc2fb26d57f09f3b00000000000000000000000000000000000000000000001822a4621607c690c400fb2b5ccebcde3b1cd0ba52bc728649f3f9954d4576bf9b0600fa277f60eeb60ce776cfee70b4182dafa7f9cc9b36066ab08fb7923e1a2523e675addd21ba3045226c399e748aac3ce80b7c23522495541a05d3922aba5a06171f4e964249fe000000000000000000000000000000000000000000000000000000000000001c3c4c70ccc327cb0329bf937ddcf35e5b8ec05ffe7fb0c8a56c6912974ca35bccd5a0af39d3fe6a9a559f5bf8aa453245cb26622071c112189cd45bfc5ae4b97e0335439aff8dea59fbdf49be44d084ccf358aa7ccd7de74d0101c797ee4790a3000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b713000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002f5fc0b79fe5b619e70f000000000000000000000000000000000000000000002f609d1fb07471b68a8b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000385e2163ac04410000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e04463adcbed29d5b80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e5455334d54426a5969307a5a5449774c54566a4d545974595455334e53316d4f574e6b4d32566a4e324e694d44596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000068db8f5113039a9b9a3a3436ffdd5ad891b5d94700000000000000000000000000000000000000000000002447160fcda97c91900000000000000000000000000000000000000000000000236ae65d60518bf25500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x00fb2b5ccebcde3b1cd0ba52bc728649f3f9954d4576bf9b0600fa277f60eeb6",
      "signature": {
        "s": "0x45226c399e748aac3ce80b7c23522495541a05d3922aba5a06171f4e964249fe",
        "r": "0x0ce776cfee70b4182dafa7f9cc9b36066ab08fb7923e1a2523e675addd21ba30",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3c4c70ccc327cb0329bf937ddcf35e5b8ec05ffe7fb0c8a56c6912974ca35bcc",
      "signature": {
        "s": "0x0335439aff8dea59fbdf49be44d084ccf358aa7ccd7de74d0101c797ee4790a3",
        "r": "0xd5a0af39d3fe6a9a559f5bf8aa453245cb26622071c112189cd45bfc5ae4b97e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15866096194946113339",
    "total": "445218085709258592452"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15866096194946113339",
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
            "amount": "27748831060367807993272"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15866096194946113"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4NTU3MTBjYi0zZTIwLTVjMTYtYTU3NS1mOWNkM2VjN2NiMDYifQ==",
    "nonce": 112403,
    "balances": {
      "current": "223717552125660704139023",
      "previous": "223733434087951845198475"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x68db8f5113039a9b9a3a3436ffdd5ad891b5d947",
    "nonce": 46,
    "balances": {
      "current": "669205085655710601616",
      "previous": "653338989460764488277"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:37.045Z",
  "updated": "2022-05-04T09:03:37.114Z",
  "id": "627241697832e20011830e44"
}
```
* *stageAmount*: `669205085655710601616`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000dc2fb26d57f09f3b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000dc2fb26d57f09f3b00000000000000000000000000000000000000000000001822a4621607c690c400fb2b5ccebcde3b1cd0ba52bc728649f3f9954d4576bf9b0600fa277f60eeb60ce776cfee70b4182dafa7f9cc9b36066ab08fb7923e1a2523e675addd21ba3045226c399e748aac3ce80b7c23522495541a05d3922aba5a06171f4e964249fe000000000000000000000000000000000000000000000000000000000000001c3c4c70ccc327cb0329bf937ddcf35e5b8ec05ffe7fb0c8a56c6912974ca35bccd5a0af39d3fe6a9a559f5bf8aa453245cb26622071c112189cd45bfc5ae4b97e0335439aff8dea59fbdf49be44d084ccf358aa7ccd7de74d0101c797ee4790a3000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b713000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002f5fc0b79fe5b619e70f000000000000000000000000000000000000000000002f609d1fb07471b68a8b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000385e2163ac04410000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e04463adcbed29d5b80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e5455334d54426a5969307a5a5449774c54566a4d545974595455334e53316d4f574e6b4d32566a4e324e694d44596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000068db8f5113039a9b9a3a3436ffdd5ad891b5d94700000000000000000000000000000000000000000000002447160fcda97c91900000000000000000000000000000000000000000000000236ae65d60518bf25500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x00fb2b5ccebcde3b1cd0ba52bc728649f3f9954d4576bf9b0600fa277f60eeb6",
      "signature": {
        "s": "0x45226c399e748aac3ce80b7c23522495541a05d3922aba5a06171f4e964249fe",
        "r": "0x0ce776cfee70b4182dafa7f9cc9b36066ab08fb7923e1a2523e675addd21ba30",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3c4c70ccc327cb0329bf937ddcf35e5b8ec05ffe7fb0c8a56c6912974ca35bcc",
      "signature": {
        "s": "0x0335439aff8dea59fbdf49be44d084ccf358aa7ccd7de74d0101c797ee4790a3",
        "r": "0xd5a0af39d3fe6a9a559f5bf8aa453245cb26622071c112189cd45bfc5ae4b97e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15866096194946113339",
    "total": "445218085709258592452"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15866096194946113339",
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
            "amount": "27748831060367807993272"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15866096194946113"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4NTU3MTBjYi0zZTIwLTVjMTYtYTU3NS1mOWNkM2VjN2NiMDYifQ==",
    "nonce": 112403,
    "balances": {
      "current": "223717552125660704139023",
      "previous": "223733434087951845198475"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x68db8f5113039a9b9a3a3436ffdd5ad891b5d947",
    "nonce": 46,
    "balances": {
      "current": "669205085655710601616",
      "previous": "653338989460764488277"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:37.045Z",
  "updated": "2022-05-04T09:03:37.114Z",
  "id": "627241697832e20011830e44"
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
0x0f200f9b00000000000000000000000000000000000000000000002447160fcda97c91900000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `669205085655710601616`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`