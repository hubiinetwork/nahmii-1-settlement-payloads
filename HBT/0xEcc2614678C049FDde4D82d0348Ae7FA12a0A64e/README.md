# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xEcc2614678C049FDde4D82d0348Ae7FA12a0A64e`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000001b000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000001b000000000000000000000000000000000000000000000000000000000000001b0987997ccca3786cb0d7b85b9bd22be7df5e9568213970c20aa4a1497acc33cc50893f5bfc53e08779ef1bb1ba7e24830a0c468116737926f816fe9290a9cef313f88283a2946e97a56a56213b468f549b89e38f7c8ff02ea87916aad9d548e49000000000000000000000000000000000000000000000000000000000000001b4ddc03ef9dd99b988dcfb64a83fe0d4ee8e51ca94dffdb044c9bf448513119f19e293cc53d4c98db7012fdee5b6aaf2276be7792b4080979797583b36845d4cb1df88a0e0e746cb0e9832f33bb8591f49d6bf5efd202ffb8bb1944c6cc146c79000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56710000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000161600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1cfadcb5ae96000000000000000000000000000000000000000000000000002e1cfadcb5b04700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008d71836d8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774d6a4d784d475a6a4d7930354e5449784c54566d5a4749744f44646b4e7930354e544d354f5751314d544a6d4d32496966513d3d0000000000000000000000000000000000000000000000000000000000000015000000000000000000000000ecc2614678c049fdde4d82d0348ae7fa12a0a64e00000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x987997ccca3786cb0d7b85b9bd22be7df5e9568213970c20aa4a1497acc33cc5",
      "signature": {
        "s": "0x3f88283a2946e97a56a56213b468f549b89e38f7c8ff02ea87916aad9d548e49",
        "r": "0x0893f5bfc53e08779ef1bb1ba7e24830a0c468116737926f816fe9290a9cef31",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4ddc03ef9dd99b988dcfb64a83fe0d4ee8e51ca94dffdb044c9bf448513119f1",
      "signature": {
        "s": "0x1df88a0e0e746cb0e9832f33bb8591f49d6bf5efd202ffb8bb1944c6cc146c79",
        "r": "0x9e293cc53d4c98db7012fdee5b6aaf2276be7792b4080979797583b36845d4cb",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "432",
    "total": "432"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "432",
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
            "amount": "37968426712"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwMjMxMGZjMy05NTIxLTVmZGItODdkNy05NTM5OWQ1MTJmM2IifQ==",
    "nonce": 5654,
    "balances": {
      "current": "12979712698986134",
      "previous": "12979712698986567"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xecc2614678c049fdde4d82d0348ae7fa12a0a64e",
    "nonce": 21,
    "balances": {
      "current": "432",
      "previous": "0"
    }
  },
  "blockNumber": "10114673",
  "created": "2020-05-22T08:42:52.358Z",
  "updated": "2020-05-22T08:42:52.440Z",
  "id": "5ec7908c005df800101bc99a"
}
```
* *stageAmount*: `432`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000001b000000000000000000000000000000000000000000000000000000000000001b0987997ccca3786cb0d7b85b9bd22be7df5e9568213970c20aa4a1497acc33cc50893f5bfc53e08779ef1bb1ba7e24830a0c468116737926f816fe9290a9cef313f88283a2946e97a56a56213b468f549b89e38f7c8ff02ea87916aad9d548e49000000000000000000000000000000000000000000000000000000000000001b4ddc03ef9dd99b988dcfb64a83fe0d4ee8e51ca94dffdb044c9bf448513119f19e293cc53d4c98db7012fdee5b6aaf2276be7792b4080979797583b36845d4cb1df88a0e0e746cb0e9832f33bb8591f49d6bf5efd202ffb8bb1944c6cc146c79000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56710000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000161600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1cfadcb5ae96000000000000000000000000000000000000000000000000002e1cfadcb5b04700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008d71836d8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774d6a4d784d475a6a4d7930354e5449784c54566d5a4749744f44646b4e7930354e544d354f5751314d544a6d4d32496966513d3d0000000000000000000000000000000000000000000000000000000000000015000000000000000000000000ecc2614678c049fdde4d82d0348ae7fa12a0a64e00000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x987997ccca3786cb0d7b85b9bd22be7df5e9568213970c20aa4a1497acc33cc5",
      "signature": {
        "s": "0x3f88283a2946e97a56a56213b468f549b89e38f7c8ff02ea87916aad9d548e49",
        "r": "0x0893f5bfc53e08779ef1bb1ba7e24830a0c468116737926f816fe9290a9cef31",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4ddc03ef9dd99b988dcfb64a83fe0d4ee8e51ca94dffdb044c9bf448513119f1",
      "signature": {
        "s": "0x1df88a0e0e746cb0e9832f33bb8591f49d6bf5efd202ffb8bb1944c6cc146c79",
        "r": "0x9e293cc53d4c98db7012fdee5b6aaf2276be7792b4080979797583b36845d4cb",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "432",
    "total": "432"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "432",
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
            "amount": "37968426712"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwMjMxMGZjMy05NTIxLTVmZGItODdkNy05NTM5OWQ1MTJmM2IifQ==",
    "nonce": 5654,
    "balances": {
      "current": "12979712698986134",
      "previous": "12979712698986567"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xecc2614678c049fdde4d82d0348ae7fa12a0a64e",
    "nonce": 21,
    "balances": {
      "current": "432",
      "previous": "0"
    }
  },
  "blockNumber": "10114673",
  "created": "2020-05-22T08:42:52.358Z",
  "updated": "2020-05-22T08:42:52.440Z",
  "id": "5ec7908c005df800101bc99a"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `432`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`