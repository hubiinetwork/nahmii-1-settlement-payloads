# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xa76a148Db5131D5c4eeAe33C76A019f5599626b5`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000009aaaba60000000000000000000000000000000000000000000000000000000009aaaba6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000009aaaba60000000000000000000000000000000000000000000000000000000009aaaba691dbaf50b4fb79f36e8caeb796e86ec2e09945f49b46b48960405bb16e465405e4175437f7cab693be1cbd3d0838abefae24c50cb829d4a6c9474bd312efd4fa065ddaa18aa0c5f3070e996996980be5ba4e8d18b7c99147ada84cd49e67d2c2000000000000000000000000000000000000000000000000000000000000001c186961eb8a4f7917c3ac6f01166abe5972194c0c518f3c4a051eaeb68741e4f750f67216bcf15f63b52b76e23425616b0cab57a8ed4c66003358b0435fb63bdd022060ca621daeeee561b07e434134af0ddab0ec0e78e020e620b41e152e22d4000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ba00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001dff00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b120c063478000000000000000000000000000000000000000000000000002e0b1215b359a200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000027984000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6ba27a3b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d44646b4d325a694d7930325a6a59354c545577596a45744f4464684e53316b5a4449784d5441315a44557a596a596966513d3d0000000000000000000000000000000000000000000000000000000000000008000000000000000000000000a76a148db5131d5c4eeae33c76a019f5599626b50000000000000000000000000000000000000000000000000000000009aaaba6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x91dbaf50b4fb79f36e8caeb796e86ec2e09945f49b46b48960405bb16e465405",
      "signature": {
        "s": "0x065ddaa18aa0c5f3070e996996980be5ba4e8d18b7c99147ada84cd49e67d2c2",
        "r": "0xe4175437f7cab693be1cbd3d0838abefae24c50cb829d4a6c9474bd312efd4fa",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x186961eb8a4f7917c3ac6f01166abe5972194c0c518f3c4a051eaeb68741e4f7",
      "signature": {
        "s": "0x022060ca621daeeee561b07e434134af0ddab0ec0e78e020e620b41e152e22d4",
        "r": "0x50f67216bcf15f63b52b76e23425616b0cab57a8ed4c66003358b0435fb63bdd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "162180006",
    "total": "162180006"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "162180006",
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
            "amount": "57640385083"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "162180"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMDdkM2ZiMy02ZjY5LTUwYjEtODdhNS1kZDIxMTA1ZDUzYjYifQ==",
    "nonce": 7679,
    "balances": {
      "current": "12960021067740280",
      "previous": "12960021230082466"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa76a148db5131d5c4eeae33c76a019f5599626b5",
    "nonce": 8,
    "balances": {
      "current": "162180006",
      "previous": "0"
    }
  },
  "blockNumber": "10114746",
  "created": "2020-05-22T08:58:40.312Z",
  "updated": "2020-05-22T08:58:40.383Z",
  "id": "5ec79440b0c6090011d5b2dc"
}
```
* *stageAmount*: `162180006`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000009aaaba6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000009aaaba60000000000000000000000000000000000000000000000000000000009aaaba691dbaf50b4fb79f36e8caeb796e86ec2e09945f49b46b48960405bb16e465405e4175437f7cab693be1cbd3d0838abefae24c50cb829d4a6c9474bd312efd4fa065ddaa18aa0c5f3070e996996980be5ba4e8d18b7c99147ada84cd49e67d2c2000000000000000000000000000000000000000000000000000000000000001c186961eb8a4f7917c3ac6f01166abe5972194c0c518f3c4a051eaeb68741e4f750f67216bcf15f63b52b76e23425616b0cab57a8ed4c66003358b0435fb63bdd022060ca621daeeee561b07e434134af0ddab0ec0e78e020e620b41e152e22d4000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ba00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001dff00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b120c063478000000000000000000000000000000000000000000000000002e0b1215b359a200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000027984000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6ba27a3b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d44646b4d325a694d7930325a6a59354c545577596a45744f4464684e53316b5a4449784d5441315a44557a596a596966513d3d0000000000000000000000000000000000000000000000000000000000000008000000000000000000000000a76a148db5131d5c4eeae33c76a019f5599626b50000000000000000000000000000000000000000000000000000000009aaaba6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x91dbaf50b4fb79f36e8caeb796e86ec2e09945f49b46b48960405bb16e465405",
      "signature": {
        "s": "0x065ddaa18aa0c5f3070e996996980be5ba4e8d18b7c99147ada84cd49e67d2c2",
        "r": "0xe4175437f7cab693be1cbd3d0838abefae24c50cb829d4a6c9474bd312efd4fa",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x186961eb8a4f7917c3ac6f01166abe5972194c0c518f3c4a051eaeb68741e4f7",
      "signature": {
        "s": "0x022060ca621daeeee561b07e434134af0ddab0ec0e78e020e620b41e152e22d4",
        "r": "0x50f67216bcf15f63b52b76e23425616b0cab57a8ed4c66003358b0435fb63bdd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "162180006",
    "total": "162180006"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "162180006",
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
            "amount": "57640385083"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "162180"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMDdkM2ZiMy02ZjY5LTUwYjEtODdhNS1kZDIxMTA1ZDUzYjYifQ==",
    "nonce": 7679,
    "balances": {
      "current": "12960021067740280",
      "previous": "12960021230082466"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa76a148db5131d5c4eeae33c76a019f5599626b5",
    "nonce": 8,
    "balances": {
      "current": "162180006",
      "previous": "0"
    }
  },
  "blockNumber": "10114746",
  "created": "2020-05-22T08:58:40.312Z",
  "updated": "2020-05-22T08:58:40.383Z",
  "id": "5ec79440b0c6090011d5b2dc"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000009aaaba6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `162180006`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`