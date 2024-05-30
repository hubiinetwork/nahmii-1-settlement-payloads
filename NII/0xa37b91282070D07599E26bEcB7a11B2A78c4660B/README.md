# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xa37b91282070D07599E26bEcB7a11B2A78c4660B`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000005cdef0e7455336030000000000000000000000000000000000000000000000000233ad4de4b852a30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000233ad4de4b852a30000000000000000000000000000000000000000000000003dc952e69ed08283c0a891c62cfb3d5139f4a52e926f5c7fd7d614dd59846381ed3796ebac6fa8b01fad3f7ddbf2b8efe640f161af9fcbae05059309a1d6b6753197cfbf135dcab902a5b86ce98af90b7def542ecec71b20278196a2a85f3aac5653728f835a6d77000000000000000000000000000000000000000000000000000000000000001bd2ab8f3fdde56853c9307949c7f5018c30d80b4477783226aa41779ccb89b426191c3d2aa12e649d7e2777810adf3986fc731ce170f2c5c26ebf11e58ddf804574230cbd5d96fcb74620914f9e16d51c555ef2dba6b1a4300ac162e08677f707000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af3d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000007f989cb75170f84974cb000000000000000000000000000000000000000000007f989eeb8f0bff489e8d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000904d2246d71f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005cbc0349f4c2bc134160000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d6d4d784e32497a4f533079597a597a4c54566a4d6a4d744f5442695a43316d5a6a6330597a49795a5745354e32496966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000a37b91282070d07599e26becb7a11b2a78c4660b0000000000000000000000000000000000000000000000005cdef0e7455336030000000000000000000000000000000000000000000000005aab4399609ae36000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc0a891c62cfb3d5139f4a52e926f5c7fd7d614dd59846381ed3796ebac6fa8b0",
      "signature": {
        "s": "0x02a5b86ce98af90b7def542ecec71b20278196a2a85f3aac5653728f835a6d77",
        "r": "0x1fad3f7ddbf2b8efe640f161af9fcbae05059309a1d6b6753197cfbf135dcab9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd2ab8f3fdde56853c9307949c7f5018c30d80b4477783226aa41779ccb89b426",
      "signature": {
        "s": "0x74230cbd5d96fcb74620914f9e16d51c555ef2dba6b1a4300ac162e08677f707",
        "r": "0x191c3d2aa12e649d7e2777810adf3986fc731ce170f2c5c26ebf11e58ddf8045",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "158660961949471395",
    "total": "4452180857092866691"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "158660961949471395",
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
            "amount": "27370371331214836577302"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "158660961949471"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4MmMxN2IzOS0yYzYzLTVjMjMtOTBiZC1mZjc0YzIyZWE5N2IifQ==",
    "nonce": 110397,
    "balances": {
      "current": "602555741007785092543691",
      "previous": "602555899827408003964557"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa37b91282070d07599e26becb7a11b2a78c4660b",
    "nonce": 46,
    "balances": {
      "current": "6692050972410328579",
      "previous": "6533390010460857184"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:53:04.909Z",
  "updated": "2022-05-04T08:53:04.988Z",
  "id": "62723ef07832e20011830ba6"
}
```
* *stageAmount*: `6692050972410328579`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000233ad4de4b852a30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000233ad4de4b852a30000000000000000000000000000000000000000000000003dc952e69ed08283c0a891c62cfb3d5139f4a52e926f5c7fd7d614dd59846381ed3796ebac6fa8b01fad3f7ddbf2b8efe640f161af9fcbae05059309a1d6b6753197cfbf135dcab902a5b86ce98af90b7def542ecec71b20278196a2a85f3aac5653728f835a6d77000000000000000000000000000000000000000000000000000000000000001bd2ab8f3fdde56853c9307949c7f5018c30d80b4477783226aa41779ccb89b426191c3d2aa12e649d7e2777810adf3986fc731ce170f2c5c26ebf11e58ddf804574230cbd5d96fcb74620914f9e16d51c555ef2dba6b1a4300ac162e08677f707000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af3d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000007f989cb75170f84974cb000000000000000000000000000000000000000000007f989eeb8f0bff489e8d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000904d2246d71f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005cbc0349f4c2bc134160000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d6d4d784e32497a4f533079597a597a4c54566a4d6a4d744f5442695a43316d5a6a6330597a49795a5745354e32496966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000a37b91282070d07599e26becb7a11b2a78c4660b0000000000000000000000000000000000000000000000005cdef0e7455336030000000000000000000000000000000000000000000000005aab4399609ae36000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc0a891c62cfb3d5139f4a52e926f5c7fd7d614dd59846381ed3796ebac6fa8b0",
      "signature": {
        "s": "0x02a5b86ce98af90b7def542ecec71b20278196a2a85f3aac5653728f835a6d77",
        "r": "0x1fad3f7ddbf2b8efe640f161af9fcbae05059309a1d6b6753197cfbf135dcab9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd2ab8f3fdde56853c9307949c7f5018c30d80b4477783226aa41779ccb89b426",
      "signature": {
        "s": "0x74230cbd5d96fcb74620914f9e16d51c555ef2dba6b1a4300ac162e08677f707",
        "r": "0x191c3d2aa12e649d7e2777810adf3986fc731ce170f2c5c26ebf11e58ddf8045",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "158660961949471395",
    "total": "4452180857092866691"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "158660961949471395",
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
            "amount": "27370371331214836577302"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "158660961949471"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4MmMxN2IzOS0yYzYzLTVjMjMtOTBiZC1mZjc0YzIyZWE5N2IifQ==",
    "nonce": 110397,
    "balances": {
      "current": "602555741007785092543691",
      "previous": "602555899827408003964557"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa37b91282070d07599e26becb7a11b2a78c4660b",
    "nonce": 46,
    "balances": {
      "current": "6692050972410328579",
      "previous": "6533390010460857184"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:53:04.909Z",
  "updated": "2022-05-04T08:53:04.988Z",
  "id": "62723ef07832e20011830ba6"
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
0x0f200f9b0000000000000000000000000000000000000000000000005cdef0e7455336030000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6692050972410328579`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`