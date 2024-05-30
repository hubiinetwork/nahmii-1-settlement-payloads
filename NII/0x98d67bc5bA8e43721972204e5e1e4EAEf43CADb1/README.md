# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x98d67bc5bA8e43721972204e5e1e4EAEf43CADb1`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000003602bc62e2769a72c50000000000000000000000000000000000000000000000000000000a42a6e5820000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000a42a6e58200000000000000000000000000000000000000000000001c8300d16a814a87744466046aa33771d54c243280f9a352d61bb84e635a3c0db608897475ea959227578d3f4062e548516882d4b9bae1c379bba15c60169203d44cedf073bf46240356b5f5c7e687821a051351499bae29354b6c6aaa3c0f26860e6212a4b0d987cf000000000000000000000000000000000000000000000000000000000000001bd2ae05519e2636a30d94e33d23d89d9a23a3f13c0a6e77a13df3cd72541e7aac031399e27b1f13d2a0c3a797cfabd57701c186273c961e49b400f29bcad820773c9ffdcdd740826ed9e752d706e377c4d2d97b3aabd573ac3292d4d16aeb43fe000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b209000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000049c30c6c4d338b0248f90000000000000000000000000000000000000000000049c30c6c4d3dd0499abd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000002a06c420000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d984c2e418d3e348680000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a5468695a4455784e6930334e5451794c5455324f5441744f5756685a5330324f544e694f545134596d52684d6a496966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000098d67bc5ba8e43721972204e5e1e4eaef43cadb100000000000000000000000000000000000000000000003602bc62e2769a72c500000000000000000000000000000000000000000000003602bc62d833f38d4300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4466046aa33771d54c243280f9a352d61bb84e635a3c0db608897475ea959227",
      "signature": {
        "s": "0x56b5f5c7e687821a051351499bae29354b6c6aaa3c0f26860e6212a4b0d987cf",
        "r": "0x578d3f4062e548516882d4b9bae1c379bba15c60169203d44cedf073bf462403",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd2ae05519e2636a30d94e33d23d89d9a23a3f13c0a6e77a13df3cd72541e7aac",
      "signature": {
        "s": "0x3c9ffdcdd740826ed9e752d706e377c4d2d97b3aabd573ac3292d4d16aeb43fe",
        "r": "0x031399e27b1f13d2a0c3a797cfabd57701c186273c961e49b400f29bcad82077",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "44067906946",
    "total": "525948609138201888628"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "44067906946",
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
            "amount": "27624342337696972359784"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "44067906"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlZThiZDUxNi03NTQyLTU2OTAtOWVhZS02OTNiOTQ4YmRhMjIifQ==",
    "nonce": 111113,
    "balances": {
      "current": "348330763519167173904633",
      "previous": "348330763519211285879485"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x98d67bc5ba8e43721972204e5e1e4eaef43cadb1",
    "nonce": 46,
    "balances": {
      "current": "996321321188805210821",
      "previous": "996321321144737303875"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:37.328Z",
  "updated": "2022-05-04T08:56:37.402Z",
  "id": "62723fc5bbd75600116d064b"
}
```
* *stageAmount*: `996321321188805210821`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000a42a6e5820000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000a42a6e58200000000000000000000000000000000000000000000001c8300d16a814a87744466046aa33771d54c243280f9a352d61bb84e635a3c0db608897475ea959227578d3f4062e548516882d4b9bae1c379bba15c60169203d44cedf073bf46240356b5f5c7e687821a051351499bae29354b6c6aaa3c0f26860e6212a4b0d987cf000000000000000000000000000000000000000000000000000000000000001bd2ae05519e2636a30d94e33d23d89d9a23a3f13c0a6e77a13df3cd72541e7aac031399e27b1f13d2a0c3a797cfabd57701c186273c961e49b400f29bcad820773c9ffdcdd740826ed9e752d706e377c4d2d97b3aabd573ac3292d4d16aeb43fe000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b209000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000049c30c6c4d338b0248f90000000000000000000000000000000000000000000049c30c6c4d3dd0499abd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000002a06c420000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d984c2e418d3e348680000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a5468695a4455784e6930334e5451794c5455324f5441744f5756685a5330324f544e694f545134596d52684d6a496966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000098d67bc5ba8e43721972204e5e1e4eaef43cadb100000000000000000000000000000000000000000000003602bc62e2769a72c500000000000000000000000000000000000000000000003602bc62d833f38d4300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4466046aa33771d54c243280f9a352d61bb84e635a3c0db608897475ea959227",
      "signature": {
        "s": "0x56b5f5c7e687821a051351499bae29354b6c6aaa3c0f26860e6212a4b0d987cf",
        "r": "0x578d3f4062e548516882d4b9bae1c379bba15c60169203d44cedf073bf462403",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd2ae05519e2636a30d94e33d23d89d9a23a3f13c0a6e77a13df3cd72541e7aac",
      "signature": {
        "s": "0x3c9ffdcdd740826ed9e752d706e377c4d2d97b3aabd573ac3292d4d16aeb43fe",
        "r": "0x031399e27b1f13d2a0c3a797cfabd57701c186273c961e49b400f29bcad82077",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "44067906946",
    "total": "525948609138201888628"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "44067906946",
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
            "amount": "27624342337696972359784"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "44067906"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlZThiZDUxNi03NTQyLTU2OTAtOWVhZS02OTNiOTQ4YmRhMjIifQ==",
    "nonce": 111113,
    "balances": {
      "current": "348330763519167173904633",
      "previous": "348330763519211285879485"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x98d67bc5ba8e43721972204e5e1e4eaef43cadb1",
    "nonce": 46,
    "balances": {
      "current": "996321321188805210821",
      "previous": "996321321144737303875"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:37.328Z",
  "updated": "2022-05-04T08:56:37.402Z",
  "id": "62723fc5bbd75600116d064b"
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
0x0f200f9b00000000000000000000000000000000000000000000003602bc62e2769a72c50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `996321321188805210821`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`