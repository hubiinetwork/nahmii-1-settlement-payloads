# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3eAF8Bea59069be3c9626c9f8352F6F054d8925a`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000006b374bac000000000000000000000000000000000000000000000000000000006b374bac000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000006b374bac000000000000000000000000000000000000000000000000000000006b374bacae2c8bf6d0069e991312161b3681e2477024ff9462beec930327cc3e8b8ee341734b199a172804c930c4ae4b3af378f5b100f1bc97f8d0e77a7ad4bae350600161897b828dfdd0126a4d8a52fb77ff41222ef8f394ddea4117f7106dc566b416000000000000000000000000000000000000000000000000000000000000001cf29d9f921650453d7ad685c95cb1edefb4f1e46d8da200ebd1784fb23ab8af319ac9cea5326d80dd468a52eb5c3dffdebc51dd2797b789b891b1a3e136362dc221e5f93dec03849c7f2d55505d4fedc1d70fcf312c822792431b065653090d42000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56950000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000196800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17e2f6918e28000000000000000000000000000000000000000000000000002e17e361e44c5500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001b7281000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a248f2a6d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334f474e6b4d546b785a6930774f446b314c54566b4f5449744f5755324e7930344d5755334d7a6b7a597a49335a574d6966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000003eaf8bea59069be3c9626c9f8352f6f054d8925a000000000000000000000000000000000000000000000000000000006b374bac000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xae2c8bf6d0069e991312161b3681e2477024ff9462beec930327cc3e8b8ee341",
      "signature": {
        "s": "0x61897b828dfdd0126a4d8a52fb77ff41222ef8f394ddea4117f7106dc566b416",
        "r": "0x734b199a172804c930c4ae4b3af378f5b100f1bc97f8d0e77a7ad4bae3506001",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf29d9f921650453d7ad685c95cb1edefb4f1e46d8da200ebd1784fb23ab8af31",
      "signature": {
        "s": "0x21e5f93dec03849c7f2d55505d4fedc1d70fcf312c822792431b065653090d42",
        "r": "0x9ac9cea5326d80dd468a52eb5c3dffdebc51dd2797b789b891b1a3e136362dc2",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1798785964",
    "total": "1798785964"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1798785964",
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
            "amount": "43563035245"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1798785"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3OGNkMTkxZi0wODk1LTVkOTItOWU2Ny04MWU3MzkzYzI3ZWMifQ==",
    "nonce": 6504,
    "balances": {
      "current": "12974112495472168",
      "previous": "12974114296056917"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3eaf8bea59069be3c9626c9f8352f6f054d8925a",
    "nonce": 22,
    "balances": {
      "current": "1798785964",
      "previous": "0"
    }
  },
  "blockNumber": "10114709",
  "created": "2020-05-22T08:49:40.609Z",
  "updated": "2020-05-22T08:49:40.706Z",
  "id": "5ec79224b0c6090011d5b146"
}
```
* *stageAmount*: `1798785964`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000006b374bac000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000006b374bac000000000000000000000000000000000000000000000000000000006b374bacae2c8bf6d0069e991312161b3681e2477024ff9462beec930327cc3e8b8ee341734b199a172804c930c4ae4b3af378f5b100f1bc97f8d0e77a7ad4bae350600161897b828dfdd0126a4d8a52fb77ff41222ef8f394ddea4117f7106dc566b416000000000000000000000000000000000000000000000000000000000000001cf29d9f921650453d7ad685c95cb1edefb4f1e46d8da200ebd1784fb23ab8af319ac9cea5326d80dd468a52eb5c3dffdebc51dd2797b789b891b1a3e136362dc221e5f93dec03849c7f2d55505d4fedc1d70fcf312c822792431b065653090d42000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56950000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000196800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17e2f6918e28000000000000000000000000000000000000000000000000002e17e361e44c5500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001b7281000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a248f2a6d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334f474e6b4d546b785a6930774f446b314c54566b4f5449744f5755324e7930344d5755334d7a6b7a597a49335a574d6966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000003eaf8bea59069be3c9626c9f8352f6f054d8925a000000000000000000000000000000000000000000000000000000006b374bac000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xae2c8bf6d0069e991312161b3681e2477024ff9462beec930327cc3e8b8ee341",
      "signature": {
        "s": "0x61897b828dfdd0126a4d8a52fb77ff41222ef8f394ddea4117f7106dc566b416",
        "r": "0x734b199a172804c930c4ae4b3af378f5b100f1bc97f8d0e77a7ad4bae3506001",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf29d9f921650453d7ad685c95cb1edefb4f1e46d8da200ebd1784fb23ab8af31",
      "signature": {
        "s": "0x21e5f93dec03849c7f2d55505d4fedc1d70fcf312c822792431b065653090d42",
        "r": "0x9ac9cea5326d80dd468a52eb5c3dffdebc51dd2797b789b891b1a3e136362dc2",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1798785964",
    "total": "1798785964"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1798785964",
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
            "amount": "43563035245"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1798785"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3OGNkMTkxZi0wODk1LTVkOTItOWU2Ny04MWU3MzkzYzI3ZWMifQ==",
    "nonce": 6504,
    "balances": {
      "current": "12974112495472168",
      "previous": "12974114296056917"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3eaf8bea59069be3c9626c9f8352f6f054d8925a",
    "nonce": 22,
    "balances": {
      "current": "1798785964",
      "previous": "0"
    }
  },
  "blockNumber": "10114709",
  "created": "2020-05-22T08:49:40.609Z",
  "updated": "2020-05-22T08:49:40.706Z",
  "id": "5ec79224b0c6090011d5b146"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000006b374bac000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1798785964`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`