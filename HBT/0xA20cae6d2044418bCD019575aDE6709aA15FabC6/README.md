# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xA20cae6d2044418bCD019575aDE6709aA15FabC6`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000016c400000000000000000000000000000000000000000000000000000000000016c40000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000016c400000000000000000000000000000000000000000000000000000000000016c405812c7404d5394707aefa523ad7545051fcc35b041e56d146af4dae14579d38239eeedd10bf7822f220bc330b17fa5af292d6a6c03170167232a69947db60a8732ee28525d8700aa31c22959c438072dcea742640d97e420a6f7432fcbd915bd000000000000000000000000000000000000000000000000000000000000001c51c154ece52648ce069ab6564639b283eb6c4f2cd358beb391d5c1c7be5a099c267037a30a94172b0a4b12c05287580dc13a1ae6c67ef9e2528ddffd0e83bb525bea56b4eb921128542f6c083d4d47ed37df6775adaf42db88030cd294ea5247000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56680000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000156b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d6134c4e7a4000000000000000000000000000000000000000000000000002e1d6134c6544100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000005d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008bcebb335000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d7a4d7759325130596930344d5445354c54566b4f47497459575578595330314e4745334d6a4e69597a41344d32496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000a20cae6d2044418bcd019575ade6709aa15fabc60000000000000000000000000000000000000000000000000000000000016c40000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5812c7404d5394707aefa523ad7545051fcc35b041e56d146af4dae14579d382",
      "signature": {
        "s": "0x32ee28525d8700aa31c22959c438072dcea742640d97e420a6f7432fcbd915bd",
        "r": "0x39eeedd10bf7822f220bc330b17fa5af292d6a6c03170167232a69947db60a87",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x51c154ece52648ce069ab6564639b283eb6c4f2cd358beb391d5c1c7be5a099c",
      "signature": {
        "s": "0x5bea56b4eb921128542f6c083d4d47ed37df6775adaf42db88030cd294ea5247",
        "r": "0x267037a30a94172b0a4b12c05287580dc13a1ae6c67ef9e2528ddffd0e83bb52",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "93248",
    "total": "93248"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "93248",
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
            "amount": "37529301813"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "93"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzMzMwY2Q0Yi04MTE5LTVkOGItYWUxYS01NGE3MjNiYzA4M2IifQ==",
    "nonce": 5483,
    "balances": {
      "current": "12980152263042980",
      "previous": "12980152263136321"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa20cae6d2044418bcd019575ade6709aa15fabc6",
    "nonce": 22,
    "balances": {
      "current": "93248",
      "previous": "0"
    }
  },
  "blockNumber": "10114664",
  "created": "2020-05-22T08:41:25.939Z",
  "updated": "2020-05-22T08:41:26.011Z",
  "id": "5ec79035005df800101bc964"
}
```
* *stageAmount*: `93248`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000016c40000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000016c400000000000000000000000000000000000000000000000000000000000016c405812c7404d5394707aefa523ad7545051fcc35b041e56d146af4dae14579d38239eeedd10bf7822f220bc330b17fa5af292d6a6c03170167232a69947db60a8732ee28525d8700aa31c22959c438072dcea742640d97e420a6f7432fcbd915bd000000000000000000000000000000000000000000000000000000000000001c51c154ece52648ce069ab6564639b283eb6c4f2cd358beb391d5c1c7be5a099c267037a30a94172b0a4b12c05287580dc13a1ae6c67ef9e2528ddffd0e83bb525bea56b4eb921128542f6c083d4d47ed37df6775adaf42db88030cd294ea5247000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56680000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000156b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d6134c4e7a4000000000000000000000000000000000000000000000000002e1d6134c6544100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000005d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008bcebb335000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d7a4d7759325130596930344d5445354c54566b4f47497459575578595330314e4745334d6a4e69597a41344d32496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000a20cae6d2044418bcd019575ade6709aa15fabc60000000000000000000000000000000000000000000000000000000000016c40000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5812c7404d5394707aefa523ad7545051fcc35b041e56d146af4dae14579d382",
      "signature": {
        "s": "0x32ee28525d8700aa31c22959c438072dcea742640d97e420a6f7432fcbd915bd",
        "r": "0x39eeedd10bf7822f220bc330b17fa5af292d6a6c03170167232a69947db60a87",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x51c154ece52648ce069ab6564639b283eb6c4f2cd358beb391d5c1c7be5a099c",
      "signature": {
        "s": "0x5bea56b4eb921128542f6c083d4d47ed37df6775adaf42db88030cd294ea5247",
        "r": "0x267037a30a94172b0a4b12c05287580dc13a1ae6c67ef9e2528ddffd0e83bb52",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "93248",
    "total": "93248"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "93248",
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
            "amount": "37529301813"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "93"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzMzMwY2Q0Yi04MTE5LTVkOGItYWUxYS01NGE3MjNiYzA4M2IifQ==",
    "nonce": 5483,
    "balances": {
      "current": "12980152263042980",
      "previous": "12980152263136321"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa20cae6d2044418bcd019575ade6709aa15fabc6",
    "nonce": 22,
    "balances": {
      "current": "93248",
      "previous": "0"
    }
  },
  "blockNumber": "10114664",
  "created": "2020-05-22T08:41:25.939Z",
  "updated": "2020-05-22T08:41:26.011Z",
  "id": "5ec79035005df800101bc964"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000016c40000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `93248`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`