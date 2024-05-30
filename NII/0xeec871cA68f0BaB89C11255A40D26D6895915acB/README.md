# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xeec871cA68f0BaB89C11255A40D26D6895915acB`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000859f4ca81da79dc84600000000000000000000000000000000000000000000000000000019a6efb98b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000019a6efb98b000000000000000000000000000000000000000000000045dff787afa73c3b23ae83abe47270940e1c895798a22f901b2440bff24ce9e66187db65c15ba899ec099d5cce0e88fcb636970324dd37c719947d2cdbe1f6eecfe2b5ccc71d1a6f960cda599ba0068877da86e140ddb727bbfd1a7d603bc0fff02b66e7abed5e4731000000000000000000000000000000000000000000000000000000000000001ccdf10c2f7a52f2773d9bf3c539ba193333dac0db1889e92000836f5588ca3e57ec59652d35945c926283ade90570391ef2b8fb123c9bc06d5957d97360bdfb235de9f5fd144617197574dd965943f61cd105c0d50c51d9361252c943b3336d42000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074be0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001acf8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000097bf81b12f7aa53ccccd0000000000000000000000000000000000000000000097bf81b12f9452bda91600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000069122be0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c592f73ff0595c33a70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d5749325a4751305979307a596a4e6c4c54557a4f444974596d46685a5330314e5451314e5441774d4751355a6a4d6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000eec871ca68f0bab89c11255a40d26d6895915acb0000000000000000000000000000000000000000000000859f4ca81da79dc8460000000000000000000000000000000000000000000000859f4ca80400ae0ebb00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xae83abe47270940e1c895798a22f901b2440bff24ce9e66187db65c15ba899ec",
      "signature": {
        "s": "0x0cda599ba0068877da86e140ddb727bbfd1a7d603bc0fff02b66e7abed5e4731",
        "r": "0x099d5cce0e88fcb636970324dd37c719947d2cdbe1f6eecfe2b5ccc71d1a6f96",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcdf10c2f7a52f2773d9bf3c539ba193333dac0db1889e92000836f5588ca3e57",
      "signature": {
        "s": "0x5de9f5fd144617197574dd965943f61cd105c0d50c51d9361252c943b3336d42",
        "r": "0xec59652d35945c926283ade90570391ef2b8fb123c9bc06d5957d97360bdfb23",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "110174910859",
    "total": "1288963858064159292195"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "110174910859",
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
            "amount": "27256431000219316663207"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "110174910"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2MWI2ZGQ0Yy0zYjNlLTUzODItYmFhZS01NTQ1NTAwMGQ5ZjMifQ==",
    "nonce": 109816,
    "balances": {
      "current": "716610012334300526857421",
      "previous": "716610012334410811943190"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xeec871ca68f0bab89c11255a40d26d6895915acb",
    "nonce": 46,
    "balances": {
      "current": "2464895696198950570054",
      "previous": "2464895696088775659195"
    }
  },
  "blockNumber": "14709950",
  "created": "2022-05-04T08:50:04.229Z",
  "updated": "2022-05-04T08:50:04.322Z",
  "id": "62723e3cbbd75600116d048d"
}
```
* *stageAmount*: `2464895696198950570054`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000019a6efb98b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000019a6efb98b000000000000000000000000000000000000000000000045dff787afa73c3b23ae83abe47270940e1c895798a22f901b2440bff24ce9e66187db65c15ba899ec099d5cce0e88fcb636970324dd37c719947d2cdbe1f6eecfe2b5ccc71d1a6f960cda599ba0068877da86e140ddb727bbfd1a7d603bc0fff02b66e7abed5e4731000000000000000000000000000000000000000000000000000000000000001ccdf10c2f7a52f2773d9bf3c539ba193333dac0db1889e92000836f5588ca3e57ec59652d35945c926283ade90570391ef2b8fb123c9bc06d5957d97360bdfb235de9f5fd144617197574dd965943f61cd105c0d50c51d9361252c943b3336d42000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074be0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001acf8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000097bf81b12f7aa53ccccd0000000000000000000000000000000000000000000097bf81b12f9452bda91600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000069122be0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c592f73ff0595c33a70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d5749325a4751305979307a596a4e6c4c54557a4f444974596d46685a5330314e5451314e5441774d4751355a6a4d6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000eec871ca68f0bab89c11255a40d26d6895915acb0000000000000000000000000000000000000000000000859f4ca81da79dc8460000000000000000000000000000000000000000000000859f4ca80400ae0ebb00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xae83abe47270940e1c895798a22f901b2440bff24ce9e66187db65c15ba899ec",
      "signature": {
        "s": "0x0cda599ba0068877da86e140ddb727bbfd1a7d603bc0fff02b66e7abed5e4731",
        "r": "0x099d5cce0e88fcb636970324dd37c719947d2cdbe1f6eecfe2b5ccc71d1a6f96",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcdf10c2f7a52f2773d9bf3c539ba193333dac0db1889e92000836f5588ca3e57",
      "signature": {
        "s": "0x5de9f5fd144617197574dd965943f61cd105c0d50c51d9361252c943b3336d42",
        "r": "0xec59652d35945c926283ade90570391ef2b8fb123c9bc06d5957d97360bdfb23",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "110174910859",
    "total": "1288963858064159292195"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "110174910859",
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
            "amount": "27256431000219316663207"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "110174910"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2MWI2ZGQ0Yy0zYjNlLTUzODItYmFhZS01NTQ1NTAwMGQ5ZjMifQ==",
    "nonce": 109816,
    "balances": {
      "current": "716610012334300526857421",
      "previous": "716610012334410811943190"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xeec871ca68f0bab89c11255a40d26d6895915acb",
    "nonce": 46,
    "balances": {
      "current": "2464895696198950570054",
      "previous": "2464895696088775659195"
    }
  },
  "blockNumber": "14709950",
  "created": "2022-05-04T08:50:04.229Z",
  "updated": "2022-05-04T08:50:04.322Z",
  "id": "62723e3cbbd75600116d048d"
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
0x0f200f9b0000000000000000000000000000000000000000000000859f4ca81da79dc8460000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2464895696198950570054`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`