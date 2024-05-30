# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x02f5B3631430d4d6956711Ccd3EEBDF6cE0D5665`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000001ba1e90731ad2d300000000000000000000000000000000000000000000000001ba1e90731ad2d300000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000001ba1e90731ad2d300000000000000000000000000000000000000000000000001ba1e90731ad2d30b8502a1653df5cc1ad0b3671a6b1059facc8f6fd3991a8e5b5a8565957376193fe9864decce8329a73a97da0039599ef07a5453a863f59ea0643035ca9185c3b46b4aaeb853752d2aa201e583f0245db1624e28929946babc8fd937768d733b4000000000000000000000000000000000000000000000000000000000000001cca79fcae0278f2c7b366b52d188bc535ee827cf1293117bdaacbe61662f40f95c8b306d52b0b80b8a89a96c8d44f3378933bb6ed9cbcafc42a21a9a07b4522880b3663d6dd393b04605a2902dd7d28b409b8be7e06d5418dfd7f6b592155bc06000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000c6eb410000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001485d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000001b49305448717db18f70000000000000000000000000000000000000000000001b4aeae407a1207ade000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000712ebc87f67b90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004048b06b2705fba19cd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4f5759345957526a4e433034597a51354c5455304e6d4d744f474d794e4330354d474a694e6a526a4f545a6d59544d6966513d3d000000000000000000000000000000000000000000000000000000000000000100000000000000000000000002f5b3631430d4d6956711ccd3eebdf6ce0d56650000000000000000000000000000000000000000000000001ba1e90731ad2d30000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb8502a1653df5cc1ad0b3671a6b1059facc8f6fd3991a8e5b5a8565957376193",
      "signature": {
        "s": "0x46b4aaeb853752d2aa201e583f0245db1624e28929946babc8fd937768d733b4",
        "r": "0xfe9864decce8329a73a97da0039599ef07a5453a863f59ea0643035ca9185c3b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xca79fcae0278f2c7b366b52d188bc535ee827cf1293117bdaacbe61662f40f95",
      "signature": {
        "s": "0x0b3663d6dd393b04605a2902dd7d28b409b8be7e06d5418dfd7f6b592155bc06",
        "r": "0xc8b306d52b0b80b8a89a96c8d44f3378933bb6ed9cbcafc42a21a9a07b452288",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1991128727381945648",
    "total": "1991128727381945648"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1991128727381945648",
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
            "amount": "18973270798390263421389"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1991128727381945"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlOWY4YWRjNC04YzQ5LTU0NmMtOGMyNC05MGJiNjRjOTZmYTMifQ==",
    "nonce": 84061,
    "balances": {
      "current": "8053374365182834972919",
      "previous": "8055367485038944300512"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x02f5b3631430d4d6956711ccd3eebdf6ce0d5665",
    "nonce": 1,
    "balances": {
      "current": "1991128727381945648",
      "previous": "0"
    }
  },
  "blockNumber": "13036353",
  "created": "2021-08-16T12:46:34.660Z",
  "updated": "2021-08-16T12:46:34.738Z",
  "id": "611a5e2a440f8100105b106f"
}
```
* *stageAmount*: `1991128727381945648`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000001ba1e90731ad2d300000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000001ba1e90731ad2d300000000000000000000000000000000000000000000000001ba1e90731ad2d30b8502a1653df5cc1ad0b3671a6b1059facc8f6fd3991a8e5b5a8565957376193fe9864decce8329a73a97da0039599ef07a5453a863f59ea0643035ca9185c3b46b4aaeb853752d2aa201e583f0245db1624e28929946babc8fd937768d733b4000000000000000000000000000000000000000000000000000000000000001cca79fcae0278f2c7b366b52d188bc535ee827cf1293117bdaacbe61662f40f95c8b306d52b0b80b8a89a96c8d44f3378933bb6ed9cbcafc42a21a9a07b4522880b3663d6dd393b04605a2902dd7d28b409b8be7e06d5418dfd7f6b592155bc06000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000c6eb410000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001485d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000001b49305448717db18f70000000000000000000000000000000000000000000001b4aeae407a1207ade000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000712ebc87f67b90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004048b06b2705fba19cd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4f5759345957526a4e433034597a51354c5455304e6d4d744f474d794e4330354d474a694e6a526a4f545a6d59544d6966513d3d000000000000000000000000000000000000000000000000000000000000000100000000000000000000000002f5b3631430d4d6956711ccd3eebdf6ce0d56650000000000000000000000000000000000000000000000001ba1e90731ad2d30000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb8502a1653df5cc1ad0b3671a6b1059facc8f6fd3991a8e5b5a8565957376193",
      "signature": {
        "s": "0x46b4aaeb853752d2aa201e583f0245db1624e28929946babc8fd937768d733b4",
        "r": "0xfe9864decce8329a73a97da0039599ef07a5453a863f59ea0643035ca9185c3b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xca79fcae0278f2c7b366b52d188bc535ee827cf1293117bdaacbe61662f40f95",
      "signature": {
        "s": "0x0b3663d6dd393b04605a2902dd7d28b409b8be7e06d5418dfd7f6b592155bc06",
        "r": "0xc8b306d52b0b80b8a89a96c8d44f3378933bb6ed9cbcafc42a21a9a07b452288",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1991128727381945648",
    "total": "1991128727381945648"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1991128727381945648",
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
            "amount": "18973270798390263421389"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1991128727381945"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlOWY4YWRjNC04YzQ5LTU0NmMtOGMyNC05MGJiNjRjOTZmYTMifQ==",
    "nonce": 84061,
    "balances": {
      "current": "8053374365182834972919",
      "previous": "8055367485038944300512"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x02f5b3631430d4d6956711ccd3eebdf6ce0d5665",
    "nonce": 1,
    "balances": {
      "current": "1991128727381945648",
      "previous": "0"
    }
  },
  "blockNumber": "13036353",
  "created": "2021-08-16T12:46:34.660Z",
  "updated": "2021-08-16T12:46:34.738Z",
  "id": "611a5e2a440f8100105b106f"
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
0x0f200f9b0000000000000000000000000000000000000000000000001ba1e90731ad2d300000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1991128727381945648`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`