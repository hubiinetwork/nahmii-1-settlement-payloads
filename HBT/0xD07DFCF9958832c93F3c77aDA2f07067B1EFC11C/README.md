# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xD07DFCF9958832c93F3c77aDA2f07067B1EFC11C`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000022af3b5d0000000000000000000000000000000000000000000000000000000022af3b5d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000022af3b5d0000000000000000000000000000000000000000000000000000000022af3b5d9efb8fa49a98c426c8ec58dc63479ab6becf4e8199d75677e450b82f4759ee81b0ac62f9f1391175cc27e1986e418b03ccb90172aaeac2aeccf953d3acb79a754d636fe000600da29e0a24e841c93e2fe48dea1b5a98d46f5de30be8c9aa00f2000000000000000000000000000000000000000000000000000000000000001b76a055129c83a2d5abdc9684df395af2166613786e19dd61ecd8cc39d8f7f8367c2120243031f15d52ecb32428549594daea849478e69277d882e0bd0bbd3f074ebe7de12b8e1a4b2cc33733e84dd490a8a3951eb2a860b5b151cc2e6eba9e64000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56960000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000199100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17cc64e71069000000000000000000000000000000000000000000000000002e17cc879f2cdb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000008e115000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a2a54c534000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e6d5577595751304e5330304e5749784c545534596d4d74596a45304d5331684f546c684e474d334d5759315a546b6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000d07dfcf9958832c93f3c77ada2f07067b1efc11c0000000000000000000000000000000000000000000000000000000022af3b5d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9efb8fa49a98c426c8ec58dc63479ab6becf4e8199d75677e450b82f4759ee81",
      "signature": {
        "s": "0x4d636fe000600da29e0a24e841c93e2fe48dea1b5a98d46f5de30be8c9aa00f2",
        "r": "0xb0ac62f9f1391175cc27e1986e418b03ccb90172aaeac2aeccf953d3acb79a75",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x76a055129c83a2d5abdc9684df395af2166613786e19dd61ecd8cc39d8f7f836",
      "signature": {
        "s": "0x4ebe7de12b8e1a4b2cc33733e84dd490a8a3951eb2a860b5b151cc2e6eba9e64",
        "r": "0x7c2120243031f15d52ecb32428549594daea849478e69277d882e0bd0bbd3f07",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "581909341",
    "total": "581909341"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "581909341",
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
            "amount": "43659871540"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "581909"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwNmUwYWQ0NS00NWIxLTU4YmMtYjE0MS1hOTlhNGM3MWY1ZTkifQ==",
    "nonce": 6545,
    "balances": {
      "current": "12974015562322025",
      "previous": "12974016144813275"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd07dfcf9958832c93f3c77ada2f07067b1efc11c",
    "nonce": 22,
    "balances": {
      "current": "581909341",
      "previous": "0"
    }
  },
  "blockNumber": "10114710",
  "created": "2020-05-22T08:50:00.552Z",
  "updated": "2020-05-22T08:50:00.630Z",
  "id": "5ec79238b0c6090011d5b155"
}
```
* *stageAmount*: `581909341`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000022af3b5d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000022af3b5d0000000000000000000000000000000000000000000000000000000022af3b5d9efb8fa49a98c426c8ec58dc63479ab6becf4e8199d75677e450b82f4759ee81b0ac62f9f1391175cc27e1986e418b03ccb90172aaeac2aeccf953d3acb79a754d636fe000600da29e0a24e841c93e2fe48dea1b5a98d46f5de30be8c9aa00f2000000000000000000000000000000000000000000000000000000000000001b76a055129c83a2d5abdc9684df395af2166613786e19dd61ecd8cc39d8f7f8367c2120243031f15d52ecb32428549594daea849478e69277d882e0bd0bbd3f074ebe7de12b8e1a4b2cc33733e84dd490a8a3951eb2a860b5b151cc2e6eba9e64000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56960000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000199100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17cc64e71069000000000000000000000000000000000000000000000000002e17cc879f2cdb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000008e115000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a2a54c534000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e6d5577595751304e5330304e5749784c545534596d4d74596a45304d5331684f546c684e474d334d5759315a546b6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000d07dfcf9958832c93f3c77ada2f07067b1efc11c0000000000000000000000000000000000000000000000000000000022af3b5d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9efb8fa49a98c426c8ec58dc63479ab6becf4e8199d75677e450b82f4759ee81",
      "signature": {
        "s": "0x4d636fe000600da29e0a24e841c93e2fe48dea1b5a98d46f5de30be8c9aa00f2",
        "r": "0xb0ac62f9f1391175cc27e1986e418b03ccb90172aaeac2aeccf953d3acb79a75",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x76a055129c83a2d5abdc9684df395af2166613786e19dd61ecd8cc39d8f7f836",
      "signature": {
        "s": "0x4ebe7de12b8e1a4b2cc33733e84dd490a8a3951eb2a860b5b151cc2e6eba9e64",
        "r": "0x7c2120243031f15d52ecb32428549594daea849478e69277d882e0bd0bbd3f07",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "581909341",
    "total": "581909341"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "581909341",
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
            "amount": "43659871540"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "581909"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwNmUwYWQ0NS00NWIxLTU4YmMtYjE0MS1hOTlhNGM3MWY1ZTkifQ==",
    "nonce": 6545,
    "balances": {
      "current": "12974015562322025",
      "previous": "12974016144813275"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd07dfcf9958832c93f3c77ada2f07067b1efc11c",
    "nonce": 22,
    "balances": {
      "current": "581909341",
      "previous": "0"
    }
  },
  "blockNumber": "10114710",
  "created": "2020-05-22T08:50:00.552Z",
  "updated": "2020-05-22T08:50:00.630Z",
  "id": "5ec79238b0c6090011d5b155"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000022af3b5d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `581909341`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`