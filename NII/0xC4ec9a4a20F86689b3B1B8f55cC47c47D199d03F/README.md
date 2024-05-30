# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xC4ec9a4a20F86689b3B1B8f55cC47c47D199d03F`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000ae2203cab041de7ab000000000000000000000000000000000000000000000000420e4f20cd9c04bc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000420e4f20cd9c04bc0000000000000000000000000000000000000000000000073d97b7069cb16734bca32d7d776604fff6275af355a92e53651da47b7545b2b2a5ccf2b175cf589b8eefc6b3d7269e184fba73e89a5752a63978a637af57c01137b71936b9d5cd8952245eaafa1a9c40cab1d19ae65d07d9a545dcd9501adbf094bc1f434dba9de7000000000000000000000000000000000000000000000000000000000000001beaa47bc6aeba1b19e3a70586db78fe329878d68728d7bd45f8cc76c18cd417e2bc48f5ea4ac70bc265d00002d217f2c6399400ed8808aae6441cf052bb647e1767b4c40ce7b1aaf22c50b12860c0c98b8b671b71aa738c54831c7a0942595df4000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074be0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001acd5000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000984e7aeb5a814ffe1d4600000000000000000000000000000000000000000000984ebd0a92ac21e7584800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000010e90a044d36460000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c56e66b236ac0cfbe80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a69597a4a684d6a59314e7930775a6d4d794c545578595441744f446b305a53307a5932466d4d574d774d32566c4e7a596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000c4ec9a4a20f86689b3b1b8f55cc47c47d199d03f00000000000000000000000000000000000000000000000ae2203cab041de7ab00000000000000000000000000000000000000000000000aa011ed8a3681e2ef00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbca32d7d776604fff6275af355a92e53651da47b7545b2b2a5ccf2b175cf589b",
      "signature": {
        "s": "0x52245eaafa1a9c40cab1d19ae65d07d9a545dcd9501adbf094bc1f434dba9de7",
        "r": "0x8eefc6b3d7269e184fba73e89a5752a63978a637af57c01137b71936b9d5cd89",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xeaa47bc6aeba1b19e3a70586db78fe329878d68728d7bd45f8cc76c18cd417e2",
      "signature": {
        "s": "0x67b4c40ce7b1aaf22c50b12860c0c98b8b671b71aa738c54831c7a0942595df4",
        "r": "0xbc48f5ea4ac70bc265d00002d217f2c6399400ed8808aae6441cf052bb647e17",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4759828858484294844",
    "total": "133565425712790333236"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4759828858484294844",
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
            "amount": "27253796238608688806888"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4759828858484294"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiYzJhMjY1Ny0wZmMyLTUxYTAtODk0ZS0zY2FmMWMwM2VlNzYifQ==",
    "nonce": 109781,
    "balances": {
      "current": "719247408706539011054918",
      "previous": "719252173295226353834056"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc4ec9a4a20f86689b3b1b8f55cc47c47d199d03f",
    "nonce": 46,
    "balances": {
      "current": "200761530894128113579",
      "previous": "196001702035643818735"
    }
  },
  "blockNumber": "14709950",
  "created": "2022-05-04T08:49:52.560Z",
  "updated": "2022-05-04T08:49:52.622Z",
  "id": "62723e307832e20011830ae4"
}
```
* *stageAmount*: `200761530894128113579`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000420e4f20cd9c04bc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000420e4f20cd9c04bc0000000000000000000000000000000000000000000000073d97b7069cb16734bca32d7d776604fff6275af355a92e53651da47b7545b2b2a5ccf2b175cf589b8eefc6b3d7269e184fba73e89a5752a63978a637af57c01137b71936b9d5cd8952245eaafa1a9c40cab1d19ae65d07d9a545dcd9501adbf094bc1f434dba9de7000000000000000000000000000000000000000000000000000000000000001beaa47bc6aeba1b19e3a70586db78fe329878d68728d7bd45f8cc76c18cd417e2bc48f5ea4ac70bc265d00002d217f2c6399400ed8808aae6441cf052bb647e1767b4c40ce7b1aaf22c50b12860c0c98b8b671b71aa738c54831c7a0942595df4000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074be0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001acd5000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000984e7aeb5a814ffe1d4600000000000000000000000000000000000000000000984ebd0a92ac21e7584800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000010e90a044d36460000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c56e66b236ac0cfbe80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a69597a4a684d6a59314e7930775a6d4d794c545578595441744f446b305a53307a5932466d4d574d774d32566c4e7a596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000c4ec9a4a20f86689b3b1b8f55cc47c47d199d03f00000000000000000000000000000000000000000000000ae2203cab041de7ab00000000000000000000000000000000000000000000000aa011ed8a3681e2ef00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbca32d7d776604fff6275af355a92e53651da47b7545b2b2a5ccf2b175cf589b",
      "signature": {
        "s": "0x52245eaafa1a9c40cab1d19ae65d07d9a545dcd9501adbf094bc1f434dba9de7",
        "r": "0x8eefc6b3d7269e184fba73e89a5752a63978a637af57c01137b71936b9d5cd89",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xeaa47bc6aeba1b19e3a70586db78fe329878d68728d7bd45f8cc76c18cd417e2",
      "signature": {
        "s": "0x67b4c40ce7b1aaf22c50b12860c0c98b8b671b71aa738c54831c7a0942595df4",
        "r": "0xbc48f5ea4ac70bc265d00002d217f2c6399400ed8808aae6441cf052bb647e17",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4759828858484294844",
    "total": "133565425712790333236"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4759828858484294844",
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
            "amount": "27253796238608688806888"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4759828858484294"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiYzJhMjY1Ny0wZmMyLTUxYTAtODk0ZS0zY2FmMWMwM2VlNzYifQ==",
    "nonce": 109781,
    "balances": {
      "current": "719247408706539011054918",
      "previous": "719252173295226353834056"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc4ec9a4a20f86689b3b1b8f55cc47c47d199d03f",
    "nonce": 46,
    "balances": {
      "current": "200761530894128113579",
      "previous": "196001702035643818735"
    }
  },
  "blockNumber": "14709950",
  "created": "2022-05-04T08:49:52.560Z",
  "updated": "2022-05-04T08:49:52.622Z",
  "id": "62723e307832e20011830ae4"
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
0x0f200f9b00000000000000000000000000000000000000000000000ae2203cab041de7ab0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `200761530894128113579`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`