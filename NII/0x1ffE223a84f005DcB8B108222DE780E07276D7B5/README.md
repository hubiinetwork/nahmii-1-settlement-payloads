# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1ffE223a84f005DcB8B108222DE780E07276D7B5`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000380d1b1d0d42e0f7000000000000000000000000000000000000000000000000000000001f11f8ab0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001f11f8ab00000000000000000000000000000000000000000000000000000002d5209e0460701e535f260336a9e237f4457b9aca1ce417efd452ef17f70a7b0cbf33c64e023792ba41eaaed08ecb1b90d380d4927c453eb1192dcfd4597e2325457e203a1ed0aebd9bf429f22b91519b1c8771da15c057cfa57282d78d459652dcd015a2000000000000000000000000000000000000000000000000000000000000001bf14cb54006aac10e4f323bb1df8b7e97e08cf0e6e12112bccd990f492b5382be6bb18bfd6dc6339d42a10d89f28722026bbde8f35512c0d6bf95d08577694e6d7190bcdf62f9c971ad4eb1adf0e7a08371a327f90294bd8efcc3e297a9a92ee4000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b752000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002dae08f04527cc105d65000000000000000000000000000000000000000000002dae08f04527eb2a4a4700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000007f4370000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e0b34f6b23532ef5750000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e4467324e6a59355a5331684d4759344c5455784d6d5174596d4e6b4e53316b4f4467355a6a6b774d4445334e6a596966513d3d00000000000000000000000000000000000000000000000000000000000000240000000000000000000000001ffe223a84f005dcb8b108222de780e07276d7b5000000000000000000000000000000000000000000000000380d1b1d0d42e0f7000000000000000000000000000000000000000000000000380d1b1cee30e84c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x60701e535f260336a9e237f4457b9aca1ce417efd452ef17f70a7b0cbf33c64e",
      "signature": {
        "s": "0x1ed0aebd9bf429f22b91519b1c8771da15c057cfa57282d78d459652dcd015a2",
        "r": "0x023792ba41eaaed08ecb1b90d380d4927c453eb1192dcfd4597e2325457e203a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf14cb54006aac10e4f323bb1df8b7e97e08cf0e6e12112bccd990f492b5382be",
      "signature": {
        "s": "0x7190bcdf62f9c971ad4eb1adf0e7a08371a327f90294bd8efcc3e297a9a92ee4",
        "r": "0x6bb18bfd6dc6339d42a10d89f28722026bbde8f35512c0d6bf95d08577694e6d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "521271467",
    "total": "12165619204"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "521271467",
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
            "amount": "27756823750514578486645"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "521271"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNDg2NjY5ZS1hMGY4LTUxMmQtYmNkNS1kODg5ZjkwMDE3NjYifQ==",
    "nonce": 112466,
    "balances": {
      "current": "215716869288743440244069",
      "previous": "215716869288743962036807"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1ffe223a84f005dcb8b108222de780e07276d7b5",
    "nonce": 36,
    "balances": {
      "current": "4038914252411691255",
      "previous": "4038914251890419788"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:56.624Z",
  "updated": "2022-05-04T09:03:56.710Z",
  "id": "6272417c7832e20011830e59"
}
```
* *stageAmount*: `4038914252411691255`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000001f11f8ab0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001f11f8ab00000000000000000000000000000000000000000000000000000002d5209e0460701e535f260336a9e237f4457b9aca1ce417efd452ef17f70a7b0cbf33c64e023792ba41eaaed08ecb1b90d380d4927c453eb1192dcfd4597e2325457e203a1ed0aebd9bf429f22b91519b1c8771da15c057cfa57282d78d459652dcd015a2000000000000000000000000000000000000000000000000000000000000001bf14cb54006aac10e4f323bb1df8b7e97e08cf0e6e12112bccd990f492b5382be6bb18bfd6dc6339d42a10d89f28722026bbde8f35512c0d6bf95d08577694e6d7190bcdf62f9c971ad4eb1adf0e7a08371a327f90294bd8efcc3e297a9a92ee4000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b752000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002dae08f04527cc105d65000000000000000000000000000000000000000000002dae08f04527eb2a4a4700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000007f4370000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e0b34f6b23532ef5750000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e4467324e6a59355a5331684d4759344c5455784d6d5174596d4e6b4e53316b4f4467355a6a6b774d4445334e6a596966513d3d00000000000000000000000000000000000000000000000000000000000000240000000000000000000000001ffe223a84f005dcb8b108222de780e07276d7b5000000000000000000000000000000000000000000000000380d1b1d0d42e0f7000000000000000000000000000000000000000000000000380d1b1cee30e84c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x60701e535f260336a9e237f4457b9aca1ce417efd452ef17f70a7b0cbf33c64e",
      "signature": {
        "s": "0x1ed0aebd9bf429f22b91519b1c8771da15c057cfa57282d78d459652dcd015a2",
        "r": "0x023792ba41eaaed08ecb1b90d380d4927c453eb1192dcfd4597e2325457e203a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf14cb54006aac10e4f323bb1df8b7e97e08cf0e6e12112bccd990f492b5382be",
      "signature": {
        "s": "0x7190bcdf62f9c971ad4eb1adf0e7a08371a327f90294bd8efcc3e297a9a92ee4",
        "r": "0x6bb18bfd6dc6339d42a10d89f28722026bbde8f35512c0d6bf95d08577694e6d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "521271467",
    "total": "12165619204"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "521271467",
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
            "amount": "27756823750514578486645"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "521271"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNDg2NjY5ZS1hMGY4LTUxMmQtYmNkNS1kODg5ZjkwMDE3NjYifQ==",
    "nonce": 112466,
    "balances": {
      "current": "215716869288743440244069",
      "previous": "215716869288743962036807"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1ffe223a84f005dcb8b108222de780e07276d7b5",
    "nonce": 36,
    "balances": {
      "current": "4038914252411691255",
      "previous": "4038914251890419788"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:56.624Z",
  "updated": "2022-05-04T09:03:56.710Z",
  "id": "6272417c7832e20011830e59"
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
0x0f200f9b000000000000000000000000000000000000000000000000380d1b1d0d42e0f70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4038914252411691255`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`