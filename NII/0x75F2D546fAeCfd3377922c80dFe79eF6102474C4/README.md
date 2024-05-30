# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x75F2D546fAeCfd3377922c80dFe79eF6102474C4`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de0c7ea494e5d3400000000000000000000000000000000000000000000001be821ec07ee9080000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000001be821ec07ee90800000000000000000000000000000000000000000000000001be821ec07ee90800067a5ddd85592b1c37d315f8d4eddd5e809a7188c2a53c23191e1f72ccd053302533dae7e7c01e211101b9a83217582086cc0de236f135f1e5d4f61f44191a931744cbb50bd2711b5725e49a3e94e0608d1428fd32d70d31eace2e98b80f39573000000000000000000000000000000000000000000000000000000000000001cc794e8d93b4a4d70ec470a2f7695d7928172b901f7106f804aec7404f60f5d4a91ee2b8c07cc9d04b47817f51789860b58e5225e164c05348d239af3961d6bf179cc5528fe6a09be886c287fb0bdb6969a79c46bf4c94f44203cd2e04561bf33000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e21ffb0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000500000000000000000000000075f2d546faecfd3377922c80dfe79ef6102474c40000000000000000000000000000000000000000000000000de0c7ea494e5d3400000000000000000000000000000000000000000000001bfd2799d06f262d3400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000724e5de374750000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000724e5de374750000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d7a46684f4749305a5330305a5456684c54526b5a474d74596d4e6a4d53316a597a63794e5441794d5441345932596966513d3d0000000000000000000000000000000000000000000000000000000000000061000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000005842d9e437b151d6fb68000000000000000000000000000000000000000000005826f1c24ba963467b6800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x67a5ddd85592b1c37d315f8d4eddd5e809a7188c2a53c23191e1f72ccd053302",
      "signature": {
        "s": "0x744cbb50bd2711b5725e49a3e94e0608d1428fd32d70d31eace2e98b80f39573",
        "r": "0x533dae7e7c01e211101b9a83217582086cc0de236f135f1e5d4f61f44191a931",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc794e8d93b4a4d70ec470a2f7695d7928172b901f7106f804aec7404f60f5d4a",
      "signature": {
        "s": "0x79cc5528fe6a09be886c287fb0bdb6969a79c46bf4c94f44203cd2e04561bf33",
        "r": "0x91ee2b8c07cc9d04b47817f51789860b58e5225e164c05348d239af3961d6bf1",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "514789000000000000000",
    "total": "514789000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "514789000000000000000",
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
            "amount": "514789000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "514789000000000000"
      }
    },
    "wallet": "0x75f2d546faecfd3377922c80dfe79ef6102474c4",
    "data": "eyJyZWYiOiJlMzFhOGI0ZS00ZTVhLTRkZGMtYmNjMS1jYzcyNTAyMTA4Y2YifQ==",
    "nonce": 5,
    "balances": {
      "current": "1000018926342397236",
      "previous": "516303807926342397236"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 97,
    "balances": {
      "current": "416801436336829251386216",
      "previous": "416286647336829251386216"
    }
  },
  "blockNumber": "14819323",
  "created": "2022-05-21T20:29:16.379Z",
  "updated": "2022-05-21T20:29:16.574Z",
  "id": "62894b9c7832e20011830f2e"
}
```
* *stageAmount*: `1000018926342397236`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000001be821ec07ee9080000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000001be821ec07ee90800000000000000000000000000000000000000000000000001be821ec07ee90800067a5ddd85592b1c37d315f8d4eddd5e809a7188c2a53c23191e1f72ccd053302533dae7e7c01e211101b9a83217582086cc0de236f135f1e5d4f61f44191a931744cbb50bd2711b5725e49a3e94e0608d1428fd32d70d31eace2e98b80f39573000000000000000000000000000000000000000000000000000000000000001cc794e8d93b4a4d70ec470a2f7695d7928172b901f7106f804aec7404f60f5d4a91ee2b8c07cc9d04b47817f51789860b58e5225e164c05348d239af3961d6bf179cc5528fe6a09be886c287fb0bdb6969a79c46bf4c94f44203cd2e04561bf33000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e21ffb0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000500000000000000000000000075f2d546faecfd3377922c80dfe79ef6102474c40000000000000000000000000000000000000000000000000de0c7ea494e5d3400000000000000000000000000000000000000000000001bfd2799d06f262d3400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000724e5de374750000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000724e5de374750000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d7a46684f4749305a5330305a5456684c54526b5a474d74596d4e6a4d53316a597a63794e5441794d5441345932596966513d3d0000000000000000000000000000000000000000000000000000000000000061000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000005842d9e437b151d6fb68000000000000000000000000000000000000000000005826f1c24ba963467b6800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x67a5ddd85592b1c37d315f8d4eddd5e809a7188c2a53c23191e1f72ccd053302",
      "signature": {
        "s": "0x744cbb50bd2711b5725e49a3e94e0608d1428fd32d70d31eace2e98b80f39573",
        "r": "0x533dae7e7c01e211101b9a83217582086cc0de236f135f1e5d4f61f44191a931",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc794e8d93b4a4d70ec470a2f7695d7928172b901f7106f804aec7404f60f5d4a",
      "signature": {
        "s": "0x79cc5528fe6a09be886c287fb0bdb6969a79c46bf4c94f44203cd2e04561bf33",
        "r": "0x91ee2b8c07cc9d04b47817f51789860b58e5225e164c05348d239af3961d6bf1",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "514789000000000000000",
    "total": "514789000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "514789000000000000000",
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
            "amount": "514789000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "514789000000000000"
      }
    },
    "wallet": "0x75f2d546faecfd3377922c80dfe79ef6102474c4",
    "data": "eyJyZWYiOiJlMzFhOGI0ZS00ZTVhLTRkZGMtYmNjMS1jYzcyNTAyMTA4Y2YifQ==",
    "nonce": 5,
    "balances": {
      "current": "1000018926342397236",
      "previous": "516303807926342397236"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 97,
    "balances": {
      "current": "416801436336829251386216",
      "previous": "416286647336829251386216"
    }
  },
  "blockNumber": "14819323",
  "created": "2022-05-21T20:29:16.379Z",
  "updated": "2022-05-21T20:29:16.574Z",
  "id": "62894b9c7832e20011830f2e"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de0c7ea494e5d340000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000018926342397236`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`