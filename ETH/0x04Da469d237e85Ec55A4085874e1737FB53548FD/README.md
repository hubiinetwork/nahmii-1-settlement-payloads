# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x04Da469d237e85Ec55A4085874e1737FB53548FD`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000041ae00000000000000000000000000000000000000000000000000000000000041ae000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000041ae00000000000000000000000000000000000000000000000000000000000041ae43b7226002032b612075c40db7df46a91cf56d418ab4e0bf7159827b33704ddcef60b0a0abce745f13ea5a64d31c3e7f27bc743724b99c0ede19faa7f54b5f266f9bd41a2d1f111fa42e31ba0ce197f811eba020cca1abd894322fe438d42b93000000000000000000000000000000000000000000000000000000000000001b13b7db63c5af251df3a4c3f99065b185bf6d6507a55dc96b55fa1a808e188d4562581b63832c688f542a0f6323cf9d7ff1fdd2455f9ba532f21f12b47d369e7d568464b4fe354fff4c1853050cb89ee73bdbfeedd73357025250693b420cd393000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000039300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caafd830000000000000000000000000000000000000000000000000002386f2cab019ee00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008844000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d3255355a544d304d7930334d5759334c54566d59574d744f5745324d7930774e3251334d44566b4e546335596a636966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000004da469d237e85ec55a4085874e1737fb53548fd00000000000000000000000000000000000000000000000000000000000041ae000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x43b7226002032b612075c40db7df46a91cf56d418ab4e0bf7159827b33704ddc",
      "signature": {
        "s": "0x6f9bd41a2d1f111fa42e31ba0ce197f811eba020cca1abd894322fe438d42b93",
        "r": "0xef60b0a0abce745f13ea5a64d31c3e7f27bc743724b99c0ede19faa7f54b5f26",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x13b7db63c5af251df3a4c3f99065b185bf6d6507a55dc96b55fa1a808e188d45",
      "signature": {
        "s": "0x568464b4fe354fff4c1853050cb89ee73bdbfeedd73357025250693b420cd393",
        "r": "0x62581b63832c688f542a0f6323cf9d7ff1fdd2455f9ba532f21f12b47d369e7d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "16814",
    "total": "16814"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16814",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "558144"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "16"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5M2U5ZTM0My03MWY3LTVmYWMtOWE2My0wN2Q3MDVkNTc5YjcifQ==",
    "nonce": 915,
    "balances": {
      "current": "10000001525602352",
      "previous": "10000001525619182"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x04da469d237e85ec55a4085874e1737fb53548fd",
    "nonce": 20,
    "balances": {
      "current": "16814",
      "previous": "0"
    }
  },
  "blockNumber": "10114515",
  "created": "2020-05-22T08:05:26.243Z",
  "updated": "2020-05-22T08:05:26.324Z",
  "id": "5ec787c6b0c6090011d5aa02"
}
```
* *stageAmount*: `16814`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000041ae000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000041ae00000000000000000000000000000000000000000000000000000000000041ae43b7226002032b612075c40db7df46a91cf56d418ab4e0bf7159827b33704ddcef60b0a0abce745f13ea5a64d31c3e7f27bc743724b99c0ede19faa7f54b5f266f9bd41a2d1f111fa42e31ba0ce197f811eba020cca1abd894322fe438d42b93000000000000000000000000000000000000000000000000000000000000001b13b7db63c5af251df3a4c3f99065b185bf6d6507a55dc96b55fa1a808e188d4562581b63832c688f542a0f6323cf9d7ff1fdd2455f9ba532f21f12b47d369e7d568464b4fe354fff4c1853050cb89ee73bdbfeedd73357025250693b420cd393000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000039300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caafd830000000000000000000000000000000000000000000000000002386f2cab019ee00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008844000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d3255355a544d304d7930334d5759334c54566d59574d744f5745324d7930774e3251334d44566b4e546335596a636966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000004da469d237e85ec55a4085874e1737fb53548fd00000000000000000000000000000000000000000000000000000000000041ae000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x43b7226002032b612075c40db7df46a91cf56d418ab4e0bf7159827b33704ddc",
      "signature": {
        "s": "0x6f9bd41a2d1f111fa42e31ba0ce197f811eba020cca1abd894322fe438d42b93",
        "r": "0xef60b0a0abce745f13ea5a64d31c3e7f27bc743724b99c0ede19faa7f54b5f26",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x13b7db63c5af251df3a4c3f99065b185bf6d6507a55dc96b55fa1a808e188d45",
      "signature": {
        "s": "0x568464b4fe354fff4c1853050cb89ee73bdbfeedd73357025250693b420cd393",
        "r": "0x62581b63832c688f542a0f6323cf9d7ff1fdd2455f9ba532f21f12b47d369e7d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "16814",
    "total": "16814"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16814",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "558144"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "16"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5M2U5ZTM0My03MWY3LTVmYWMtOWE2My0wN2Q3MDVkNTc5YjcifQ==",
    "nonce": 915,
    "balances": {
      "current": "10000001525602352",
      "previous": "10000001525619182"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x04da469d237e85ec55a4085874e1737fb53548fd",
    "nonce": 20,
    "balances": {
      "current": "16814",
      "previous": "0"
    }
  },
  "blockNumber": "10114515",
  "created": "2020-05-22T08:05:26.243Z",
  "updated": "2020-05-22T08:05:26.324Z",
  "id": "5ec787c6b0c6090011d5aa02"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000000000000000041ae0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `16814`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``