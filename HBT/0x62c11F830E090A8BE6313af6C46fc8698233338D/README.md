# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x62c11F830E090A8BE6313af6C46fc8698233338D`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000d420000000000000000000000000000000000000000000000000000000000000d42000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000d420000000000000000000000000000000000000000000000000000000000000d4259122d6a274663827927c0bde1f2f917aa6e6311f82036d19d567bd032b65da8eaa6dbf3dba7c9ed3763c41365f30349acbee2b7ace840b8213a15c0f2891996071386f4e9845b0f8f4561e6df986e1559d9b072cb5672581aea7bc5978cf429000000000000000000000000000000000000000000000000000000000000001ba7e99bc817c706db2cea37f9b275acabb5fd3ffbf0559755d483b883473456ad52a31618c41fd4e216b02c0512f25331933bc6a5c08edbd8022754bbff81322f056bbd6a8eeb679f3d37bccbaf43101032ade801cf8cbf2457b39111bd1d3b92000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001daf00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b21f3591cc8000000000000000000000000000000000000000000000000002e0b21f3592a0d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000003000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d679142aa000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774f54453159546377596930324f5467304c5456684d6a45745954597a596930794f44526d597a6c6d4d5455324e54596966513d3d000000000000000000000000000000000000000000000000000000000000000500000000000000000000000062c11f830e090a8be6313af6c46fc8698233338d0000000000000000000000000000000000000000000000000000000000000d42000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x59122d6a274663827927c0bde1f2f917aa6e6311f82036d19d567bd032b65da8",
      "signature": {
        "s": "0x071386f4e9845b0f8f4561e6df986e1559d9b072cb5672581aea7bc5978cf429",
        "r": "0xeaa6dbf3dba7c9ed3763c41365f30349acbee2b7ace840b8213a15c0f2891996",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa7e99bc817c706db2cea37f9b275acabb5fd3ffbf0559755d483b883473456ad",
      "signature": {
        "s": "0x056bbd6a8eeb679f3d37bccbaf43101032ade801cf8cbf2457b39111bd1d3b92",
        "r": "0x52a31618c41fd4e216b02c0512f25331933bc6a5c08edbd8022754bbff81322f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3394",
    "total": "3394"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3394",
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
            "amount": "57572147882"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwOTE1YTcwYi02OTg0LTVhMjEtYTYzYi0yODRmYzlmMTU2NTYifQ==",
    "nonce": 7599,
    "balances": {
      "current": "12960089373220040",
      "previous": "12960089373223437"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x62c11f830e090a8be6313af6c46fc8698233338d",
    "nonce": 5,
    "balances": {
      "current": "3394",
      "previous": "0"
    }
  },
  "blockNumber": "10114744",
  "created": "2020-05-22T08:57:55.704Z",
  "updated": "2020-05-22T08:57:55.778Z",
  "id": "5ec79413005df800101bcc26"
}
```
* *stageAmount*: `3394`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000d42000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000d420000000000000000000000000000000000000000000000000000000000000d4259122d6a274663827927c0bde1f2f917aa6e6311f82036d19d567bd032b65da8eaa6dbf3dba7c9ed3763c41365f30349acbee2b7ace840b8213a15c0f2891996071386f4e9845b0f8f4561e6df986e1559d9b072cb5672581aea7bc5978cf429000000000000000000000000000000000000000000000000000000000000001ba7e99bc817c706db2cea37f9b275acabb5fd3ffbf0559755d483b883473456ad52a31618c41fd4e216b02c0512f25331933bc6a5c08edbd8022754bbff81322f056bbd6a8eeb679f3d37bccbaf43101032ade801cf8cbf2457b39111bd1d3b92000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001daf00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b21f3591cc8000000000000000000000000000000000000000000000000002e0b21f3592a0d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000003000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d679142aa000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774f54453159546377596930324f5467304c5456684d6a45745954597a596930794f44526d597a6c6d4d5455324e54596966513d3d000000000000000000000000000000000000000000000000000000000000000500000000000000000000000062c11f830e090a8be6313af6c46fc8698233338d0000000000000000000000000000000000000000000000000000000000000d42000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x59122d6a274663827927c0bde1f2f917aa6e6311f82036d19d567bd032b65da8",
      "signature": {
        "s": "0x071386f4e9845b0f8f4561e6df986e1559d9b072cb5672581aea7bc5978cf429",
        "r": "0xeaa6dbf3dba7c9ed3763c41365f30349acbee2b7ace840b8213a15c0f2891996",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa7e99bc817c706db2cea37f9b275acabb5fd3ffbf0559755d483b883473456ad",
      "signature": {
        "s": "0x056bbd6a8eeb679f3d37bccbaf43101032ade801cf8cbf2457b39111bd1d3b92",
        "r": "0x52a31618c41fd4e216b02c0512f25331933bc6a5c08edbd8022754bbff81322f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3394",
    "total": "3394"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3394",
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
            "amount": "57572147882"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwOTE1YTcwYi02OTg0LTVhMjEtYTYzYi0yODRmYzlmMTU2NTYifQ==",
    "nonce": 7599,
    "balances": {
      "current": "12960089373220040",
      "previous": "12960089373223437"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x62c11f830e090a8be6313af6c46fc8698233338d",
    "nonce": 5,
    "balances": {
      "current": "3394",
      "previous": "0"
    }
  },
  "blockNumber": "10114744",
  "created": "2020-05-22T08:57:55.704Z",
  "updated": "2020-05-22T08:57:55.778Z",
  "id": "5ec79413005df800101bcc26"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000d42000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3394`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`