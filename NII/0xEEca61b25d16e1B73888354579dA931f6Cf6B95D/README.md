# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xEEca61b25d16e1B73888354579dA931f6Cf6B95D`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000029af6b09fa7f000000000000000000000000000000000000000000000000000000fd01dba7800000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000fd01dba78000000000000000000000000000000000000000000000000000001bbba130fef0d759649d856be1eab99bb8d37397234a1629e4dc229ed7be8565b320c1b84609e8d4ddd99a40ab92423822d6250df36b4d9dab63475c25c1c7aac4bc2c6c01801ec5dda1441729204611ef5bed1c014dcb6fd3beefc99aaff2ba282620ea4f38000000000000000000000000000000000000000000000000000000000000001c368634e0e2cbe3a2d5cc89a16418b9bc794e94df64c40735375e32599838fb4f2f3fcea846437d21dd369fafd523e6bde2b914e4d12926dff2027d93d2ca1dd928e7e4ebdd84e0a589920dcdddfbbb97d9652b2d1cd87eb7514546a0cfb92b4e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af95000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000005384783568fce46b62ef000000000000000000000000000000000000000000005384783569fa270c1fd900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000040c5156a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d7060f69d2cef07b470000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e4449335a6a64684e7930354d7a59784c5456694e6a4574595463345a53316d4e6d45774d54646c4d446b355a544d6966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000eeca61b25d16e1b73888354579da931f6cf6b95d000000000000000000000000000000000000000000000000000029af6b09fa7f000000000000000000000000000000000000000000000000000028b2692e52ff00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd759649d856be1eab99bb8d37397234a1629e4dc229ed7be8565b320c1b84609",
      "signature": {
        "s": "0x1ec5dda1441729204611ef5bed1c014dcb6fd3beefc99aaff2ba282620ea4f38",
        "r": "0xe8d4ddd99a40ab92423822d6250df36b4d9dab63475c25c1c7aac4bc2c6c0180",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x368634e0e2cbe3a2d5cc89a16418b9bc794e94df64c40735375e32599838fb4f",
      "signature": {
        "s": "0x28e7e4ebdd84e0a589920dcdddfbbb97d9652b2d1cd87eb7514546a0cfb92b4e",
        "r": "0x2f3fcea846437d21dd369fafd523e6bde2b914e4d12926dff2027d93d2ca1dd9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1086657898368",
    "total": "30492677177072"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1086657898368",
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
            "amount": "27578319074238793808711"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1086657898"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkNDI3ZjdhNy05MzYxLTViNjEtYTc4ZS1mNmEwMTdlMDk5ZTMifQ==",
    "nonce": 110485,
    "balances": {
      "current": "394400050240803903857391",
      "previous": "394400050241891648413657"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xeeca61b25d16e1b73888354579da931f6cf6b95d",
    "nonce": 45,
    "balances": {
      "current": "45833391831679",
      "previous": "44746733933311"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:31.742Z",
  "updated": "2022-05-04T08:53:31.813Z",
  "id": "62723f0bbbd75600116d0579"
}
```
* *stageAmount*: `45833391831679`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000fd01dba7800000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000fd01dba78000000000000000000000000000000000000000000000000000001bbba130fef0d759649d856be1eab99bb8d37397234a1629e4dc229ed7be8565b320c1b84609e8d4ddd99a40ab92423822d6250df36b4d9dab63475c25c1c7aac4bc2c6c01801ec5dda1441729204611ef5bed1c014dcb6fd3beefc99aaff2ba282620ea4f38000000000000000000000000000000000000000000000000000000000000001c368634e0e2cbe3a2d5cc89a16418b9bc794e94df64c40735375e32599838fb4f2f3fcea846437d21dd369fafd523e6bde2b914e4d12926dff2027d93d2ca1dd928e7e4ebdd84e0a589920dcdddfbbb97d9652b2d1cd87eb7514546a0cfb92b4e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af95000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000005384783568fce46b62ef000000000000000000000000000000000000000000005384783569fa270c1fd900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000040c5156a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d7060f69d2cef07b470000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e4449335a6a64684e7930354d7a59784c5456694e6a4574595463345a53316d4e6d45774d54646c4d446b355a544d6966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000eeca61b25d16e1b73888354579da931f6cf6b95d000000000000000000000000000000000000000000000000000029af6b09fa7f000000000000000000000000000000000000000000000000000028b2692e52ff00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd759649d856be1eab99bb8d37397234a1629e4dc229ed7be8565b320c1b84609",
      "signature": {
        "s": "0x1ec5dda1441729204611ef5bed1c014dcb6fd3beefc99aaff2ba282620ea4f38",
        "r": "0xe8d4ddd99a40ab92423822d6250df36b4d9dab63475c25c1c7aac4bc2c6c0180",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x368634e0e2cbe3a2d5cc89a16418b9bc794e94df64c40735375e32599838fb4f",
      "signature": {
        "s": "0x28e7e4ebdd84e0a589920dcdddfbbb97d9652b2d1cd87eb7514546a0cfb92b4e",
        "r": "0x2f3fcea846437d21dd369fafd523e6bde2b914e4d12926dff2027d93d2ca1dd9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1086657898368",
    "total": "30492677177072"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1086657898368",
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
            "amount": "27578319074238793808711"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1086657898"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkNDI3ZjdhNy05MzYxLTViNjEtYTc4ZS1mNmEwMTdlMDk5ZTMifQ==",
    "nonce": 110485,
    "balances": {
      "current": "394400050240803903857391",
      "previous": "394400050241891648413657"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xeeca61b25d16e1b73888354579da931f6cf6b95d",
    "nonce": 45,
    "balances": {
      "current": "45833391831679",
      "previous": "44746733933311"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:31.742Z",
  "updated": "2022-05-04T08:53:31.813Z",
  "id": "62723f0bbbd75600116d0579"
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
0x0f200f9b000000000000000000000000000000000000000000000000000029af6b09fa7f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `45833391831679`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`