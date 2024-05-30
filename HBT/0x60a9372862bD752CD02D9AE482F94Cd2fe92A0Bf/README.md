# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x60a9372862bD752CD02D9AE482F94Cd2fe92A0Bf`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000004850adba000000000000000000000000000000000000000000000000000000004850adba000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004850adba000000000000000000000000000000000000000000000000000000004850adba9289feb9a818a1f4673dfa620e24ab86624c1ac5d59f7b07dd6d80c66285e654b48606be811bb84c7c55ce482c95e42c09fd686e8adda2433d9ec2c20fdf86ac3976e9370bd25f858497e9ae01e2402d80ce026807b380a0eb8039a4d354d4a4000000000000000000000000000000000000000000000000000000000000001cc09054b998f599622e5f32e22881f916f10b39666f77ed4c61ec207f81e25c3a2180f15387ec73486b433e7ba92f4733df08637700630d5a54cb0d12b9f52f2720f6d7d25bea8db9cd065ca5bc4d715283c99c11a631499b57c18f8286faa952000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c4300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e137c641cc18a000000000000000000000000000000000000000000000000002e137cac7ff28200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000012833e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b44ac6ea5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684e324d774f4449335a6931694d7a46694c5455344e6d5974596a4d355a53307a4e474e6c4e5751355a6a68685954556966513d3d000000000000000000000000000000000000000000000000000000000000000f00000000000000000000000060a9372862bd752cd02d9ae482f94cd2fe92a0bf000000000000000000000000000000000000000000000000000000004850adba000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9289feb9a818a1f4673dfa620e24ab86624c1ac5d59f7b07dd6d80c66285e654",
      "signature": {
        "s": "0x3976e9370bd25f858497e9ae01e2402d80ce026807b380a0eb8039a4d354d4a4",
        "r": "0xb48606be811bb84c7c55ce482c95e42c09fd686e8adda2433d9ec2c20fdf86ac",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc09054b998f599622e5f32e22881f916f10b39666f77ed4c61ec207f81e25c3a",
      "signature": {
        "s": "0x20f6d7d25bea8db9cd065ca5bc4d715283c99c11a631499b57c18f8286faa952",
        "r": "0x2180f15387ec73486b433e7ba92f4733df08637700630d5a54cb0d12b9f52f27",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1213246906",
    "total": "1213246906"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1213246906",
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
            "amount": "48396791461"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1213246"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhN2MwODI3Zi1iMzFiLTU4NmYtYjM5ZS0zNGNlNWQ5ZjhhYTUifQ==",
    "nonce": 7235,
    "balances": {
      "current": "12969273905168778",
      "previous": "12969275119628930"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x60a9372862bd752cd02d9ae482f94cd2fe92a0bf",
    "nonce": 15,
    "balances": {
      "current": "1213246906",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:15.264Z",
  "updated": "2020-05-22T08:55:15.335Z",
  "id": "5ec79373e5756b00111b88a9"
}
```
* *stageAmount*: `1213246906`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000004850adba000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004850adba000000000000000000000000000000000000000000000000000000004850adba9289feb9a818a1f4673dfa620e24ab86624c1ac5d59f7b07dd6d80c66285e654b48606be811bb84c7c55ce482c95e42c09fd686e8adda2433d9ec2c20fdf86ac3976e9370bd25f858497e9ae01e2402d80ce026807b380a0eb8039a4d354d4a4000000000000000000000000000000000000000000000000000000000000001cc09054b998f599622e5f32e22881f916f10b39666f77ed4c61ec207f81e25c3a2180f15387ec73486b433e7ba92f4733df08637700630d5a54cb0d12b9f52f2720f6d7d25bea8db9cd065ca5bc4d715283c99c11a631499b57c18f8286faa952000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c4300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e137c641cc18a000000000000000000000000000000000000000000000000002e137cac7ff28200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000012833e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b44ac6ea5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684e324d774f4449335a6931694d7a46694c5455344e6d5974596a4d355a53307a4e474e6c4e5751355a6a68685954556966513d3d000000000000000000000000000000000000000000000000000000000000000f00000000000000000000000060a9372862bd752cd02d9ae482f94cd2fe92a0bf000000000000000000000000000000000000000000000000000000004850adba000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9289feb9a818a1f4673dfa620e24ab86624c1ac5d59f7b07dd6d80c66285e654",
      "signature": {
        "s": "0x3976e9370bd25f858497e9ae01e2402d80ce026807b380a0eb8039a4d354d4a4",
        "r": "0xb48606be811bb84c7c55ce482c95e42c09fd686e8adda2433d9ec2c20fdf86ac",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc09054b998f599622e5f32e22881f916f10b39666f77ed4c61ec207f81e25c3a",
      "signature": {
        "s": "0x20f6d7d25bea8db9cd065ca5bc4d715283c99c11a631499b57c18f8286faa952",
        "r": "0x2180f15387ec73486b433e7ba92f4733df08637700630d5a54cb0d12b9f52f27",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1213246906",
    "total": "1213246906"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1213246906",
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
            "amount": "48396791461"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1213246"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhN2MwODI3Zi1iMzFiLTU4NmYtYjM5ZS0zNGNlNWQ5ZjhhYTUifQ==",
    "nonce": 7235,
    "balances": {
      "current": "12969273905168778",
      "previous": "12969275119628930"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x60a9372862bd752cd02d9ae482f94cd2fe92a0bf",
    "nonce": 15,
    "balances": {
      "current": "1213246906",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:15.264Z",
  "updated": "2020-05-22T08:55:15.335Z",
  "id": "5ec79373e5756b00111b88a9"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000004850adba000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1213246906`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`