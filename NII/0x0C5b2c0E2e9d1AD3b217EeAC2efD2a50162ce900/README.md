# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0C5b2c0E2e9d1AD3b217EeAC2efD2a50162ce900`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000057bfb0e369d27ddbc0000000000000000000000000000000000000000000000000000000106ac4af50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000106ac4af5000000000000000000000000000000000000000000000002ef3517eb787b95e0d6fe74439f056c091b37fc93e9be8ba77df6d72e8c5a31ea48f8069c6e92014054d81fb836adf40cbac02283588c85cfcb65c1ea089e330540be5b2f2ec6155a7c8b658947b691901a2bebe95551a53d1acbae9500ca7f6b89459da0f7f77133000000000000000000000000000000000000000000000000000000000000001b1ef39afe44adb85c4ee1a18fa54f5d581785cc0d1b9bd2cba291a5a7e6a8f0d341fb00dc1bdde269497a80474c56dfdc1706b2910b7b77f803016bded83de3792fea04fa99d039dbcd4c0607a0270266b8b7873c480ff04bb21d60fc4dd098f7000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074cd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aebd000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095e26d8aaf90e881d5190000000000000000000000000000000000000000000095e26d8aaf91ef715e9700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000433e890000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c60cf9d87d7f661a700000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d6a55314d7a557a596930324e4455794c545669596a6b7459544268596930344e57497a5a44686b4d5759355a6a4d6966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000000c5b2c0e2e9d1ad3b217eeac2efd2a50162ce9000000000000000000000000000000000000000000000000057bfb0e369d27ddbc0000000000000000000000000000000000000000000000057bfb0e35967b92c700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd6fe74439f056c091b37fc93e9be8ba77df6d72e8c5a31ea48f8069c6e920140",
      "signature": {
        "s": "0x7c8b658947b691901a2bebe95551a53d1acbae9500ca7f6b89459da0f7f77133",
        "r": "0x54d81fb836adf40cbac02283588c85cfcb65c1ea089e330540be5b2f2ec6155a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x1ef39afe44adb85c4ee1a18fa54f5d581785cc0d1b9bd2cba291a5a7e6a8f0d3",
      "signature": {
        "s": "0x2fea04fa99d039dbcd4c0607a0270266b8b7873c480ff04bb21d60fc4dd098f7",
        "r": "0x41fb00dc1bdde269497a80474c56dfdc1706b2910b7b77f803016bded83de379",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4406921973",
    "total": "54130197596355663328"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4406921973",
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
            "amount": "27265222757373893286512"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4406921"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjMjU1MzUzYi02NDUyLTViYjktYTBhYi04NWIzZDhkMWY5ZjMifQ==",
    "nonce": 110269,
    "balances": {
      "current": "707809463422569326695705",
      "previous": "707809463422573738024599"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0c5b2c0e2e9d1ad3b217eeac2efd2a50162ce900",
    "nonce": 46,
    "balances": {
      "current": "101167470282094927292",
      "previous": "101167470277688005319"
    }
  },
  "blockNumber": "14709965",
  "created": "2022-05-04T08:52:25.363Z",
  "updated": "2022-05-04T08:52:25.426Z",
  "id": "62723ec97832e20011830b7e"
}
```
* *stageAmount*: `101167470282094927292`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000106ac4af50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000106ac4af5000000000000000000000000000000000000000000000002ef3517eb787b95e0d6fe74439f056c091b37fc93e9be8ba77df6d72e8c5a31ea48f8069c6e92014054d81fb836adf40cbac02283588c85cfcb65c1ea089e330540be5b2f2ec6155a7c8b658947b691901a2bebe95551a53d1acbae9500ca7f6b89459da0f7f77133000000000000000000000000000000000000000000000000000000000000001b1ef39afe44adb85c4ee1a18fa54f5d581785cc0d1b9bd2cba291a5a7e6a8f0d341fb00dc1bdde269497a80474c56dfdc1706b2910b7b77f803016bded83de3792fea04fa99d039dbcd4c0607a0270266b8b7873c480ff04bb21d60fc4dd098f7000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074cd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aebd000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095e26d8aaf90e881d5190000000000000000000000000000000000000000000095e26d8aaf91ef715e9700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000433e890000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c60cf9d87d7f661a700000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d6a55314d7a557a596930324e4455794c545669596a6b7459544268596930344e57497a5a44686b4d5759355a6a4d6966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000000c5b2c0e2e9d1ad3b217eeac2efd2a50162ce9000000000000000000000000000000000000000000000000057bfb0e369d27ddbc0000000000000000000000000000000000000000000000057bfb0e35967b92c700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd6fe74439f056c091b37fc93e9be8ba77df6d72e8c5a31ea48f8069c6e920140",
      "signature": {
        "s": "0x7c8b658947b691901a2bebe95551a53d1acbae9500ca7f6b89459da0f7f77133",
        "r": "0x54d81fb836adf40cbac02283588c85cfcb65c1ea089e330540be5b2f2ec6155a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x1ef39afe44adb85c4ee1a18fa54f5d581785cc0d1b9bd2cba291a5a7e6a8f0d3",
      "signature": {
        "s": "0x2fea04fa99d039dbcd4c0607a0270266b8b7873c480ff04bb21d60fc4dd098f7",
        "r": "0x41fb00dc1bdde269497a80474c56dfdc1706b2910b7b77f803016bded83de379",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4406921973",
    "total": "54130197596355663328"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4406921973",
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
            "amount": "27265222757373893286512"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4406921"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjMjU1MzUzYi02NDUyLTViYjktYTBhYi04NWIzZDhkMWY5ZjMifQ==",
    "nonce": 110269,
    "balances": {
      "current": "707809463422569326695705",
      "previous": "707809463422573738024599"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0c5b2c0e2e9d1ad3b217eeac2efd2a50162ce900",
    "nonce": 46,
    "balances": {
      "current": "101167470282094927292",
      "previous": "101167470277688005319"
    }
  },
  "blockNumber": "14709965",
  "created": "2022-05-04T08:52:25.363Z",
  "updated": "2022-05-04T08:52:25.426Z",
  "id": "62723ec97832e20011830b7e"
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
0x0f200f9b0000000000000000000000000000000000000000000000057bfb0e369d27ddbc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `101167470282094927292`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`