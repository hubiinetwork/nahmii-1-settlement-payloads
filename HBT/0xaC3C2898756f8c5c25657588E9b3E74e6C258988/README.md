# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xaC3C2898756f8c5c25657588E9b3E74e6C258988`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000002a469f29d00000000000000000000000000000000000000000000000000000002a469f29d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000002a469f29d00000000000000000000000000000000000000000000000000000002a469f29d7cbda704964638c0a0ce2511e622e900169f460090af881f24b464d0894e8b2d9a5c8536f879adaee7eee8354b0ddef21466845fadd7fd3165b34caf4fe04afc300c769a0c37fe7bb6a5ef9bd600aacefa442b1f2319be15a5ed596450fef629000000000000000000000000000000000000000000000000000000000000001ba25598d1affc85756615ba716564a863fde1c11a21a182a0207489886681ecc0996f4ee16ed7c1f6a587929a135c430d58095d51a6d0f0930f12a111a6a1a9bc6c6225ca48b008f9a2620d79b94ca2d9321f6a337bf06fe2feec2b49097fc9d1000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a700000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b8c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e155b7a0000d1000000000000000000000000000000000000000000000000002e155e1f171ce300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000ad2975000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000aca2673c7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694977597a553559574d7a4d4330784d7a59344c545533596d5574595463315969316c4e7a67774d6a597a5a6d55784f54676966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000ac3c2898756f8c5c25657588e9b3e74e6c25898800000000000000000000000000000000000000000000000000000002a469f29d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7cbda704964638c0a0ce2511e622e900169f460090af881f24b464d0894e8b2d",
      "signature": {
        "s": "0x300c769a0c37fe7bb6a5ef9bd600aacefa442b1f2319be15a5ed596450fef629",
        "r": "0x9a5c8536f879adaee7eee8354b0ddef21466845fadd7fd3165b34caf4fe04afc",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa25598d1affc85756615ba716564a863fde1c11a21a182a0207489886681ecc0",
      "signature": {
        "s": "0x6c6225ca48b008f9a2620d79b94ca2d9321f6a337bf06fe2feec2b49097fc9d1",
        "r": "0x996f4ee16ed7c1f6a587929a135c430d58095d51a6d0f0930f12a111a6a1a9bc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "11348341405",
    "total": "11348341405"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11348341405",
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
            "amount": "46341190599"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "11348341"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwYzU5YWMzMC0xMzY4LTU3YmUtYTc1Yi1lNzgwMjYzZmUxOTgifQ==",
    "nonce": 7052,
    "balances": {
      "current": "12971331561717969",
      "previous": "12971342921407715"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xac3c2898756f8c5c25657588e9b3e74e6c258988",
    "nonce": 13,
    "balances": {
      "current": "11348341405",
      "previous": "0"
    }
  },
  "blockNumber": "10114727",
  "created": "2020-05-22T08:53:43.401Z",
  "updated": "2020-05-22T08:53:43.482Z",
  "id": "5ec79317b0c6090011d5b204"
}
```
* *stageAmount*: `11348341405`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000002a469f29d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000002a469f29d00000000000000000000000000000000000000000000000000000002a469f29d7cbda704964638c0a0ce2511e622e900169f460090af881f24b464d0894e8b2d9a5c8536f879adaee7eee8354b0ddef21466845fadd7fd3165b34caf4fe04afc300c769a0c37fe7bb6a5ef9bd600aacefa442b1f2319be15a5ed596450fef629000000000000000000000000000000000000000000000000000000000000001ba25598d1affc85756615ba716564a863fde1c11a21a182a0207489886681ecc0996f4ee16ed7c1f6a587929a135c430d58095d51a6d0f0930f12a111a6a1a9bc6c6225ca48b008f9a2620d79b94ca2d9321f6a337bf06fe2feec2b49097fc9d1000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a700000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b8c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e155b7a0000d1000000000000000000000000000000000000000000000000002e155e1f171ce300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000ad2975000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000aca2673c7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694977597a553559574d7a4d4330784d7a59344c545533596d5574595463315969316c4e7a67774d6a597a5a6d55784f54676966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000ac3c2898756f8c5c25657588e9b3e74e6c25898800000000000000000000000000000000000000000000000000000002a469f29d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7cbda704964638c0a0ce2511e622e900169f460090af881f24b464d0894e8b2d",
      "signature": {
        "s": "0x300c769a0c37fe7bb6a5ef9bd600aacefa442b1f2319be15a5ed596450fef629",
        "r": "0x9a5c8536f879adaee7eee8354b0ddef21466845fadd7fd3165b34caf4fe04afc",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa25598d1affc85756615ba716564a863fde1c11a21a182a0207489886681ecc0",
      "signature": {
        "s": "0x6c6225ca48b008f9a2620d79b94ca2d9321f6a337bf06fe2feec2b49097fc9d1",
        "r": "0x996f4ee16ed7c1f6a587929a135c430d58095d51a6d0f0930f12a111a6a1a9bc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "11348341405",
    "total": "11348341405"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11348341405",
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
            "amount": "46341190599"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "11348341"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwYzU5YWMzMC0xMzY4LTU3YmUtYTc1Yi1lNzgwMjYzZmUxOTgifQ==",
    "nonce": 7052,
    "balances": {
      "current": "12971331561717969",
      "previous": "12971342921407715"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xac3c2898756f8c5c25657588e9b3e74e6c258988",
    "nonce": 13,
    "balances": {
      "current": "11348341405",
      "previous": "0"
    }
  },
  "blockNumber": "10114727",
  "created": "2020-05-22T08:53:43.401Z",
  "updated": "2020-05-22T08:53:43.482Z",
  "id": "5ec79317b0c6090011d5b204"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000002a469f29d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `11348341405`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`