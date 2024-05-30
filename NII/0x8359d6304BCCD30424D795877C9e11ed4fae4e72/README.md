# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8359d6304BCCD30424D795877C9e11ed4fae4e72`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000006a3903a77e8aa7535d00000000000000000000000000000000000000000000000000000017f15957420000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000017f159574200000000000000000000000000000000000000000000002eb8919e9945da6e79ba2221ce12bd40885e058c588986fe1ed9c418d10538b65b8b1784e3ba60286cc5c316dd3c24b28c1f06cc809fd5221bdc10281de490b00203b0ee99b5b9f7af22388ec2bb74698c78ab29e0c2406a1c5cad8fc3a9784546fac443a2bc650e8e000000000000000000000000000000000000000000000000000000000000001b70a25fabef58249e030d16a15cc1ba215bd55b2d09aaf10539ce00ee0ae06149e3c923709869734396e5657013212d6cc4d8afa52699f84ef0190945add869072a45ab3de294a1ef0277105bc79f74cec00167fc0f93683d57815af53911c14c000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0db000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004bab8ac9be60e8e2d86d000000000000000000000000000000000000000000004bab8ac9be78e05d4cb200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000006211d030000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d907d4f49b77b9e2d80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694f44646c4d6a6b785a43307a4e6a45314c5455775a5459744f4455344d43307a4f5756684d6a417a596d45774f44496966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000008359d6304bccd30424d795877c9e11ed4fae4e7200000000000000000000000000000000000000000000006a3903a77e8aa7535d00000000000000000000000000000000000000000000006a3903a766994dfc1b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xba2221ce12bd40885e058c588986fe1ed9c418d10538b65b8b1784e3ba60286c",
      "signature": {
        "s": "0x22388ec2bb74698c78ab29e0c2406a1c5cad8fc3a9784546fac443a2bc650e8e",
        "r": "0xc5c316dd3c24b28c1f06cc809fd5221bdc10281de490b00203b0ee99b5b9f7af",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x70a25fabef58249e030d16a15cc1ba215bd55b2d09aaf10539ce00ee0ae06149",
      "signature": {
        "s": "0x2a45ab3de294a1ef0277105bc79f74cec00167fc0f93683d57815af53911c14c",
        "r": "0xe3c923709869734396e5657013212d6cc4d8afa52699f84ef0190945add86907",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "102833411906",
    "total": "861849812946380287609"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "102833411906",
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
            "amount": "27615340223145092702936"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "102833411"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiODdlMjkxZC0zNjE1LTUwZTYtODU4MC0zOWVhMjAzYmEwODIifQ==",
    "nonce": 110811,
    "balances": {
      "current": "357341880185598710569069",
      "previous": "357341880185701646814386"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8359d6304bccd30424d795877c9e11ed4fae4e72",
    "nonce": 46,
    "balances": {
      "current": "1959463183260238435165",
      "previous": "1959463183157405023259"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:55:09.443Z",
  "updated": "2022-05-04T08:55:09.552Z",
  "id": "62723f6d7832e20011830c31"
}
```
* *stageAmount*: `1959463183260238435165`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000017f15957420000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000017f159574200000000000000000000000000000000000000000000002eb8919e9945da6e79ba2221ce12bd40885e058c588986fe1ed9c418d10538b65b8b1784e3ba60286cc5c316dd3c24b28c1f06cc809fd5221bdc10281de490b00203b0ee99b5b9f7af22388ec2bb74698c78ab29e0c2406a1c5cad8fc3a9784546fac443a2bc650e8e000000000000000000000000000000000000000000000000000000000000001b70a25fabef58249e030d16a15cc1ba215bd55b2d09aaf10539ce00ee0ae06149e3c923709869734396e5657013212d6cc4d8afa52699f84ef0190945add869072a45ab3de294a1ef0277105bc79f74cec00167fc0f93683d57815af53911c14c000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0db000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004bab8ac9be60e8e2d86d000000000000000000000000000000000000000000004bab8ac9be78e05d4cb200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000006211d030000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d907d4f49b77b9e2d80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694f44646c4d6a6b785a43307a4e6a45314c5455775a5459744f4455344d43307a4f5756684d6a417a596d45774f44496966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000008359d6304bccd30424d795877c9e11ed4fae4e7200000000000000000000000000000000000000000000006a3903a77e8aa7535d00000000000000000000000000000000000000000000006a3903a766994dfc1b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xba2221ce12bd40885e058c588986fe1ed9c418d10538b65b8b1784e3ba60286c",
      "signature": {
        "s": "0x22388ec2bb74698c78ab29e0c2406a1c5cad8fc3a9784546fac443a2bc650e8e",
        "r": "0xc5c316dd3c24b28c1f06cc809fd5221bdc10281de490b00203b0ee99b5b9f7af",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x70a25fabef58249e030d16a15cc1ba215bd55b2d09aaf10539ce00ee0ae06149",
      "signature": {
        "s": "0x2a45ab3de294a1ef0277105bc79f74cec00167fc0f93683d57815af53911c14c",
        "r": "0xe3c923709869734396e5657013212d6cc4d8afa52699f84ef0190945add86907",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "102833411906",
    "total": "861849812946380287609"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "102833411906",
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
            "amount": "27615340223145092702936"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "102833411"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiODdlMjkxZC0zNjE1LTUwZTYtODU4MC0zOWVhMjAzYmEwODIifQ==",
    "nonce": 110811,
    "balances": {
      "current": "357341880185598710569069",
      "previous": "357341880185701646814386"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8359d6304bccd30424d795877c9e11ed4fae4e72",
    "nonce": 46,
    "balances": {
      "current": "1959463183260238435165",
      "previous": "1959463183157405023259"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:55:09.443Z",
  "updated": "2022-05-04T08:55:09.552Z",
  "id": "62723f6d7832e20011830c31"
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
0x0f200f9b00000000000000000000000000000000000000000000006a3903a77e8aa7535d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1959463183260238435165`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`