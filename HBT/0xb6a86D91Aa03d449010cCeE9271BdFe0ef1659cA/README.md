# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb6a86D91Aa03d449010cCeE9271BdFe0ef1659cA`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000081f99f960000000000000000000000000000000000000000000000000000000081f99f96000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000081f99f960000000000000000000000000000000000000000000000000000000081f99f960c6c44ebfcddb88f69664b9d7e598c5ecfce596a330d49c1699db53de6cde702638f0a65e5ca788857c0a2f405e5f2691ce4c389a06c36533431baa6994121a160dd1ac3ef5d68bcbaaadd8fef69a60d602bcad82acd2ca74f1abb9f876d0cef000000000000000000000000000000000000000000000000000000000000001bf467c62ca6b6f55a631c42198c5e6a1db08fc9864f9911b330faaa89255cc6352e6bb66379d59d160c98fe7265c3c3e79f0e4ae4ba42f4f6a3fc57aa34999d246e418474e9cce502419989ed740d85d118b5caefe3de310f4d5b0abfbf297382000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56600000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000147000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e324109c45766000000000000000000000000000000000000000000000000002e32418bdf3d0800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000021460c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000366443091000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a444d344e5745354e6930354f4446684c5455794d6a63744f5455355a69316a597a52684e546b795a6a49334e7a496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000b6a86d91aa03d449010ccee9271bdfe0ef1659ca0000000000000000000000000000000000000000000000000000000081f99f96000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0c6c44ebfcddb88f69664b9d7e598c5ecfce596a330d49c1699db53de6cde702",
      "signature": {
        "s": "0x60dd1ac3ef5d68bcbaaadd8fef69a60d602bcad82acd2ca74f1abb9f876d0cef",
        "r": "0x638f0a65e5ca788857c0a2f405e5f2691ce4c389a06c36533431baa6994121a1",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf467c62ca6b6f55a631c42198c5e6a1db08fc9864f9911b330faaa89255cc635",
      "signature": {
        "s": "0x6e418474e9cce502419989ed740d85d118b5caefe3de310f4d5b0abfbf297382",
        "r": "0x2e6bb66379d59d160c98fe7265c3c3e79f0e4ae4ba42f4f6a3fc57aa34999d24",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2180620182",
    "total": "2180620182"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2180620182",
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
            "amount": "14600646801"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2180620"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZDM4NWE5Ni05ODFhLTUyMjctOTU5Zi1jYzRhNTkyZjI3NzIifQ==",
    "nonce": 5232,
    "balances": {
      "current": "13003103846815590",
      "previous": "13003106029616392"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb6a86d91aa03d449010ccee9271bdfe0ef1659ca",
    "nonce": 22,
    "balances": {
      "current": "2180620182",
      "previous": "0"
    }
  },
  "blockNumber": "10114656",
  "created": "2020-05-22T08:39:32.071Z",
  "updated": "2020-05-22T08:39:33.153Z",
  "id": "5ec78fc4b0c6090011d5af91"
}
```
* *stageAmount*: `2180620182`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000081f99f96000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000081f99f960000000000000000000000000000000000000000000000000000000081f99f960c6c44ebfcddb88f69664b9d7e598c5ecfce596a330d49c1699db53de6cde702638f0a65e5ca788857c0a2f405e5f2691ce4c389a06c36533431baa6994121a160dd1ac3ef5d68bcbaaadd8fef69a60d602bcad82acd2ca74f1abb9f876d0cef000000000000000000000000000000000000000000000000000000000000001bf467c62ca6b6f55a631c42198c5e6a1db08fc9864f9911b330faaa89255cc6352e6bb66379d59d160c98fe7265c3c3e79f0e4ae4ba42f4f6a3fc57aa34999d246e418474e9cce502419989ed740d85d118b5caefe3de310f4d5b0abfbf297382000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56600000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000147000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e324109c45766000000000000000000000000000000000000000000000000002e32418bdf3d0800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000021460c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000366443091000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a444d344e5745354e6930354f4446684c5455794d6a63744f5455355a69316a597a52684e546b795a6a49334e7a496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000b6a86d91aa03d449010ccee9271bdfe0ef1659ca0000000000000000000000000000000000000000000000000000000081f99f96000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0c6c44ebfcddb88f69664b9d7e598c5ecfce596a330d49c1699db53de6cde702",
      "signature": {
        "s": "0x60dd1ac3ef5d68bcbaaadd8fef69a60d602bcad82acd2ca74f1abb9f876d0cef",
        "r": "0x638f0a65e5ca788857c0a2f405e5f2691ce4c389a06c36533431baa6994121a1",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf467c62ca6b6f55a631c42198c5e6a1db08fc9864f9911b330faaa89255cc635",
      "signature": {
        "s": "0x6e418474e9cce502419989ed740d85d118b5caefe3de310f4d5b0abfbf297382",
        "r": "0x2e6bb66379d59d160c98fe7265c3c3e79f0e4ae4ba42f4f6a3fc57aa34999d24",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2180620182",
    "total": "2180620182"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2180620182",
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
            "amount": "14600646801"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2180620"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZDM4NWE5Ni05ODFhLTUyMjctOTU5Zi1jYzRhNTkyZjI3NzIifQ==",
    "nonce": 5232,
    "balances": {
      "current": "13003103846815590",
      "previous": "13003106029616392"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb6a86d91aa03d449010ccee9271bdfe0ef1659ca",
    "nonce": 22,
    "balances": {
      "current": "2180620182",
      "previous": "0"
    }
  },
  "blockNumber": "10114656",
  "created": "2020-05-22T08:39:32.071Z",
  "updated": "2020-05-22T08:39:33.153Z",
  "id": "5ec78fc4b0c6090011d5af91"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000081f99f96000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2180620182`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`