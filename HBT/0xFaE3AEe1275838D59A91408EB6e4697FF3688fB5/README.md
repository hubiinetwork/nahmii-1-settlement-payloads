# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xFaE3AEe1275838D59A91408EB6e4697FF3688fB5`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000bd358e7000000000000000000000000000000000000000000000000000000000bd358e7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000bd358e7000000000000000000000000000000000000000000000000000000000bd358e7e070137f8c7452f970dfabacdeab45b629ef252e11a78d1fa4293ced6eddb675b0b4030f01f19af000f4ee74d4834e5c541c746ed1381d223864d2892289b62d0872c1328daf5f0bd56e50f8c36db1b4ddaa3b1786c8f3b469a5c732bedc9ee2000000000000000000000000000000000000000000000000000000000000001cfd9c4dc4a1aeda129f06f0d4fc6df847443b52d54c942f21a8599f58f32a4321cd1d008514496bc9e133f3a5a6e77c3b8efc03b008a022aee0190396ad5bd9fc4b99cdf6b81a62aea9365ab7a173b2423b5edf554f8e9738a00f2a91d95d887e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56770000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000171f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b35ecf647fb000000000000000000000000000000000000000000000000002e1b35f8cca7e200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000030700000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000094aee34ae000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a4446695a6d4d794d4331694e54526d4c54566a4d324574596a45344d5330784e6d52684d446b784d6a4e6d4d32596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000fae3aee1275838d59a91408eb6e4697ff3688fb5000000000000000000000000000000000000000000000000000000000bd358e7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe070137f8c7452f970dfabacdeab45b629ef252e11a78d1fa4293ced6eddb675",
      "signature": {
        "s": "0x0872c1328daf5f0bd56e50f8c36db1b4ddaa3b1786c8f3b469a5c732bedc9ee2",
        "r": "0xb0b4030f01f19af000f4ee74d4834e5c541c746ed1381d223864d2892289b62d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xfd9c4dc4a1aeda129f06f0d4fc6df847443b52d54c942f21a8599f58f32a4321",
      "signature": {
        "s": "0x4b99cdf6b81a62aea9365ab7a173b2423b5edf554f8e9738a00f2a91d95d887e",
        "r": "0xcd1d008514496bc9e133f3a5a6e77c3b8efc03b008a022aee0190396ad5bd9fc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "198400231",
    "total": "198400231"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "198400231",
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
            "amount": "39911830702"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "198400"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxZDFiZmMyMC1iNTRmLTVjM2EtYjE4MS0xNmRhMDkxMjNmM2YifQ==",
    "nonce": 5919,
    "balances": {
      "current": "12977767351470075",
      "previous": "12977767550068706"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfae3aee1275838d59a91408eb6e4697ff3688fb5",
    "nonce": 22,
    "balances": {
      "current": "198400231",
      "previous": "0"
    }
  },
  "blockNumber": "10114679",
  "created": "2020-05-22T08:45:03.623Z",
  "updated": "2020-05-22T08:45:03.693Z",
  "id": "5ec7910fe5756b00111b870b"
}
```
* *stageAmount*: `198400231`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000bd358e7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000bd358e7000000000000000000000000000000000000000000000000000000000bd358e7e070137f8c7452f970dfabacdeab45b629ef252e11a78d1fa4293ced6eddb675b0b4030f01f19af000f4ee74d4834e5c541c746ed1381d223864d2892289b62d0872c1328daf5f0bd56e50f8c36db1b4ddaa3b1786c8f3b469a5c732bedc9ee2000000000000000000000000000000000000000000000000000000000000001cfd9c4dc4a1aeda129f06f0d4fc6df847443b52d54c942f21a8599f58f32a4321cd1d008514496bc9e133f3a5a6e77c3b8efc03b008a022aee0190396ad5bd9fc4b99cdf6b81a62aea9365ab7a173b2423b5edf554f8e9738a00f2a91d95d887e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56770000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000171f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b35ecf647fb000000000000000000000000000000000000000000000000002e1b35f8cca7e200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000030700000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000094aee34ae000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a4446695a6d4d794d4331694e54526d4c54566a4d324574596a45344d5330784e6d52684d446b784d6a4e6d4d32596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000fae3aee1275838d59a91408eb6e4697ff3688fb5000000000000000000000000000000000000000000000000000000000bd358e7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe070137f8c7452f970dfabacdeab45b629ef252e11a78d1fa4293ced6eddb675",
      "signature": {
        "s": "0x0872c1328daf5f0bd56e50f8c36db1b4ddaa3b1786c8f3b469a5c732bedc9ee2",
        "r": "0xb0b4030f01f19af000f4ee74d4834e5c541c746ed1381d223864d2892289b62d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xfd9c4dc4a1aeda129f06f0d4fc6df847443b52d54c942f21a8599f58f32a4321",
      "signature": {
        "s": "0x4b99cdf6b81a62aea9365ab7a173b2423b5edf554f8e9738a00f2a91d95d887e",
        "r": "0xcd1d008514496bc9e133f3a5a6e77c3b8efc03b008a022aee0190396ad5bd9fc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "198400231",
    "total": "198400231"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "198400231",
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
            "amount": "39911830702"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "198400"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxZDFiZmMyMC1iNTRmLTVjM2EtYjE4MS0xNmRhMDkxMjNmM2YifQ==",
    "nonce": 5919,
    "balances": {
      "current": "12977767351470075",
      "previous": "12977767550068706"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfae3aee1275838d59a91408eb6e4697ff3688fb5",
    "nonce": 22,
    "balances": {
      "current": "198400231",
      "previous": "0"
    }
  },
  "blockNumber": "10114679",
  "created": "2020-05-22T08:45:03.623Z",
  "updated": "2020-05-22T08:45:03.693Z",
  "id": "5ec7910fe5756b00111b870b"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000bd358e7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `198400231`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`