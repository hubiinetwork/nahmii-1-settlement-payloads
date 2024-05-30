# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xadF72F2F846EC84191D72FC2D359baBB5102305C`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000002594000000000000000000000000000000000000000000000000000000000000259400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000002594000000000000000000000000000000000000000000000000000000000000259424af10e9e6c1453e75834130a9f85aeb1145bace1716be5510c3497042f6f1d2dec0a6b5b2710a549da4c68eee7395754815f2604688c198246fe753033fb3446bf7caedfec974ecf58f184580855acc85e3dd0adff871afdf4fac0705ba2dbc000000000000000000000000000000000000000000000000000000000000001cba19515f8ee9412f28677e805b2521c243f6d080e12d09dd794c774cf8f429f49d861fd3d000fd5676ecfed1e5a210f6dfb1c4a325c54bcb5d732bea3e236ae11a14bbe2611987ad93776107ba6bcd5a440a161651e7bbfcf5527c8a65064815000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55cd000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000002f900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caea4ff8000000000000000000000000000000000000000000000000002386f2caea759500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008758b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d6d49795a6a63344f4330354e7a526d4c5455304e544d74596d4a6c5a4330354e6d457a5a5749785a6d49344e54556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000adf72f2f846ec84191d72fc2d359babb5102305c0000000000000000000000000000000000000000000000000000000000002594000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x24af10e9e6c1453e75834130a9f85aeb1145bace1716be5510c3497042f6f1d2",
      "signature": {
        "s": "0x6bf7caedfec974ecf58f184580855acc85e3dd0adff871afdf4fac0705ba2dbc",
        "r": "0xdec0a6b5b2710a549da4c68eee7395754815f2604688c198246fe753033fb344",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xba19515f8ee9412f28677e805b2521c243f6d080e12d09dd794c774cf8f429f4",
      "signature": {
        "s": "0x1a14bbe2611987ad93776107ba6bcd5a440a161651e7bbfcf5527c8a65064815",
        "r": "0x9d861fd3d000fd5676ecfed1e5a210f6dfb1c4a325c54bcb5d732bea3e236ae1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "9620",
    "total": "9620"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9620",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "554379"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "9"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiMmIyZjc4OC05NzRmLTU0NTMtYmJlZC05NmEzZWIxZmI4NTUifQ==",
    "nonce": 761,
    "balances": {
      "current": "10000001529434104",
      "previous": "10000001529443733"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xadf72f2f846ec84191d72fc2d359babb5102305c",
    "nonce": 20,
    "balances": {
      "current": "9620",
      "previous": "0"
    }
  },
  "blockNumber": "10114509",
  "created": "2020-05-22T08:04:35.137Z",
  "updated": "2020-05-22T08:04:35.207Z",
  "id": "5ec78793b0c6090011d5a9ce"
}
```
* *stageAmount*: `9620`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000259400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000002594000000000000000000000000000000000000000000000000000000000000259424af10e9e6c1453e75834130a9f85aeb1145bace1716be5510c3497042f6f1d2dec0a6b5b2710a549da4c68eee7395754815f2604688c198246fe753033fb3446bf7caedfec974ecf58f184580855acc85e3dd0adff871afdf4fac0705ba2dbc000000000000000000000000000000000000000000000000000000000000001cba19515f8ee9412f28677e805b2521c243f6d080e12d09dd794c774cf8f429f49d861fd3d000fd5676ecfed1e5a210f6dfb1c4a325c54bcb5d732bea3e236ae11a14bbe2611987ad93776107ba6bcd5a440a161651e7bbfcf5527c8a65064815000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55cd000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000002f900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caea4ff8000000000000000000000000000000000000000000000000002386f2caea759500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008758b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d6d49795a6a63344f4330354e7a526d4c5455304e544d74596d4a6c5a4330354e6d457a5a5749785a6d49344e54556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000adf72f2f846ec84191d72fc2d359babb5102305c0000000000000000000000000000000000000000000000000000000000002594000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x24af10e9e6c1453e75834130a9f85aeb1145bace1716be5510c3497042f6f1d2",
      "signature": {
        "s": "0x6bf7caedfec974ecf58f184580855acc85e3dd0adff871afdf4fac0705ba2dbc",
        "r": "0xdec0a6b5b2710a549da4c68eee7395754815f2604688c198246fe753033fb344",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xba19515f8ee9412f28677e805b2521c243f6d080e12d09dd794c774cf8f429f4",
      "signature": {
        "s": "0x1a14bbe2611987ad93776107ba6bcd5a440a161651e7bbfcf5527c8a65064815",
        "r": "0x9d861fd3d000fd5676ecfed1e5a210f6dfb1c4a325c54bcb5d732bea3e236ae1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "9620",
    "total": "9620"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9620",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "554379"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "9"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiMmIyZjc4OC05NzRmLTU0NTMtYmJlZC05NmEzZWIxZmI4NTUifQ==",
    "nonce": 761,
    "balances": {
      "current": "10000001529434104",
      "previous": "10000001529443733"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xadf72f2f846ec84191d72fc2d359babb5102305c",
    "nonce": 20,
    "balances": {
      "current": "9620",
      "previous": "0"
    }
  },
  "blockNumber": "10114509",
  "created": "2020-05-22T08:04:35.137Z",
  "updated": "2020-05-22T08:04:35.207Z",
  "id": "5ec78793b0c6090011d5a9ce"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000000000000000025940000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `9620`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``