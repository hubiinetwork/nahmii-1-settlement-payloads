# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xfeB00B902a251079ddd2413Ad21005905B29409e`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000f854ebf000000000000000000000000000000000000000000000000000000000f854ebf0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000f854ebf000000000000000000000000000000000000000000000000000000000f854ebf0c3739cf0a1f96b0a5891c11bb3c9ceb5587e53ecc7bbf000be561b1dd7f481baebd583062c215254c41234f6723cfc8caf699172b1f8cfbdef0d903a4eb40080285bde0a16c3d0b31ab5af7783d21ecb262c72b3665a4d6ecb6e64d71ca61e0d000000000000000000000000000000000000000000000000000000000000001c6c18f4be3f4b9ec053b542dd7221efa34ded45c7f82d0522762ae9312b3592432a86dc99fe8cfd44c0ee6d75dacae753f718d9875502a51a8ed113a90d4d48e8501b8f4d4307ba536e6ea25e12ac471d78c1e91486d58c705f58b4f2bdda0813000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000192100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e181b4ff91a8e000000000000000000000000000000000000000000000000002e181c488d992800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000003f92aa000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1625f3a6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324f47526b596d49794e7930355a6d566b4c5455784d4759744f5752684d4330784e446c685a6a59315a4449795957556966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000feb00b902a251079ddd2413ad21005905b29409e00000000000000000000000000000000000000000000000000000000f854ebf0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc3739cf0a1f96b0a5891c11bb3c9ceb5587e53ecc7bbf000be561b1dd7f481ba",
      "signature": {
        "s": "0x285bde0a16c3d0b31ab5af7783d21ecb262c72b3665a4d6ecb6e64d71ca61e0d",
        "r": "0xebd583062c215254c41234f6723cfc8caf699172b1f8cfbdef0d903a4eb40080",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6c18f4be3f4b9ec053b542dd7221efa34ded45c7f82d0522762ae9312b359243",
      "signature": {
        "s": "0x501b8f4d4307ba536e6ea25e12ac471d78c1e91486d58c705f58b4f2bdda0813",
        "r": "0x2a86dc99fe8cfd44c0ee6d75dacae753f718d9875502a51a8ed113a90d4d48e8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4166314992",
    "total": "4166314992"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4166314992",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "43321258918"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "4166314"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2OGRkYmIyNy05ZmVkLTUxMGYtOWRhMC0xNDlhZjY1ZDIyYWUifQ==",
    "nonce": 6433,
    "balances": {
      "current": "12974354513599118",
      "previous": "12974358684080424"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfeb00b902a251079ddd2413ad21005905b29409e",
    "nonce": 22,
    "balances": {
      "current": "4166314992",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:05.436Z",
  "updated": "2020-05-22T08:49:05.501Z",
  "id": "5ec79201005df800101bca9f"
}
```
* *stageAmount*: `4166314992`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000f854ebf0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000f854ebf000000000000000000000000000000000000000000000000000000000f854ebf0c3739cf0a1f96b0a5891c11bb3c9ceb5587e53ecc7bbf000be561b1dd7f481baebd583062c215254c41234f6723cfc8caf699172b1f8cfbdef0d903a4eb40080285bde0a16c3d0b31ab5af7783d21ecb262c72b3665a4d6ecb6e64d71ca61e0d000000000000000000000000000000000000000000000000000000000000001c6c18f4be3f4b9ec053b542dd7221efa34ded45c7f82d0522762ae9312b3592432a86dc99fe8cfd44c0ee6d75dacae753f718d9875502a51a8ed113a90d4d48e8501b8f4d4307ba536e6ea25e12ac471d78c1e91486d58c705f58b4f2bdda0813000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000192100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e181b4ff91a8e000000000000000000000000000000000000000000000000002e181c488d992800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000003f92aa000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1625f3a6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324f47526b596d49794e7930355a6d566b4c5455784d4759744f5752684d4330784e446c685a6a59315a4449795957556966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000feb00b902a251079ddd2413ad21005905b29409e00000000000000000000000000000000000000000000000000000000f854ebf0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc3739cf0a1f96b0a5891c11bb3c9ceb5587e53ecc7bbf000be561b1dd7f481ba",
      "signature": {
        "s": "0x285bde0a16c3d0b31ab5af7783d21ecb262c72b3665a4d6ecb6e64d71ca61e0d",
        "r": "0xebd583062c215254c41234f6723cfc8caf699172b1f8cfbdef0d903a4eb40080",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6c18f4be3f4b9ec053b542dd7221efa34ded45c7f82d0522762ae9312b359243",
      "signature": {
        "s": "0x501b8f4d4307ba536e6ea25e12ac471d78c1e91486d58c705f58b4f2bdda0813",
        "r": "0x2a86dc99fe8cfd44c0ee6d75dacae753f718d9875502a51a8ed113a90d4d48e8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4166314992",
    "total": "4166314992"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4166314992",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "43321258918"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "4166314"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2OGRkYmIyNy05ZmVkLTUxMGYtOWRhMC0xNDlhZjY1ZDIyYWUifQ==",
    "nonce": 6433,
    "balances": {
      "current": "12974354513599118",
      "previous": "12974358684080424"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfeb00b902a251079ddd2413ad21005905b29409e",
    "nonce": 22,
    "balances": {
      "current": "4166314992",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:05.436Z",
  "updated": "2020-05-22T08:49:05.501Z",
  "id": "5ec79201005df800101bca9f"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000f854ebf0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4166314992`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`