# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe18Cc62F43b72d25d883471F366A0F4701F40BB6`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000017bd302a1a00000000000000000000000000000000000000000000000000000017bd302a1a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000017bd302a1a00000000000000000000000000000000000000000000000000000017bd302a1aebaa404e9afc85c930d5ab5b95da8ee9672dbfed6e0599b87e30bceaf95d1788ce2dbc9e0d472e1f99aeb445a73bb9aa77f718cda7dda8d50505224085b4c9bf4a3cbb699fefad5e43d3a3b0d779aec8e135c07914c728e8a837ef4cbe55768e000000000000000000000000000000000000000000000000000000000000001b92a24d12a6f352ae2ce5904c0fad099c75b08c5e5e0a8a36dc4589c71408e612838b82c9cb90eb57aa72f4eb471e811635b4d85572496b5ba0078341515800f24052d820bba9c4cbf8f2ef3303038c8a63a078f818af3481ea9c713aee9bc335000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56610000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000148000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e2f19e3f23d41000000000000000000000000000000000000000000000000002e2f31a73629f500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000613c29a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000434b0944d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d4749314e5455314d793168596a67304c5455305a6d49744f446c684d79316b596a4e695a544d7a4e4751344d574d6966513d3d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000e18cc62f43b72d25d883471f366a0f4701f40bb600000000000000000000000000000000000000000000000000000017bd302a1a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xebaa404e9afc85c930d5ab5b95da8ee9672dbfed6e0599b87e30bceaf95d1788",
      "signature": {
        "s": "0x4a3cbb699fefad5e43d3a3b0d779aec8e135c07914c728e8a837ef4cbe55768e",
        "r": "0xce2dbc9e0d472e1f99aeb445a73bb9aa77f718cda7dda8d50505224085b4c9bf",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x92a24d12a6f352ae2ce5904c0fad099c75b08c5e5e0a8a36dc4589c71408e612",
      "signature": {
        "s": "0x4052d820bba9c4cbf8f2ef3303038c8a63a078f818af3481ea9c713aee9bc335",
        "r": "0x838b82c9cb90eb57aa72f4eb471e811635b4d85572496b5ba0078341515800f2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "101958298138",
    "total": "101958298138"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "101958298138",
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
            "amount": "18063856717"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "101958298"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMGI1NTU1My1hYjg0LTU0ZmItODlhMy1kYjNiZTMzNGQ4MWMifQ==",
    "nonce": 5248,
    "balances": {
      "current": "12999637173681473",
      "previous": "12999739233937909"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe18cc62f43b72d25d883471f366a0f4701f40bb6",
    "nonce": 12,
    "balances": {
      "current": "101958298138",
      "previous": "0"
    }
  },
  "blockNumber": "10114657",
  "created": "2020-05-22T08:39:38.258Z",
  "updated": "2020-05-22T08:39:38.324Z",
  "id": "5ec78fcae5756b00111b862c"
}
```
* *stageAmount*: `101958298138`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000017bd302a1a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000017bd302a1a00000000000000000000000000000000000000000000000000000017bd302a1aebaa404e9afc85c930d5ab5b95da8ee9672dbfed6e0599b87e30bceaf95d1788ce2dbc9e0d472e1f99aeb445a73bb9aa77f718cda7dda8d50505224085b4c9bf4a3cbb699fefad5e43d3a3b0d779aec8e135c07914c728e8a837ef4cbe55768e000000000000000000000000000000000000000000000000000000000000001b92a24d12a6f352ae2ce5904c0fad099c75b08c5e5e0a8a36dc4589c71408e612838b82c9cb90eb57aa72f4eb471e811635b4d85572496b5ba0078341515800f24052d820bba9c4cbf8f2ef3303038c8a63a078f818af3481ea9c713aee9bc335000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56610000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000148000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e2f19e3f23d41000000000000000000000000000000000000000000000000002e2f31a73629f500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000613c29a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000434b0944d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d4749314e5455314d793168596a67304c5455305a6d49744f446c684d79316b596a4e695a544d7a4e4751344d574d6966513d3d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000e18cc62f43b72d25d883471f366a0f4701f40bb600000000000000000000000000000000000000000000000000000017bd302a1a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xebaa404e9afc85c930d5ab5b95da8ee9672dbfed6e0599b87e30bceaf95d1788",
      "signature": {
        "s": "0x4a3cbb699fefad5e43d3a3b0d779aec8e135c07914c728e8a837ef4cbe55768e",
        "r": "0xce2dbc9e0d472e1f99aeb445a73bb9aa77f718cda7dda8d50505224085b4c9bf",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x92a24d12a6f352ae2ce5904c0fad099c75b08c5e5e0a8a36dc4589c71408e612",
      "signature": {
        "s": "0x4052d820bba9c4cbf8f2ef3303038c8a63a078f818af3481ea9c713aee9bc335",
        "r": "0x838b82c9cb90eb57aa72f4eb471e811635b4d85572496b5ba0078341515800f2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "101958298138",
    "total": "101958298138"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "101958298138",
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
            "amount": "18063856717"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "101958298"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMGI1NTU1My1hYjg0LTU0ZmItODlhMy1kYjNiZTMzNGQ4MWMifQ==",
    "nonce": 5248,
    "balances": {
      "current": "12999637173681473",
      "previous": "12999739233937909"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe18cc62f43b72d25d883471f366a0f4701f40bb6",
    "nonce": 12,
    "balances": {
      "current": "101958298138",
      "previous": "0"
    }
  },
  "blockNumber": "10114657",
  "created": "2020-05-22T08:39:38.258Z",
  "updated": "2020-05-22T08:39:38.324Z",
  "id": "5ec78fcae5756b00111b862c"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000017bd302a1a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `101958298138`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`