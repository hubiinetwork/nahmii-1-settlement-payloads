# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x61b4aeeC790045dB2cbC0e9C4827A966bD38e9b5`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000227a000000000000000000000000000000000000000000000000000000000000227a0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000227a000000000000000000000000000000000000000000000000000000000000227a078e422fc75bf9296a536bc5e59563be68c1e83977d10ac1f04c9cbb3b17cbad194241519a284bab6155189c69a8d6f7086e56ed1fa95eda2a6c0d650afab328d4e07194b758e600b22d42cec4b15910ec8c4b6de5512802428a513fa4ceb9ddd000000000000000000000000000000000000000000000000000000000000001b7c8e4562251805b23d45c82e9a41157627614f0d80c822eb6bd62e7a2f742bc33ec49a618e2880b4e75586c7e2943554ee6640028f2fc5af44675653a3852bff57caaf1409b0e233a6b24e82cc4d24b74c047504a7a9032956702ce769ee596e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56930000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000195900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17e83f0d77ed000000000000000000000000000000000000000000000000002e17e83f0fa01a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000008d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a2335469a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e544d345a4445344d6930775a4464684c5455305a5445744f444d7a5a69316c4f5745314d6a497a595449794d6d596966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000061b4aeec790045db2cbc0e9c4827a966bd38e9b500000000000000000000000000000000000000000000000000000000000227a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x78e422fc75bf9296a536bc5e59563be68c1e83977d10ac1f04c9cbb3b17cbad1",
      "signature": {
        "s": "0x4e07194b758e600b22d42cec4b15910ec8c4b6de5512802428a513fa4ceb9ddd",
        "r": "0x94241519a284bab6155189c69a8d6f7086e56ed1fa95eda2a6c0d650afab328d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7c8e4562251805b23d45c82e9a41157627614f0d80c822eb6bd62e7a2f742bc3",
      "signature": {
        "s": "0x57caaf1409b0e233a6b24e82cc4d24b74c047504a7a9032956702ce769ee596e",
        "r": "0x3ec49a618e2880b4e75586c7e2943554ee6640028f2fc5af44675653a3852bff",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "141216",
    "total": "141216"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "141216",
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
            "amount": "43540367002"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "141"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0NTM4ZDE4Mi0wZDdhLTU0ZTEtODMzZi1lOWE1MjIzYTIyMmYifQ==",
    "nonce": 6489,
    "balances": {
      "current": "12974135186388973",
      "previous": "12974135186530330"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x61b4aeec790045db2cbc0e9c4827a966bd38e9b5",
    "nonce": 22,
    "balances": {
      "current": "141216",
      "previous": "0"
    }
  },
  "blockNumber": "10114707",
  "created": "2020-05-22T08:49:30.478Z",
  "updated": "2020-05-22T08:49:30.549Z",
  "id": "5ec7921ab0c6090011d5b13e"
}
```
* *stageAmount*: `141216`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000227a0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000227a000000000000000000000000000000000000000000000000000000000000227a078e422fc75bf9296a536bc5e59563be68c1e83977d10ac1f04c9cbb3b17cbad194241519a284bab6155189c69a8d6f7086e56ed1fa95eda2a6c0d650afab328d4e07194b758e600b22d42cec4b15910ec8c4b6de5512802428a513fa4ceb9ddd000000000000000000000000000000000000000000000000000000000000001b7c8e4562251805b23d45c82e9a41157627614f0d80c822eb6bd62e7a2f742bc33ec49a618e2880b4e75586c7e2943554ee6640028f2fc5af44675653a3852bff57caaf1409b0e233a6b24e82cc4d24b74c047504a7a9032956702ce769ee596e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56930000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000195900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17e83f0d77ed000000000000000000000000000000000000000000000000002e17e83f0fa01a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000008d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a2335469a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e544d345a4445344d6930775a4464684c5455305a5445744f444d7a5a69316c4f5745314d6a497a595449794d6d596966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000061b4aeec790045db2cbc0e9c4827a966bd38e9b500000000000000000000000000000000000000000000000000000000000227a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x78e422fc75bf9296a536bc5e59563be68c1e83977d10ac1f04c9cbb3b17cbad1",
      "signature": {
        "s": "0x4e07194b758e600b22d42cec4b15910ec8c4b6de5512802428a513fa4ceb9ddd",
        "r": "0x94241519a284bab6155189c69a8d6f7086e56ed1fa95eda2a6c0d650afab328d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7c8e4562251805b23d45c82e9a41157627614f0d80c822eb6bd62e7a2f742bc3",
      "signature": {
        "s": "0x57caaf1409b0e233a6b24e82cc4d24b74c047504a7a9032956702ce769ee596e",
        "r": "0x3ec49a618e2880b4e75586c7e2943554ee6640028f2fc5af44675653a3852bff",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "141216",
    "total": "141216"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "141216",
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
            "amount": "43540367002"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "141"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0NTM4ZDE4Mi0wZDdhLTU0ZTEtODMzZi1lOWE1MjIzYTIyMmYifQ==",
    "nonce": 6489,
    "balances": {
      "current": "12974135186388973",
      "previous": "12974135186530330"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x61b4aeec790045db2cbc0e9c4827a966bd38e9b5",
    "nonce": 22,
    "balances": {
      "current": "141216",
      "previous": "0"
    }
  },
  "blockNumber": "10114707",
  "created": "2020-05-22T08:49:30.478Z",
  "updated": "2020-05-22T08:49:30.549Z",
  "id": "5ec7921ab0c6090011d5b13e"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000227a0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `141216`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`