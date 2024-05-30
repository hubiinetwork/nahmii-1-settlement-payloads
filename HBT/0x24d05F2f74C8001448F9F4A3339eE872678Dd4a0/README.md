# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x24d05F2f74C8001448F9F4A3339eE872678Dd4a0`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000009dad2cc5000000000000000000000000000000000000000000000000000000009dad2cc5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000009dad2cc5000000000000000000000000000000000000000000000000000000009dad2cc538ffb944a5931b8b5f95836a3d3d5d6991c70a10e7ea9cb973b0ace3e8e2f8322f696eb6e0ad929c0fd2763f61faf345972707f5be5af04f26c8d8a82168f64729f0e795de5754932fd6304685a9c2cd5a7a869d67bb9e3bf856d6dac57f9eb7000000000000000000000000000000000000000000000000000000000000001b9ede97095e350df7301fada37220dc0a724c539421a1e83ad0d106a37340283aaee6609a9cf20bbe8e0770ab9e70a6500414d6c916d04170b40c83c4c8c155b0100be9306c7129253222b39c720071d534e637cfc052909203c0f08b7a2d2d30000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a566a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000159f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d5370751fa1000000000000000000000000000000000000000000000000002e1d540e4aa9e200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000285d7c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008c07105b5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344f5759304d325179596930345a5755324c54566d4d6a4d74596a67784e79316a5a6a51775a4759794e57466a5a6d556966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000024d05f2f74c8001448f9f4a3339ee872678dd4a0000000000000000000000000000000000000000000000000000000009dad2cc5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x38ffb944a5931b8b5f95836a3d3d5d6991c70a10e7ea9cb973b0ace3e8e2f832",
      "signature": {
        "s": "0x29f0e795de5754932fd6304685a9c2cd5a7a869d67bb9e3bf856d6dac57f9eb7",
        "r": "0x2f696eb6e0ad929c0fd2763f61faf345972707f5be5af04f26c8d8a82168f647",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9ede97095e350df7301fada37220dc0a724c539421a1e83ad0d106a37340283a",
      "signature": {
        "s": "0x100be9306c7129253222b39c720071d534e637cfc052909203c0f08b7a2d2d30",
        "r": "0xaee6609a9cf20bbe8e0770ab9e70a6500414d6c916d04170b40c83c4c8c155b0",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2645372101",
    "total": "2645372101"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2645372101",
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
            "amount": "37588370869"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2645372"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4OWY0M2QyYi04ZWU2LTVmMjMtYjgxNy1jZjQwZGYyNWFjZmUifQ==",
    "nonce": 5535,
    "balances": {
      "current": "12980093134905249",
      "previous": "12980095782922722"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x24d05f2f74c8001448f9f4a3339ee872678dd4a0",
    "nonce": 22,
    "balances": {
      "current": "2645372101",
      "previous": "0"
    }
  },
  "blockNumber": "10114666",
  "created": "2020-05-22T08:41:53.875Z",
  "updated": "2020-05-22T08:41:53.938Z",
  "id": "5ec79051005df800101bc973"
}
```
* *stageAmount*: `2645372101`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000009dad2cc5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000009dad2cc5000000000000000000000000000000000000000000000000000000009dad2cc538ffb944a5931b8b5f95836a3d3d5d6991c70a10e7ea9cb973b0ace3e8e2f8322f696eb6e0ad929c0fd2763f61faf345972707f5be5af04f26c8d8a82168f64729f0e795de5754932fd6304685a9c2cd5a7a869d67bb9e3bf856d6dac57f9eb7000000000000000000000000000000000000000000000000000000000000001b9ede97095e350df7301fada37220dc0a724c539421a1e83ad0d106a37340283aaee6609a9cf20bbe8e0770ab9e70a6500414d6c916d04170b40c83c4c8c155b0100be9306c7129253222b39c720071d534e637cfc052909203c0f08b7a2d2d30000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a566a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000159f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d5370751fa1000000000000000000000000000000000000000000000000002e1d540e4aa9e200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000285d7c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008c07105b5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344f5759304d325179596930345a5755324c54566d4d6a4d74596a67784e79316a5a6a51775a4759794e57466a5a6d556966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000024d05f2f74c8001448f9f4a3339ee872678dd4a0000000000000000000000000000000000000000000000000000000009dad2cc5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x38ffb944a5931b8b5f95836a3d3d5d6991c70a10e7ea9cb973b0ace3e8e2f832",
      "signature": {
        "s": "0x29f0e795de5754932fd6304685a9c2cd5a7a869d67bb9e3bf856d6dac57f9eb7",
        "r": "0x2f696eb6e0ad929c0fd2763f61faf345972707f5be5af04f26c8d8a82168f647",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9ede97095e350df7301fada37220dc0a724c539421a1e83ad0d106a37340283a",
      "signature": {
        "s": "0x100be9306c7129253222b39c720071d534e637cfc052909203c0f08b7a2d2d30",
        "r": "0xaee6609a9cf20bbe8e0770ab9e70a6500414d6c916d04170b40c83c4c8c155b0",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2645372101",
    "total": "2645372101"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2645372101",
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
            "amount": "37588370869"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2645372"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4OWY0M2QyYi04ZWU2LTVmMjMtYjgxNy1jZjQwZGYyNWFjZmUifQ==",
    "nonce": 5535,
    "balances": {
      "current": "12980093134905249",
      "previous": "12980095782922722"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x24d05f2f74c8001448f9f4a3339ee872678dd4a0",
    "nonce": 22,
    "balances": {
      "current": "2645372101",
      "previous": "0"
    }
  },
  "blockNumber": "10114666",
  "created": "2020-05-22T08:41:53.875Z",
  "updated": "2020-05-22T08:41:53.938Z",
  "id": "5ec79051005df800101bc973"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000009dad2cc5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2645372101`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`