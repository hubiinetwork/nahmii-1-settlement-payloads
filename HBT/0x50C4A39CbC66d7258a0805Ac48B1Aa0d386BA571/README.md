# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x50C4A39CbC66d7258a0805Ac48B1Aa0d386BA571`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000052c765740000000000000000000000000000000000000000000000000000000052c76574000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000052c765740000000000000000000000000000000000000000000000000000000052c76574141da85b549987c610f0d4c7427bfb076e716c6319530b3d57bf86cb154c91a3875707548b2a63b163e598b22de45a30cc52252c7fbd496df8c6400dbef4a4f3094608aed652b1a65cb637a98033249f830e4c45a0d7b2ba0c5c5266673d6990000000000000000000000000000000000000000000000000000000000000001b963df6248bd64a106e81625ea939e623edc5c18d9309d335168ec7b82c05423942b5f3da5c6e4248acd00f04338863dc3e27ce92aedc5e6b398e6a513107b87817c43e6f28a4b288612715dc8d58b137aa407fe856222b1cd0ce83c769a744c4000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56780000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000173900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b2d859c0ff4000000000000000000000000000000000000000000000000002e1b2dd878a66700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001530ff000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000094d1466ce000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d475a6d4e7a45315a43316d4f54526a4c5455794d7a51744f54466b4d7930774e6d466b4f5468694d6a55774e446b6966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000050c4a39cbc66d7258a0805ac48b1aa0d386ba5710000000000000000000000000000000000000000000000000000000052c76574000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x141da85b549987c610f0d4c7427bfb076e716c6319530b3d57bf86cb154c91a3",
      "signature": {
        "s": "0x094608aed652b1a65cb637a98033249f830e4c45a0d7b2ba0c5c5266673d6990",
        "r": "0x875707548b2a63b163e598b22de45a30cc52252c7fbd496df8c6400dbef4a4f3",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x963df6248bd64a106e81625ea939e623edc5c18d9309d335168ec7b82c054239",
      "signature": {
        "s": "0x17c43e6f28a4b288612715dc8d58b137aa407fe856222b1cd0ce83c769a744c4",
        "r": "0x42b5f3da5c6e4248acd00f04338863dc3e27ce92aedc5e6b398e6a513107b878",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1388799348",
    "total": "1388799348"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1388799348",
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
            "amount": "39947888334"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1388799"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlMGZmNzE1ZC1mOTRjLTUyMzQtOTFkMy0wNmFkOThiMjUwNDkifQ==",
    "nonce": 5945,
    "balances": {
      "current": "12977731257765876",
      "previous": "12977732647954023"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x50c4a39cbc66d7258a0805ac48b1aa0d386ba571",
    "nonce": 22,
    "balances": {
      "current": "1388799348",
      "previous": "0"
    }
  },
  "blockNumber": "10114680",
  "created": "2020-05-22T08:45:11.749Z",
  "updated": "2020-05-22T08:45:11.815Z",
  "id": "5ec79117b0c6090011d5b07a"
}
```
* *stageAmount*: `1388799348`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000052c76574000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000052c765740000000000000000000000000000000000000000000000000000000052c76574141da85b549987c610f0d4c7427bfb076e716c6319530b3d57bf86cb154c91a3875707548b2a63b163e598b22de45a30cc52252c7fbd496df8c6400dbef4a4f3094608aed652b1a65cb637a98033249f830e4c45a0d7b2ba0c5c5266673d6990000000000000000000000000000000000000000000000000000000000000001b963df6248bd64a106e81625ea939e623edc5c18d9309d335168ec7b82c05423942b5f3da5c6e4248acd00f04338863dc3e27ce92aedc5e6b398e6a513107b87817c43e6f28a4b288612715dc8d58b137aa407fe856222b1cd0ce83c769a744c4000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56780000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000173900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b2d859c0ff4000000000000000000000000000000000000000000000000002e1b2dd878a66700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001530ff000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000094d1466ce000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d475a6d4e7a45315a43316d4f54526a4c5455794d7a51744f54466b4d7930774e6d466b4f5468694d6a55774e446b6966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000050c4a39cbc66d7258a0805ac48b1aa0d386ba5710000000000000000000000000000000000000000000000000000000052c76574000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x141da85b549987c610f0d4c7427bfb076e716c6319530b3d57bf86cb154c91a3",
      "signature": {
        "s": "0x094608aed652b1a65cb637a98033249f830e4c45a0d7b2ba0c5c5266673d6990",
        "r": "0x875707548b2a63b163e598b22de45a30cc52252c7fbd496df8c6400dbef4a4f3",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x963df6248bd64a106e81625ea939e623edc5c18d9309d335168ec7b82c054239",
      "signature": {
        "s": "0x17c43e6f28a4b288612715dc8d58b137aa407fe856222b1cd0ce83c769a744c4",
        "r": "0x42b5f3da5c6e4248acd00f04338863dc3e27ce92aedc5e6b398e6a513107b878",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1388799348",
    "total": "1388799348"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1388799348",
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
            "amount": "39947888334"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1388799"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlMGZmNzE1ZC1mOTRjLTUyMzQtOTFkMy0wNmFkOThiMjUwNDkifQ==",
    "nonce": 5945,
    "balances": {
      "current": "12977731257765876",
      "previous": "12977732647954023"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x50c4a39cbc66d7258a0805ac48b1aa0d386ba571",
    "nonce": 22,
    "balances": {
      "current": "1388799348",
      "previous": "0"
    }
  },
  "blockNumber": "10114680",
  "created": "2020-05-22T08:45:11.749Z",
  "updated": "2020-05-22T08:45:11.815Z",
  "id": "5ec79117b0c6090011d5b07a"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000052c76574000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1388799348`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`