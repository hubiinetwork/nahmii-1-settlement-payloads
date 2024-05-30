# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2CA269dab0a70BEB8bef6fa96E630475c91D8db6`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000fc21830000000000000000000000000000000000000000000000000000000000fc2183000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000fc21830000000000000000000000000000000000000000000000000000000000fc2183b49264fd40b5f292d6b80654477aabfb78c23e3d79d43fae63a2669c0645c65b69bf40a6c2012d08a94f2382a4eec76bb8640ff91cd9fab01dd95a292fd07989411ef603ac109e0efebfe0f0359a983fcfeed9aaae0dca6e8eeec08f33d3cc36000000000000000000000000000000000000000000000000000000000000001b14824abd115aff520c1767cdf91b361d362ef996c08d8ae50ae120c57175d0faa54732ad6d9aa635234dc055ce5dfd3eae47b26441258c06dc5f4191fb11113f7abc79da74ff44411ca0922e1eb8dcb370c4289c46f90edc959167deb9c22c34000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a566a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000158c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d5f73cf92c7000000000000000000000000000000000000000000000000002e1d5f74cbf4d500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000408b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008bd5e84b6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935595456695a57466a4e53307a5932566c4c5455775a4451744f546b7959793079597a51794d6a426c597a6b345a54676966513d3d00000000000000000000000000000000000000000000000000000000000000060000000000000000000000002ca269dab0a70beb8bef6fa96e630475c91d8db60000000000000000000000000000000000000000000000000000000000fc2183000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb49264fd40b5f292d6b80654477aabfb78c23e3d79d43fae63a2669c0645c65b",
      "signature": {
        "s": "0x411ef603ac109e0efebfe0f0359a983fcfeed9aaae0dca6e8eeec08f33d3cc36",
        "r": "0x69bf40a6c2012d08a94f2382a4eec76bb8640ff91cd9fab01dd95a292fd07989",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x14824abd115aff520c1767cdf91b361d362ef996c08d8ae50ae120c57175d0fa",
      "signature": {
        "s": "0x7abc79da74ff44411ca0922e1eb8dcb370c4289c46f90edc959167deb9c22c34",
        "r": "0xa54732ad6d9aa635234dc055ce5dfd3eae47b26441258c06dc5f4191fb11113f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "16523651",
    "total": "16523651"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16523651",
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
            "amount": "37536826550"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "16523"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5YTViZWFjNS0zY2VlLTUwZDQtOTkyYy0yYzQyMjBlYzk4ZTgifQ==",
    "nonce": 5516,
    "balances": {
      "current": "12980144730772167",
      "previous": "12980144747312341"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2ca269dab0a70beb8bef6fa96e630475c91d8db6",
    "nonce": 6,
    "balances": {
      "current": "16523651",
      "previous": "0"
    }
  },
  "blockNumber": "10114666",
  "created": "2020-05-22T08:41:49.353Z",
  "updated": "2020-05-22T08:41:49.430Z",
  "id": "5ec7904db0c6090011d5aff2"
}
```
* *stageAmount*: `16523651`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000fc2183000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000fc21830000000000000000000000000000000000000000000000000000000000fc2183b49264fd40b5f292d6b80654477aabfb78c23e3d79d43fae63a2669c0645c65b69bf40a6c2012d08a94f2382a4eec76bb8640ff91cd9fab01dd95a292fd07989411ef603ac109e0efebfe0f0359a983fcfeed9aaae0dca6e8eeec08f33d3cc36000000000000000000000000000000000000000000000000000000000000001b14824abd115aff520c1767cdf91b361d362ef996c08d8ae50ae120c57175d0faa54732ad6d9aa635234dc055ce5dfd3eae47b26441258c06dc5f4191fb11113f7abc79da74ff44411ca0922e1eb8dcb370c4289c46f90edc959167deb9c22c34000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a566a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000158c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d5f73cf92c7000000000000000000000000000000000000000000000000002e1d5f74cbf4d500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000408b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008bd5e84b6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935595456695a57466a4e53307a5932566c4c5455775a4451744f546b7959793079597a51794d6a426c597a6b345a54676966513d3d00000000000000000000000000000000000000000000000000000000000000060000000000000000000000002ca269dab0a70beb8bef6fa96e630475c91d8db60000000000000000000000000000000000000000000000000000000000fc2183000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb49264fd40b5f292d6b80654477aabfb78c23e3d79d43fae63a2669c0645c65b",
      "signature": {
        "s": "0x411ef603ac109e0efebfe0f0359a983fcfeed9aaae0dca6e8eeec08f33d3cc36",
        "r": "0x69bf40a6c2012d08a94f2382a4eec76bb8640ff91cd9fab01dd95a292fd07989",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x14824abd115aff520c1767cdf91b361d362ef996c08d8ae50ae120c57175d0fa",
      "signature": {
        "s": "0x7abc79da74ff44411ca0922e1eb8dcb370c4289c46f90edc959167deb9c22c34",
        "r": "0xa54732ad6d9aa635234dc055ce5dfd3eae47b26441258c06dc5f4191fb11113f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "16523651",
    "total": "16523651"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16523651",
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
            "amount": "37536826550"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "16523"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5YTViZWFjNS0zY2VlLTUwZDQtOTkyYy0yYzQyMjBlYzk4ZTgifQ==",
    "nonce": 5516,
    "balances": {
      "current": "12980144730772167",
      "previous": "12980144747312341"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2ca269dab0a70beb8bef6fa96e630475c91d8db6",
    "nonce": 6,
    "balances": {
      "current": "16523651",
      "previous": "0"
    }
  },
  "blockNumber": "10114666",
  "created": "2020-05-22T08:41:49.353Z",
  "updated": "2020-05-22T08:41:49.430Z",
  "id": "5ec7904db0c6090011d5aff2"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000fc2183000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `16523651`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`