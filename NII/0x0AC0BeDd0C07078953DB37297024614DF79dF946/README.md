# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0AC0BeDd0C07078953DB37297024614DF79dF946`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000155831b9ace509b7400000000000000000000000000000000000000000000000155831b9ace509b740000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000155831b9ace509b7400000000000000000000000000000000000000000000000155831b9ace509b746887c442dfd6ae85f6e14787cd3addb38bf4672daae3a283cb129347f2f930b4c387dfaeab759440dbcd70908efa5ef2ce050957730d8b3ee40783bbd3310fc81c64b5ac97941dc230e5cfb27c31fb117b71a0a198b5455be097aed0663fac8b000000000000000000000000000000000000000000000000000000000000001cf7fe75f8f15b364642325cf16d8f86206d527d1739faaf346b97ed50edf8b2033718f41de5af52c86694aa58d635d434eee431e99c2fcf29739d6a2e13447796114db3f41c4dbdecc050d7f83d301a30e02374fe3863710d1608a48cf49db41a000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000c2cf9900000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000013ab5000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002192d9dbe6f4bf98da7d0000000000000000000000000000000000000000000021942fb66fe67e3f0b9900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000576d56f05595a80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c63cab7c9f157d12040000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e6a55354e32526b5a43316a4e4459304c545535596a5974596a457a5a5330344d7a426c4d3259794f54557a4e6d596966513d3d00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000ac0bedd0c07078953db37297024614df79df94600000000000000000000000000000000000000000000000155831b9ace509b74000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6887c442dfd6ae85f6e14787cd3addb38bf4672daae3a283cb129347f2f930b4",
      "signature": {
        "s": "0x1c64b5ac97941dc230e5cfb27c31fb117b71a0a198b5455be097aed0663fac8b",
        "r": "0xc387dfaeab759440dbcd70908efa5ef2ce050957730d8b3ee40783bbd3310fc8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf7fe75f8f15b364642325cf16d8f86206d527d1739faaf346b97ed50edf8b203",
      "signature": {
        "s": "0x114db3f41c4dbdecc050d7f83d301a30e02374fe3863710d1608a48cf49db41a",
        "r": "0x3718f41de5af52c86694aa58d635d434eee431e99c2fcf29739d6a2e13447796",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "24608543140582824820",
    "total": "24608543140582824820"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "24608543140582824820",
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
            "amount": "17823926500089422221828"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "24608543140582824"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkNjU5N2RkZC1jNDY0LTU5YjYtYjEzZS04MzBlM2YyOTUzNmYifQ==",
    "nonce": 80565,
    "balances": {
      "current": "158547016964324877458045",
      "previous": "158571650116008600865689"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0ac0bedd0c07078953db37297024614df79df946",
    "nonce": 1,
    "balances": {
      "current": "24608543140582824820",
      "previous": "0"
    }
  },
  "blockNumber": "12767129",
  "created": "2021-07-05T11:16:05.436Z",
  "updated": "2021-07-05T11:16:05.546Z",
  "id": "60e2e9f5f2deeb00101fcb65"
}
```
* *stageAmount*: `24608543140582824820`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000155831b9ace509b740000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000155831b9ace509b7400000000000000000000000000000000000000000000000155831b9ace509b746887c442dfd6ae85f6e14787cd3addb38bf4672daae3a283cb129347f2f930b4c387dfaeab759440dbcd70908efa5ef2ce050957730d8b3ee40783bbd3310fc81c64b5ac97941dc230e5cfb27c31fb117b71a0a198b5455be097aed0663fac8b000000000000000000000000000000000000000000000000000000000000001cf7fe75f8f15b364642325cf16d8f86206d527d1739faaf346b97ed50edf8b2033718f41de5af52c86694aa58d635d434eee431e99c2fcf29739d6a2e13447796114db3f41c4dbdecc050d7f83d301a30e02374fe3863710d1608a48cf49db41a000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000c2cf9900000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000013ab5000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002192d9dbe6f4bf98da7d0000000000000000000000000000000000000000000021942fb66fe67e3f0b9900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000576d56f05595a80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c63cab7c9f157d12040000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e6a55354e32526b5a43316a4e4459304c545535596a5974596a457a5a5330344d7a426c4d3259794f54557a4e6d596966513d3d00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000ac0bedd0c07078953db37297024614df79df94600000000000000000000000000000000000000000000000155831b9ace509b74000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6887c442dfd6ae85f6e14787cd3addb38bf4672daae3a283cb129347f2f930b4",
      "signature": {
        "s": "0x1c64b5ac97941dc230e5cfb27c31fb117b71a0a198b5455be097aed0663fac8b",
        "r": "0xc387dfaeab759440dbcd70908efa5ef2ce050957730d8b3ee40783bbd3310fc8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf7fe75f8f15b364642325cf16d8f86206d527d1739faaf346b97ed50edf8b203",
      "signature": {
        "s": "0x114db3f41c4dbdecc050d7f83d301a30e02374fe3863710d1608a48cf49db41a",
        "r": "0x3718f41de5af52c86694aa58d635d434eee431e99c2fcf29739d6a2e13447796",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "24608543140582824820",
    "total": "24608543140582824820"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "24608543140582824820",
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
            "amount": "17823926500089422221828"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "24608543140582824"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkNjU5N2RkZC1jNDY0LTU5YjYtYjEzZS04MzBlM2YyOTUzNmYifQ==",
    "nonce": 80565,
    "balances": {
      "current": "158547016964324877458045",
      "previous": "158571650116008600865689"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0ac0bedd0c07078953db37297024614df79df946",
    "nonce": 1,
    "balances": {
      "current": "24608543140582824820",
      "previous": "0"
    }
  },
  "blockNumber": "12767129",
  "created": "2021-07-05T11:16:05.436Z",
  "updated": "2021-07-05T11:16:05.546Z",
  "id": "60e2e9f5f2deeb00101fcb65"
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
0x0f200f9b00000000000000000000000000000000000000000000000155831b9ace509b740000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `24608543140582824820`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`