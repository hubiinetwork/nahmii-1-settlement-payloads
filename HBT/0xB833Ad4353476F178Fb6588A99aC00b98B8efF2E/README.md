# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xB833Ad4353476F178Fb6588A99aC00b98B8efF2E`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000892d000000000000000000000000000000000000000000000000000000000000892d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000892d000000000000000000000000000000000000000000000000000000000000892d534407b7f8524c591a486cb5d58ac75774c0739f75d93a2296a9999b0aeae7c2c103bfcd19849b85142dec23b92ea9f31f23f6bc751d252642ab3ba3c51ca63b4cd5b1426a31b6c7790cf216293776683968507892728c83cb00be59b2403c4c000000000000000000000000000000000000000000000000000000000000001ce510d6c4ad73a9da49e16e68ba2a59b70d3f2977ad77dd4d455aa72fda668e9bb3e2249305f3416b75a4bbb4921baf4deef1048ed5bb415b9a04d6dd7897c9615ad860821eaf288b55e25088596a20b1cb5d694073035fc290f6457c5f99e75b000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001db300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b21cd3833e5000000000000000000000000000000000000000000000000002e0b21cd38bd3500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000023000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d679b02f5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684f474d7a4f4745795a533033597a686c4c54566d4f475174595455784e6930354d6d5534596a6733596a4a6d4d544d6966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000b833ad4353476f178fb6588a99ac00b98b8eff2e000000000000000000000000000000000000000000000000000000000000892d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x534407b7f8524c591a486cb5d58ac75774c0739f75d93a2296a9999b0aeae7c2",
      "signature": {
        "s": "0x4cd5b1426a31b6c7790cf216293776683968507892728c83cb00be59b2403c4c",
        "r": "0xc103bfcd19849b85142dec23b92ea9f31f23f6bc751d252642ab3ba3c51ca63b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe510d6c4ad73a9da49e16e68ba2a59b70d3f2977ad77dd4d455aa72fda668e9b",
      "signature": {
        "s": "0x5ad860821eaf288b55e25088596a20b1cb5d694073035fc290f6457c5f99e75b",
        "r": "0xb3e2249305f3416b75a4bbb4921baf4deef1048ed5bb415b9a04d6dd7897c961",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "35117",
    "total": "35117"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "35117",
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
            "amount": "57572786933"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "35"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhOGMzOGEyZS03YzhlLTVmOGQtYTUxNi05MmU4Yjg3YjJmMTMifQ==",
    "nonce": 7603,
    "balances": {
      "current": "12960088733529061",
      "previous": "12960088733564213"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb833ad4353476f178fb6588a99ac00b98b8eff2e",
    "nonce": 4,
    "balances": {
      "current": "35117",
      "previous": "0"
    }
  },
  "blockNumber": "10114744",
  "created": "2020-05-22T08:57:57.484Z",
  "updated": "2020-05-22T08:57:57.558Z",
  "id": "5ec79415005df800101bcc28"
}
```
* *stageAmount*: `35117`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000892d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000892d000000000000000000000000000000000000000000000000000000000000892d534407b7f8524c591a486cb5d58ac75774c0739f75d93a2296a9999b0aeae7c2c103bfcd19849b85142dec23b92ea9f31f23f6bc751d252642ab3ba3c51ca63b4cd5b1426a31b6c7790cf216293776683968507892728c83cb00be59b2403c4c000000000000000000000000000000000000000000000000000000000000001ce510d6c4ad73a9da49e16e68ba2a59b70d3f2977ad77dd4d455aa72fda668e9bb3e2249305f3416b75a4bbb4921baf4deef1048ed5bb415b9a04d6dd7897c9615ad860821eaf288b55e25088596a20b1cb5d694073035fc290f6457c5f99e75b000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001db300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b21cd3833e5000000000000000000000000000000000000000000000000002e0b21cd38bd3500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000023000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d679b02f5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684f474d7a4f4745795a533033597a686c4c54566d4f475174595455784e6930354d6d5534596a6733596a4a6d4d544d6966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000b833ad4353476f178fb6588a99ac00b98b8eff2e000000000000000000000000000000000000000000000000000000000000892d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x534407b7f8524c591a486cb5d58ac75774c0739f75d93a2296a9999b0aeae7c2",
      "signature": {
        "s": "0x4cd5b1426a31b6c7790cf216293776683968507892728c83cb00be59b2403c4c",
        "r": "0xc103bfcd19849b85142dec23b92ea9f31f23f6bc751d252642ab3ba3c51ca63b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe510d6c4ad73a9da49e16e68ba2a59b70d3f2977ad77dd4d455aa72fda668e9b",
      "signature": {
        "s": "0x5ad860821eaf288b55e25088596a20b1cb5d694073035fc290f6457c5f99e75b",
        "r": "0xb3e2249305f3416b75a4bbb4921baf4deef1048ed5bb415b9a04d6dd7897c961",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "35117",
    "total": "35117"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "35117",
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
            "amount": "57572786933"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "35"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhOGMzOGEyZS03YzhlLTVmOGQtYTUxNi05MmU4Yjg3YjJmMTMifQ==",
    "nonce": 7603,
    "balances": {
      "current": "12960088733529061",
      "previous": "12960088733564213"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb833ad4353476f178fb6588a99ac00b98b8eff2e",
    "nonce": 4,
    "balances": {
      "current": "35117",
      "previous": "0"
    }
  },
  "blockNumber": "10114744",
  "created": "2020-05-22T08:57:57.484Z",
  "updated": "2020-05-22T08:57:57.558Z",
  "id": "5ec79415005df800101bcc28"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000892d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `35117`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`