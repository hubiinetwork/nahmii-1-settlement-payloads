# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x39E7A11cb369ED7C764dc593DB46D309C675b1Ce`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000001de0f8e9540000000000000000000000000000000000000000000000000000001de0f8e954000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000001de0f8e9540000000000000000000000000000000000000000000000000000001de0f8e954762b2e4f1db0c929e3b1d9253a8fb15ec07c678791bb66a26bf258d7e48870ed20d892aebb308409b0966d13ff009ec96a797c12377bc5bbccfed73085cef31262fda696a3ed659904f47e540189552b27aa22e9bd3cd5147600651315eda48f000000000000000000000000000000000000000000000000000000000000001cd05dac0f193310b38ae3e0cd26e3f68db539120df5ba8412a71944f51b7342cbb68467d944f5e60d5d49949e25d8efae29facad2949cd65a5699f9e1c919cc2c0ecc72d748d94f95a2edb15775402f51d84ced9af3613d37d5a9c2caf3c007b5000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56610000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000149400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e2e80578bd3da000000000000000000000000000000000000000000000000002e2e9e402ae03a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000007a6230c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000045bf57a03000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5957526b4d6d45314d6931694d4451354c54566b4e47497459544130595330784f545a6b4e6d51785957457a4e32516966513d3d000000000000000000000000000000000000000000000000000000000000000b00000000000000000000000039e7a11cb369ed7c764dc593db46d309c675b1ce0000000000000000000000000000000000000000000000000000001de0f8e954000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x762b2e4f1db0c929e3b1d9253a8fb15ec07c678791bb66a26bf258d7e48870ed",
      "signature": {
        "s": "0x62fda696a3ed659904f47e540189552b27aa22e9bd3cd5147600651315eda48f",
        "r": "0x20d892aebb308409b0966d13ff009ec96a797c12377bc5bbccfed73085cef312",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd05dac0f193310b38ae3e0cd26e3f68db539120df5ba8412a71944f51b7342cb",
      "signature": {
        "s": "0x0ecc72d748d94f95a2edb15775402f51d84ced9af3613d37d5a9c2caf3c007b5",
        "r": "0xb68467d944f5e60d5d49949e25d8efae29facad2949cd65a5699f9e1c919cc2c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "128328460628",
    "total": "128328460628"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "128328460628",
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
            "amount": "18722683395"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "128328460"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmYWRkMmE1Mi1iMDQ5LTVkNGItYTA0YS0xOTZkNmQxYWEzN2QifQ==",
    "nonce": 5268,
    "balances": {
      "current": "12998977688163290",
      "previous": "12999106144952378"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x39e7a11cb369ed7c764dc593db46d309c675b1ce",
    "nonce": 11,
    "balances": {
      "current": "128328460628",
      "previous": "0"
    }
  },
  "blockNumber": "10114657",
  "created": "2020-05-22T08:39:47.312Z",
  "updated": "2020-05-22T08:39:47.372Z",
  "id": "5ec78fd3e5756b00111b8632"
}
```
* *stageAmount*: `128328460628`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000001de0f8e954000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000001de0f8e9540000000000000000000000000000000000000000000000000000001de0f8e954762b2e4f1db0c929e3b1d9253a8fb15ec07c678791bb66a26bf258d7e48870ed20d892aebb308409b0966d13ff009ec96a797c12377bc5bbccfed73085cef31262fda696a3ed659904f47e540189552b27aa22e9bd3cd5147600651315eda48f000000000000000000000000000000000000000000000000000000000000001cd05dac0f193310b38ae3e0cd26e3f68db539120df5ba8412a71944f51b7342cbb68467d944f5e60d5d49949e25d8efae29facad2949cd65a5699f9e1c919cc2c0ecc72d748d94f95a2edb15775402f51d84ced9af3613d37d5a9c2caf3c007b5000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56610000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000149400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e2e80578bd3da000000000000000000000000000000000000000000000000002e2e9e402ae03a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000007a6230c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000045bf57a03000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5957526b4d6d45314d6931694d4451354c54566b4e47497459544130595330784f545a6b4e6d51785957457a4e32516966513d3d000000000000000000000000000000000000000000000000000000000000000b00000000000000000000000039e7a11cb369ed7c764dc593db46d309c675b1ce0000000000000000000000000000000000000000000000000000001de0f8e954000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x762b2e4f1db0c929e3b1d9253a8fb15ec07c678791bb66a26bf258d7e48870ed",
      "signature": {
        "s": "0x62fda696a3ed659904f47e540189552b27aa22e9bd3cd5147600651315eda48f",
        "r": "0x20d892aebb308409b0966d13ff009ec96a797c12377bc5bbccfed73085cef312",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd05dac0f193310b38ae3e0cd26e3f68db539120df5ba8412a71944f51b7342cb",
      "signature": {
        "s": "0x0ecc72d748d94f95a2edb15775402f51d84ced9af3613d37d5a9c2caf3c007b5",
        "r": "0xb68467d944f5e60d5d49949e25d8efae29facad2949cd65a5699f9e1c919cc2c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "128328460628",
    "total": "128328460628"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "128328460628",
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
            "amount": "18722683395"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "128328460"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmYWRkMmE1Mi1iMDQ5LTVkNGItYTA0YS0xOTZkNmQxYWEzN2QifQ==",
    "nonce": 5268,
    "balances": {
      "current": "12998977688163290",
      "previous": "12999106144952378"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x39e7a11cb369ed7c764dc593db46d309c675b1ce",
    "nonce": 11,
    "balances": {
      "current": "128328460628",
      "previous": "0"
    }
  },
  "blockNumber": "10114657",
  "created": "2020-05-22T08:39:47.312Z",
  "updated": "2020-05-22T08:39:47.372Z",
  "id": "5ec78fd3e5756b00111b8632"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000001de0f8e954000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `128328460628`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`