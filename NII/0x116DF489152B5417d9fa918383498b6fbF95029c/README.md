# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x116DF489152B5417d9fa918383498b6fbF95029c`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de24afe6121d5a400000000000000000000000000000000000000000000007a3e65cb00d51580000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000007a3e65cb00d515800000000000000000000000000000000000000000000000007a3e65cb00d51580005e9b38c2359052432a4b6ddd70948e9686fa512973f18e3cb01c862027e07ed2dac078cb33b38d9bbaea6acc94c4e75b7d40fbcc1ef79baf47bde5934e9f95d820e17e22a51a014e2d5805c571807b3b6dd880582093e16ed70db9291765fe54000000000000000000000000000000000000000000000000000000000000001b4d4f9982c8c2523175b311f6693d97308ec46d5294f14568feac7e98ac234558903f1eb3ef9e7920e27aa3602adc0a33b53b8084e27e4075c34d218ec2a8db51513e281ace5451d0914789a5b8928e21f12d9469bcedad59791bf8c17c1b0602000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e307ab00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000000002000000000000000000000000116df489152b5417d9fa918383498b6fbf95029c0000000000000000000000000000000000000000000000000de24afe6121d5a400000000000000000000000000000000000000000000007a6b9373a3d213c5a400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000001f4b5da49bdc70000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001f4b5da49bdc70000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4f574d794e47517a5a693033595455784c5451335a44637459575a6c5a53316b4d444a695a54557a4e5759324f47516966513d3d000000000000000000000000000000000000000000000000000000000000010e000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000001a8d0d2d9e206dc2f4a5f00000000000000000000000000000000000000000001a856947417060719ca5f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5e9b38c2359052432a4b6ddd70948e9686fa512973f18e3cb01c862027e07ed2",
      "signature": {
        "s": "0x20e17e22a51a014e2d5805c571807b3b6dd880582093e16ed70db9291765fe54",
        "r": "0xdac078cb33b38d9bbaea6acc94c4e75b7d40fbcc1ef79baf47bde5934e9f95d8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4d4f9982c8c2523175b311f6693d97308ec46d5294f14568feac7e98ac234558",
      "signature": {
        "s": "0x513e281ace5451d0914789a5b8928e21f12d9469bcedad59791bf8c17c1b0602",
        "r": "0x903f1eb3ef9e7920e27aa3602adc0a33b53b8084e27e4075c34d218ec2a8db51",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2254999000000000000000",
    "total": "2254999000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2254999000000000000000",
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
            "amount": "2254999000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2254999000000000000"
      }
    },
    "wallet": "0x116df489152b5417d9fa918383498b6fbf95029c",
    "data": "eyJyZWYiOiIzOWMyNGQzZi03YTUxLTQ3ZDctYWZlZS1kMDJiZTUzNWY2OGQifQ==",
    "nonce": 2,
    "balances": {
      "current": "1000444523641427364",
      "previous": "2258254443523641427364"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 270,
    "balances": {
      "current": "2006135504927398160190047",
      "previous": "2003880505927398160190047"
    }
  },
  "blockNumber": "14878635",
  "created": "2022-05-31T12:17:15.253Z",
  "updated": "2022-05-31T12:17:15.372Z",
  "id": "6296074bbbd75600116d091e"
}
```
* *stageAmount*: `1000444523641427364`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000007a3e65cb00d51580000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000007a3e65cb00d515800000000000000000000000000000000000000000000000007a3e65cb00d51580005e9b38c2359052432a4b6ddd70948e9686fa512973f18e3cb01c862027e07ed2dac078cb33b38d9bbaea6acc94c4e75b7d40fbcc1ef79baf47bde5934e9f95d820e17e22a51a014e2d5805c571807b3b6dd880582093e16ed70db9291765fe54000000000000000000000000000000000000000000000000000000000000001b4d4f9982c8c2523175b311f6693d97308ec46d5294f14568feac7e98ac234558903f1eb3ef9e7920e27aa3602adc0a33b53b8084e27e4075c34d218ec2a8db51513e281ace5451d0914789a5b8928e21f12d9469bcedad59791bf8c17c1b0602000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e307ab00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000000002000000000000000000000000116df489152b5417d9fa918383498b6fbf95029c0000000000000000000000000000000000000000000000000de24afe6121d5a400000000000000000000000000000000000000000000007a6b9373a3d213c5a400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000001f4b5da49bdc70000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001f4b5da49bdc70000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4f574d794e47517a5a693033595455784c5451335a44637459575a6c5a53316b4d444a695a54557a4e5759324f47516966513d3d000000000000000000000000000000000000000000000000000000000000010e000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000001a8d0d2d9e206dc2f4a5f00000000000000000000000000000000000000000001a856947417060719ca5f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5e9b38c2359052432a4b6ddd70948e9686fa512973f18e3cb01c862027e07ed2",
      "signature": {
        "s": "0x20e17e22a51a014e2d5805c571807b3b6dd880582093e16ed70db9291765fe54",
        "r": "0xdac078cb33b38d9bbaea6acc94c4e75b7d40fbcc1ef79baf47bde5934e9f95d8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4d4f9982c8c2523175b311f6693d97308ec46d5294f14568feac7e98ac234558",
      "signature": {
        "s": "0x513e281ace5451d0914789a5b8928e21f12d9469bcedad59791bf8c17c1b0602",
        "r": "0x903f1eb3ef9e7920e27aa3602adc0a33b53b8084e27e4075c34d218ec2a8db51",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2254999000000000000000",
    "total": "2254999000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2254999000000000000000",
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
            "amount": "2254999000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2254999000000000000"
      }
    },
    "wallet": "0x116df489152b5417d9fa918383498b6fbf95029c",
    "data": "eyJyZWYiOiIzOWMyNGQzZi03YTUxLTQ3ZDctYWZlZS1kMDJiZTUzNWY2OGQifQ==",
    "nonce": 2,
    "balances": {
      "current": "1000444523641427364",
      "previous": "2258254443523641427364"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 270,
    "balances": {
      "current": "2006135504927398160190047",
      "previous": "2003880505927398160190047"
    }
  },
  "blockNumber": "14878635",
  "created": "2022-05-31T12:17:15.253Z",
  "updated": "2022-05-31T12:17:15.372Z",
  "id": "6296074bbbd75600116d091e"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de24afe6121d5a40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000444523641427364`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`