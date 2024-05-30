# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x292F6802B1c16e3eE2f792665Fe03a499CbC7aA2`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000117382050000000000000000000000000000000000000000000000000000000011738205000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000011738205000000000000000000000000000000000000000000000000000000001173820524847ce27e4b6173646b4489e69c03350c6bd85f5b2b545a406df7365c5db4f355e1a2de3767f1c11d66ada05d8c904eea667a2b64ea110c78f39c746a3b87be4c252ff01d63c2287d8dffc4e8131b2f4fbde4219e35dc931f61f4b4bf266043000000000000000000000000000000000000000000000000000000000000001b56b4d6dc8cf36173051c71acded347143ebbd54cf6851bda330ea4f7e069a4b0f654302a56008f52cf75aca9226c8b90854ea3b4a867bdf597d298f9c20690d64098b25cf88647235c835fd9a0482e761e2c9c4133ae20afe32496e34e1f00a6000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56960000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000198200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17cebf8a1c0f000000000000000000000000000000000000000000000000002e17ced10215c200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000477ae000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a29baa647000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a4463794d4451784d533032596d55774c545668597a4d744f4746694e53316b59546b784e324e685a446c6b5a574d6966513d3d0000000000000000000000000000000000000000000000000000000000000010000000000000000000000000292f6802b1c16e3ee2f792665fe03a499cbc7aa20000000000000000000000000000000000000000000000000000000011738205000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x24847ce27e4b6173646b4489e69c03350c6bd85f5b2b545a406df7365c5db4f3",
      "signature": {
        "s": "0x4c252ff01d63c2287d8dffc4e8131b2f4fbde4219e35dc931f61f4b4bf266043",
        "r": "0x55e1a2de3767f1c11d66ada05d8c904eea667a2b64ea110c78f39c746a3b87be",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x56b4d6dc8cf36173051c71acded347143ebbd54cf6851bda330ea4f7e069a4b0",
      "signature": {
        "s": "0x4098b25cf88647235c835fd9a0482e761e2c9c4133ae20afe32496e34e1f00a6",
        "r": "0xf654302a56008f52cf75aca9226c8b90854ea3b4a867bdf597d298f9c20690d6",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "292782597",
    "total": "292782597"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "292782597",
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
            "amount": "43649771079"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "292782"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1ZDcyMDQxMS02YmUwLTVhYzMtOGFiNS1kYTkxN2NhZDlkZWMifQ==",
    "nonce": 6530,
    "balances": {
      "current": "12974025672891407",
      "previous": "12974025965966786"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x292f6802b1c16e3ee2f792665fe03a499cbc7aa2",
    "nonce": 16,
    "balances": {
      "current": "292782597",
      "previous": "0"
    }
  },
  "blockNumber": "10114710",
  "created": "2020-05-22T08:49:52.540Z",
  "updated": "2020-05-22T08:49:52.612Z",
  "id": "5ec79230e5756b00111b87c7"
}
```
* *stageAmount*: `292782597`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000011738205000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000011738205000000000000000000000000000000000000000000000000000000001173820524847ce27e4b6173646b4489e69c03350c6bd85f5b2b545a406df7365c5db4f355e1a2de3767f1c11d66ada05d8c904eea667a2b64ea110c78f39c746a3b87be4c252ff01d63c2287d8dffc4e8131b2f4fbde4219e35dc931f61f4b4bf266043000000000000000000000000000000000000000000000000000000000000001b56b4d6dc8cf36173051c71acded347143ebbd54cf6851bda330ea4f7e069a4b0f654302a56008f52cf75aca9226c8b90854ea3b4a867bdf597d298f9c20690d64098b25cf88647235c835fd9a0482e761e2c9c4133ae20afe32496e34e1f00a6000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56960000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000198200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17cebf8a1c0f000000000000000000000000000000000000000000000000002e17ced10215c200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000477ae000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a29baa647000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a4463794d4451784d533032596d55774c545668597a4d744f4746694e53316b59546b784e324e685a446c6b5a574d6966513d3d0000000000000000000000000000000000000000000000000000000000000010000000000000000000000000292f6802b1c16e3ee2f792665fe03a499cbc7aa20000000000000000000000000000000000000000000000000000000011738205000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x24847ce27e4b6173646b4489e69c03350c6bd85f5b2b545a406df7365c5db4f3",
      "signature": {
        "s": "0x4c252ff01d63c2287d8dffc4e8131b2f4fbde4219e35dc931f61f4b4bf266043",
        "r": "0x55e1a2de3767f1c11d66ada05d8c904eea667a2b64ea110c78f39c746a3b87be",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x56b4d6dc8cf36173051c71acded347143ebbd54cf6851bda330ea4f7e069a4b0",
      "signature": {
        "s": "0x4098b25cf88647235c835fd9a0482e761e2c9c4133ae20afe32496e34e1f00a6",
        "r": "0xf654302a56008f52cf75aca9226c8b90854ea3b4a867bdf597d298f9c20690d6",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "292782597",
    "total": "292782597"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "292782597",
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
            "amount": "43649771079"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "292782"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1ZDcyMDQxMS02YmUwLTVhYzMtOGFiNS1kYTkxN2NhZDlkZWMifQ==",
    "nonce": 6530,
    "balances": {
      "current": "12974025672891407",
      "previous": "12974025965966786"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x292f6802b1c16e3ee2f792665fe03a499cbc7aa2",
    "nonce": 16,
    "balances": {
      "current": "292782597",
      "previous": "0"
    }
  },
  "blockNumber": "10114710",
  "created": "2020-05-22T08:49:52.540Z",
  "updated": "2020-05-22T08:49:52.612Z",
  "id": "5ec79230e5756b00111b87c7"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000011738205000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `292782597`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`