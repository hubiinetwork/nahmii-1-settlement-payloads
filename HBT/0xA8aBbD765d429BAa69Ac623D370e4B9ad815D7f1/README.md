# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xA8aBbD765d429BAa69Ac623D370e4B9ad815D7f1`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000007e241460000000000000000000000000000000000000000000000000000000007e24146000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000007e241460000000000000000000000000000000000000000000000000000000007e24146391e9d34559288274a205ab6177bc6aca3d8d769f8fae31be4d19193c4c88d805797cb0fd18ef47a0e4c0a9ec9cd2d55ab2cbc999cb0c6fee746d776144e167765001000f4668394464ba6dce3a5327b434d9a53b0ab538112e635d6f1a53183000000000000000000000000000000000000000000000000000000000000001cc9065c1caae169d7c0e9e7686dd793e5df4346b2595677f948981d2f0b0be8504526e46f26a2da49b15f87b12aab02b3f19354c9bc7df65ae086a7535fbac2b70ec276377b534c023e8e8b584b5ebc7a391ad2bcaadbc2bf032feb36f80372ad000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a566e000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000015eb00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d47ca8110c0000000000000000000000000000000000000000000000000002e1d47d26556b200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000204ac000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008c36ba3b9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a4468695a6a6c6d4d79316c596d59784c5456685a5755744f5749314d79316d4f4441314d4755314d5449774d44496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000a8abbd765d429baa69ac623d370e4b9ad815d7f10000000000000000000000000000000000000000000000000000000007e24146000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x391e9d34559288274a205ab6177bc6aca3d8d769f8fae31be4d19193c4c88d80",
      "signature": {
        "s": "0x65001000f4668394464ba6dce3a5327b434d9a53b0ab538112e635d6f1a53183",
        "r": "0x5797cb0fd18ef47a0e4c0a9ec9cd2d55ab2cbc999cb0c6fee746d776144e1677",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc9065c1caae169d7c0e9e7686dd793e5df4346b2595677f948981d2f0b0be850",
      "signature": {
        "s": "0x0ec276377b534c023e8e8b584b5ebc7a391ad2bcaadbc2bf032feb36f80372ad",
        "r": "0x4526e46f26a2da49b15f87b12aab02b3f19354c9bc7df65ae086a7535fbac2b7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "132268358",
    "total": "132268358"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "132268358",
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
            "amount": "37638349753"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "132268"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZDhiZjlmMy1lYmYxLTVhZWUtOWI1My1mODA1MGU1MTIwMDIifQ==",
    "nonce": 5611,
    "balances": {
      "current": "12980043106029760",
      "previous": "12980043238430386"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa8abbd765d429baa69ac623d370e4b9ad815d7f1",
    "nonce": 22,
    "balances": {
      "current": "132268358",
      "previous": "0"
    }
  },
  "blockNumber": "10114670",
  "created": "2020-05-22T08:42:28.337Z",
  "updated": "2020-05-22T08:42:28.411Z",
  "id": "5ec79074005df800101bc98e"
}
```
* *stageAmount*: `132268358`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000007e24146000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000007e241460000000000000000000000000000000000000000000000000000000007e24146391e9d34559288274a205ab6177bc6aca3d8d769f8fae31be4d19193c4c88d805797cb0fd18ef47a0e4c0a9ec9cd2d55ab2cbc999cb0c6fee746d776144e167765001000f4668394464ba6dce3a5327b434d9a53b0ab538112e635d6f1a53183000000000000000000000000000000000000000000000000000000000000001cc9065c1caae169d7c0e9e7686dd793e5df4346b2595677f948981d2f0b0be8504526e46f26a2da49b15f87b12aab02b3f19354c9bc7df65ae086a7535fbac2b70ec276377b534c023e8e8b584b5ebc7a391ad2bcaadbc2bf032feb36f80372ad000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a566e000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000015eb00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d47ca8110c0000000000000000000000000000000000000000000000000002e1d47d26556b200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000204ac000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008c36ba3b9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a4468695a6a6c6d4d79316c596d59784c5456685a5755744f5749314d79316d4f4441314d4755314d5449774d44496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000a8abbd765d429baa69ac623d370e4b9ad815d7f10000000000000000000000000000000000000000000000000000000007e24146000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x391e9d34559288274a205ab6177bc6aca3d8d769f8fae31be4d19193c4c88d80",
      "signature": {
        "s": "0x65001000f4668394464ba6dce3a5327b434d9a53b0ab538112e635d6f1a53183",
        "r": "0x5797cb0fd18ef47a0e4c0a9ec9cd2d55ab2cbc999cb0c6fee746d776144e1677",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc9065c1caae169d7c0e9e7686dd793e5df4346b2595677f948981d2f0b0be850",
      "signature": {
        "s": "0x0ec276377b534c023e8e8b584b5ebc7a391ad2bcaadbc2bf032feb36f80372ad",
        "r": "0x4526e46f26a2da49b15f87b12aab02b3f19354c9bc7df65ae086a7535fbac2b7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "132268358",
    "total": "132268358"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "132268358",
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
            "amount": "37638349753"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "132268"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZDhiZjlmMy1lYmYxLTVhZWUtOWI1My1mODA1MGU1MTIwMDIifQ==",
    "nonce": 5611,
    "balances": {
      "current": "12980043106029760",
      "previous": "12980043238430386"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa8abbd765d429baa69ac623d370e4b9ad815d7f1",
    "nonce": 22,
    "balances": {
      "current": "132268358",
      "previous": "0"
    }
  },
  "blockNumber": "10114670",
  "created": "2020-05-22T08:42:28.337Z",
  "updated": "2020-05-22T08:42:28.411Z",
  "id": "5ec79074005df800101bc98e"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000007e24146000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `132268358`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`