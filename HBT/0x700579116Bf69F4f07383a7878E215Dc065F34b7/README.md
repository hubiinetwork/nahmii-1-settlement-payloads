# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x700579116Bf69F4f07383a7878E215Dc065F34b7`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000766039b900000000000000000000000000000000000000000000000000000000766039b9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000766039b900000000000000000000000000000000000000000000000000000000766039b94f9261055c81ba7ab1dc2f6a1621369df1019d45234fb4167dfe0c9ba685e19bdd38b9a0c685ddb4359266866a9230dc09d2028f06181085049fc56e39b2bbe420eb0fe7f5df4d4b1065162b9a05cb4ebbc62f555552dbf423f111a98a472fe2000000000000000000000000000000000000000000000000000000000000001b6fd8c03f2403ba346c5eb215d0f8c5d6a32b763ed01d5bc7b5c2cd30fe64e6213bd9a5b13f215fba14a35a3c1220888e495d11109e641357535da472222306a40373fc6242a51761f72f898fa9009a6fd5bb59b61fefd0df65750e5c56b2bed4000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56aa00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001bac00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e150c5418a862000000000000000000000000000000000000000000000000002e150cca972ffc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001e4de1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ade645146000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a54426c4e6d5668597930344d5751324c54566b4f5441744f544530597930304f4459795a6d5a6d4e6d517859574d6966513d3d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000700579116bf69f4f07383a7878e215dc065f34b700000000000000000000000000000000000000000000000000000000766039b9000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4f9261055c81ba7ab1dc2f6a1621369df1019d45234fb4167dfe0c9ba685e19b",
      "signature": {
        "s": "0x20eb0fe7f5df4d4b1065162b9a05cb4ebbc62f555552dbf423f111a98a472fe2",
        "r": "0xdd38b9a0c685ddb4359266866a9230dc09d2028f06181085049fc56e39b2bbe4",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6fd8c03f2403ba346c5eb215d0f8c5d6a32b763ed01d5bc7b5c2cd30fe64e621",
      "signature": {
        "s": "0x0373fc6242a51761f72f898fa9009a6fd5bb59b61fefd0df65750e5c56b2bed4",
        "r": "0x3bd9a5b13f215fba14a35a3c1220888e495d11109e641357535da472222306a4",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1986017721",
    "total": "1986017721"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1986017721",
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
            "amount": "46680789318"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1986017"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZTBlNmVhYy04MWQ2LTVkOTAtOTE0Yy00ODYyZmZmNmQxYWMifQ==",
    "nonce": 7084,
    "balances": {
      "current": "12970991623383138",
      "previous": "12970993611386876"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x700579116bf69f4f07383a7878e215dc065f34b7",
    "nonce": 12,
    "balances": {
      "current": "1986017721",
      "previous": "0"
    }
  },
  "blockNumber": "10114730",
  "created": "2020-05-22T08:54:10.727Z",
  "updated": "2020-05-22T08:54:10.799Z",
  "id": "5ec79332005df800101bcb7d"
}
```
* *stageAmount*: `1986017721`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000766039b9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000766039b900000000000000000000000000000000000000000000000000000000766039b94f9261055c81ba7ab1dc2f6a1621369df1019d45234fb4167dfe0c9ba685e19bdd38b9a0c685ddb4359266866a9230dc09d2028f06181085049fc56e39b2bbe420eb0fe7f5df4d4b1065162b9a05cb4ebbc62f555552dbf423f111a98a472fe2000000000000000000000000000000000000000000000000000000000000001b6fd8c03f2403ba346c5eb215d0f8c5d6a32b763ed01d5bc7b5c2cd30fe64e6213bd9a5b13f215fba14a35a3c1220888e495d11109e641357535da472222306a40373fc6242a51761f72f898fa9009a6fd5bb59b61fefd0df65750e5c56b2bed4000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56aa00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001bac00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e150c5418a862000000000000000000000000000000000000000000000000002e150cca972ffc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001e4de1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ade645146000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a54426c4e6d5668597930344d5751324c54566b4f5441744f544530597930304f4459795a6d5a6d4e6d517859574d6966513d3d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000700579116bf69f4f07383a7878e215dc065f34b700000000000000000000000000000000000000000000000000000000766039b9000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4f9261055c81ba7ab1dc2f6a1621369df1019d45234fb4167dfe0c9ba685e19b",
      "signature": {
        "s": "0x20eb0fe7f5df4d4b1065162b9a05cb4ebbc62f555552dbf423f111a98a472fe2",
        "r": "0xdd38b9a0c685ddb4359266866a9230dc09d2028f06181085049fc56e39b2bbe4",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6fd8c03f2403ba346c5eb215d0f8c5d6a32b763ed01d5bc7b5c2cd30fe64e621",
      "signature": {
        "s": "0x0373fc6242a51761f72f898fa9009a6fd5bb59b61fefd0df65750e5c56b2bed4",
        "r": "0x3bd9a5b13f215fba14a35a3c1220888e495d11109e641357535da472222306a4",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1986017721",
    "total": "1986017721"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1986017721",
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
            "amount": "46680789318"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1986017"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZTBlNmVhYy04MWQ2LTVkOTAtOTE0Yy00ODYyZmZmNmQxYWMifQ==",
    "nonce": 7084,
    "balances": {
      "current": "12970991623383138",
      "previous": "12970993611386876"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x700579116bf69f4f07383a7878e215dc065f34b7",
    "nonce": 12,
    "balances": {
      "current": "1986017721",
      "previous": "0"
    }
  },
  "blockNumber": "10114730",
  "created": "2020-05-22T08:54:10.727Z",
  "updated": "2020-05-22T08:54:10.799Z",
  "id": "5ec79332005df800101bcb7d"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000766039b9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1986017721`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`