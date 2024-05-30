# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x90D1E63Fd61BeDEE4447Ca9398d0d15cdBd4dd42`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000181b000000000000000000000000000000000000000000000000000000000000181b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000181b000000000000000000000000000000000000000000000000000000000000181b17b51bce3453eed718abc2b08b17f0cf158863719674b0ced958eda234431f5744f70f3292e3a3b048d898769532d2c447e9b6ec4644bd8d569d624fd7275bce551d1e770932efee8db479bf877acf5a1675f2a5411eafd9707a9203fa7c1b0d000000000000000000000000000000000000000000000000000000000000001bb3ed02e57c22701ac9c2c4d3024cd375da86a94c4b5d311c297c027bc16654c1178c96c70fa917f4a5731272b761b8507c37efa5ad50584b55a0f5432e9069c66c24cdc3d184c49ba8abcfd19fed5f7dc7d142e879bb271a157f03af342a4f1d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56bc00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e4000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b05ca5ea690000000000000000000000000000000000000000000000000002e0b05ca5ebeb100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000006000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6ec4ea05000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a6a4532593259774f53307a597a45354c54566959544d744f5449355a5330334d54457a4d444e695a5459355a54636966513d3d000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000090d1e63fd61bedee4447ca9398d0d15cdbd4dd42000000000000000000000000000000000000000000000000000000000000181b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x17b51bce3453eed718abc2b08b17f0cf158863719674b0ced958eda234431f57",
      "signature": {
        "s": "0x551d1e770932efee8db479bf877acf5a1675f2a5411eafd9707a9203fa7c1b0d",
        "r": "0x44f70f3292e3a3b048d898769532d2c447e9b6ec4644bd8d569d624fd7275bce",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb3ed02e57c22701ac9c2c4d3024cd375da86a94c4b5d311c297c027bc16654c1",
      "signature": {
        "s": "0x6c24cdc3d184c49ba8abcfd19fed5f7dc7d142e879bb271a157f03af342a4f1d",
        "r": "0x178c96c70fa917f4a5731272b761b8507c37efa5ad50584b55a0f5432e9069c6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6171",
    "total": "6171"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6171",
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
            "amount": "57692973573"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjZjE2Y2YwOS0zYzE5LTViYTMtOTI5ZS03MTEzMDNiZTY5ZTcifQ==",
    "nonce": 7744,
    "balances": {
      "current": "12959968426632848",
      "previous": "12959968426639025"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x90d1e63fd61bedee4447ca9398d0d15cdbd4dd42",
    "nonce": 10,
    "balances": {
      "current": "6171",
      "previous": "0"
    }
  },
  "blockNumber": "10114748",
  "created": "2020-05-22T08:59:13.462Z",
  "updated": "2020-05-22T08:59:13.531Z",
  "id": "5ec79461005df800101bcc5d"
}
```
* *stageAmount*: `6171`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000181b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000181b000000000000000000000000000000000000000000000000000000000000181b17b51bce3453eed718abc2b08b17f0cf158863719674b0ced958eda234431f5744f70f3292e3a3b048d898769532d2c447e9b6ec4644bd8d569d624fd7275bce551d1e770932efee8db479bf877acf5a1675f2a5411eafd9707a9203fa7c1b0d000000000000000000000000000000000000000000000000000000000000001bb3ed02e57c22701ac9c2c4d3024cd375da86a94c4b5d311c297c027bc16654c1178c96c70fa917f4a5731272b761b8507c37efa5ad50584b55a0f5432e9069c66c24cdc3d184c49ba8abcfd19fed5f7dc7d142e879bb271a157f03af342a4f1d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56bc00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e4000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b05ca5ea690000000000000000000000000000000000000000000000000002e0b05ca5ebeb100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000006000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6ec4ea05000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a6a4532593259774f53307a597a45354c54566959544d744f5449355a5330334d54457a4d444e695a5459355a54636966513d3d000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000090d1e63fd61bedee4447ca9398d0d15cdbd4dd42000000000000000000000000000000000000000000000000000000000000181b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x17b51bce3453eed718abc2b08b17f0cf158863719674b0ced958eda234431f57",
      "signature": {
        "s": "0x551d1e770932efee8db479bf877acf5a1675f2a5411eafd9707a9203fa7c1b0d",
        "r": "0x44f70f3292e3a3b048d898769532d2c447e9b6ec4644bd8d569d624fd7275bce",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb3ed02e57c22701ac9c2c4d3024cd375da86a94c4b5d311c297c027bc16654c1",
      "signature": {
        "s": "0x6c24cdc3d184c49ba8abcfd19fed5f7dc7d142e879bb271a157f03af342a4f1d",
        "r": "0x178c96c70fa917f4a5731272b761b8507c37efa5ad50584b55a0f5432e9069c6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6171",
    "total": "6171"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6171",
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
            "amount": "57692973573"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjZjE2Y2YwOS0zYzE5LTViYTMtOTI5ZS03MTEzMDNiZTY5ZTcifQ==",
    "nonce": 7744,
    "balances": {
      "current": "12959968426632848",
      "previous": "12959968426639025"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x90d1e63fd61bedee4447ca9398d0d15cdbd4dd42",
    "nonce": 10,
    "balances": {
      "current": "6171",
      "previous": "0"
    }
  },
  "blockNumber": "10114748",
  "created": "2020-05-22T08:59:13.462Z",
  "updated": "2020-05-22T08:59:13.531Z",
  "id": "5ec79461005df800101bcc5d"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000181b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6171`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`