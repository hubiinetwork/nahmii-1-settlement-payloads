# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x05fBf91E102Fe3Dff9C698b83025945EF886A16A`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000013b9d7da0000000000000000000000000000000000000000000000000000000013b9d7da000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000013b9d7da0000000000000000000000000000000000000000000000000000000013b9d7da7067032543038997de41dad51577834fa64294f139a4fe0fa90d4886c45d7eef9cb96211b1cde204a373f9500a91a718e8578e76b7eae60b59eb919730936b240fc0d2ecf46cca9db61b4c9af756fb5740674d717984e2dc686ffebfd083af9a000000000000000000000000000000000000000000000000000000000000001bcbf87fe925a462e67c8764fd489d0fe3304bf5774104da04a7aac18948ae2d3b5b881c0fd9a5bb495c88bd7b13787adb0f80df972af6fbf5e482b2aa4f37ded041e95b4e6f9def0d2f088e31dc456b540ea4fcb964be3aed04d106c1e57d04bb000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5682000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000017ea00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b0de1b7dad7000000000000000000000000000000000000000000000000002e1b0df576bf7300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000050cc2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009552be6a9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d57466c4d5451354d79316d4d6a41794c5456684f5749744f5463314e79316c4d5441324d6a49794e474a6d4e474d6966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000005fbf91e102fe3dff9c698b83025945ef886a16a0000000000000000000000000000000000000000000000000000000013b9d7da000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7067032543038997de41dad51577834fa64294f139a4fe0fa90d4886c45d7eef",
      "signature": {
        "s": "0x0fc0d2ecf46cca9db61b4c9af756fb5740674d717984e2dc686ffebfd083af9a",
        "r": "0x9cb96211b1cde204a373f9500a91a718e8578e76b7eae60b59eb919730936b24",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xcbf87fe925a462e67c8764fd489d0fe3304bf5774104da04a7aac18948ae2d3b",
      "signature": {
        "s": "0x41e95b4e6f9def0d2f088e31dc456b540ea4fcb964be3aed04d106c1e57d04bb",
        "r": "0x5b881c0fd9a5bb495c88bd7b13787adb0f80df972af6fbf5e482b2aa4f37ded0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "330946522",
    "total": "330946522"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "330946522",
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
            "amount": "40083646121"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "330946"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MWFlMTQ5My1mMjAyLTVhOWItOTc1Ny1lMTA2MjIyNGJmNGMifQ==",
    "nonce": 6122,
    "balances": {
      "current": "12977595364137687",
      "previous": "12977595695415155"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x05fbf91e102fe3dff9c698b83025945ef886a16a",
    "nonce": 22,
    "balances": {
      "current": "330946522",
      "previous": "0"
    }
  },
  "blockNumber": "10114690",
  "created": "2020-05-22T08:46:38.829Z",
  "updated": "2020-05-22T08:46:38.898Z",
  "id": "5ec7916eb0c6090011d5b0be"
}
```
* *stageAmount*: `330946522`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000013b9d7da000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000013b9d7da0000000000000000000000000000000000000000000000000000000013b9d7da7067032543038997de41dad51577834fa64294f139a4fe0fa90d4886c45d7eef9cb96211b1cde204a373f9500a91a718e8578e76b7eae60b59eb919730936b240fc0d2ecf46cca9db61b4c9af756fb5740674d717984e2dc686ffebfd083af9a000000000000000000000000000000000000000000000000000000000000001bcbf87fe925a462e67c8764fd489d0fe3304bf5774104da04a7aac18948ae2d3b5b881c0fd9a5bb495c88bd7b13787adb0f80df972af6fbf5e482b2aa4f37ded041e95b4e6f9def0d2f088e31dc456b540ea4fcb964be3aed04d106c1e57d04bb000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5682000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000017ea00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b0de1b7dad7000000000000000000000000000000000000000000000000002e1b0df576bf7300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000050cc2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009552be6a9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d57466c4d5451354d79316d4d6a41794c5456684f5749744f5463314e79316c4d5441324d6a49794e474a6d4e474d6966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000005fbf91e102fe3dff9c698b83025945ef886a16a0000000000000000000000000000000000000000000000000000000013b9d7da000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7067032543038997de41dad51577834fa64294f139a4fe0fa90d4886c45d7eef",
      "signature": {
        "s": "0x0fc0d2ecf46cca9db61b4c9af756fb5740674d717984e2dc686ffebfd083af9a",
        "r": "0x9cb96211b1cde204a373f9500a91a718e8578e76b7eae60b59eb919730936b24",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xcbf87fe925a462e67c8764fd489d0fe3304bf5774104da04a7aac18948ae2d3b",
      "signature": {
        "s": "0x41e95b4e6f9def0d2f088e31dc456b540ea4fcb964be3aed04d106c1e57d04bb",
        "r": "0x5b881c0fd9a5bb495c88bd7b13787adb0f80df972af6fbf5e482b2aa4f37ded0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "330946522",
    "total": "330946522"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "330946522",
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
            "amount": "40083646121"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "330946"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MWFlMTQ5My1mMjAyLTVhOWItOTc1Ny1lMTA2MjIyNGJmNGMifQ==",
    "nonce": 6122,
    "balances": {
      "current": "12977595364137687",
      "previous": "12977595695415155"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x05fbf91e102fe3dff9c698b83025945ef886a16a",
    "nonce": 22,
    "balances": {
      "current": "330946522",
      "previous": "0"
    }
  },
  "blockNumber": "10114690",
  "created": "2020-05-22T08:46:38.829Z",
  "updated": "2020-05-22T08:46:38.898Z",
  "id": "5ec7916eb0c6090011d5b0be"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000013b9d7da000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `330946522`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`