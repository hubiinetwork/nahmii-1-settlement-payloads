# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe1CDb3FA3edf41d6dc890f5403F9DE695209428E`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000093cf62b0e000000000000000000000000000000000000000000000000000000093cf62b0e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000093cf62b0e000000000000000000000000000000000000000000000000000000093cf62b0e27d86bfd849619e96915b4e1711de6c245829def62215bc267e8d9cd6bc92892fd2ee37a47455e01d99814955672aabcc656938810963036860b226f7e85a1b0230e8b250b90c95704e3e79ff58d4b38ac2d9d172172bcaaaa227edd32fa689a000000000000000000000000000000000000000000000000000000000000001bd03a5bb6665aa23af9e011d2535ecae413f851df7af676bf1bc7f9402fe07aceb4156f9d87bed067fc83ab2af85ec152d6e86f3bbb8df53455b18e117dba4571429e6c07caf67328b67945f42f6c8fd0f6387d0d06ce48cfd4551ebe6d1ea443000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ce200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e12f43a3f5007000000000000000000000000000000000000000000000000002e12fd7992e93400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000025d6e1f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b677f2138000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a44566d4e54646a4d69316d4f57457a4c5456685a544d744f5445354d5330334f574a6b4f544177595449344f44416966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e1cdb3fa3edf41d6dc890f5403f9de695209428e000000000000000000000000000000000000000000000000000000093cf62b0e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x27d86bfd849619e96915b4e1711de6c245829def62215bc267e8d9cd6bc92892",
      "signature": {
        "s": "0x230e8b250b90c95704e3e79ff58d4b38ac2d9d172172bcaaaa227edd32fa689a",
        "r": "0xfd2ee37a47455e01d99814955672aabcc656938810963036860b226f7e85a1b0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd03a5bb6665aa23af9e011d2535ecae413f851df7af676bf1bc7f9402fe07ace",
      "signature": {
        "s": "0x429e6c07caf67328b67945f42f6c8fd0f6387d0d06ce48cfd4551ebe6d1ea443",
        "r": "0xb4156f9d87bed067fc83ab2af85ec152d6e86f3bbb8df53455b18e117dba4571",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "39677471502",
    "total": "39677471502"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "39677471502",
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
            "amount": "48981025080"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "39677471"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1ZDVmNTdjMi1mOWEzLTVhZTMtOTE5MS03OWJkOTAwYTI4ODAifQ==",
    "nonce": 7394,
    "balances": {
      "current": "12968689087238151",
      "previous": "12968728804387124"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe1cdb3fa3edf41d6dc890f5403f9de695209428e",
    "nonce": 22,
    "balances": {
      "current": "39677471502",
      "previous": "0"
    }
  },
  "blockNumber": "10114738",
  "created": "2020-05-22T08:56:25.611Z",
  "updated": "2020-05-22T08:56:26.671Z",
  "id": "5ec793b9e5756b00111b88d2"
}
```
* *stageAmount*: `39677471502`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000093cf62b0e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000093cf62b0e000000000000000000000000000000000000000000000000000000093cf62b0e27d86bfd849619e96915b4e1711de6c245829def62215bc267e8d9cd6bc92892fd2ee37a47455e01d99814955672aabcc656938810963036860b226f7e85a1b0230e8b250b90c95704e3e79ff58d4b38ac2d9d172172bcaaaa227edd32fa689a000000000000000000000000000000000000000000000000000000000000001bd03a5bb6665aa23af9e011d2535ecae413f851df7af676bf1bc7f9402fe07aceb4156f9d87bed067fc83ab2af85ec152d6e86f3bbb8df53455b18e117dba4571429e6c07caf67328b67945f42f6c8fd0f6387d0d06ce48cfd4551ebe6d1ea443000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ce200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e12f43a3f5007000000000000000000000000000000000000000000000000002e12fd7992e93400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000025d6e1f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b677f2138000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a44566d4e54646a4d69316d4f57457a4c5456685a544d744f5445354d5330334f574a6b4f544177595449344f44416966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e1cdb3fa3edf41d6dc890f5403f9de695209428e000000000000000000000000000000000000000000000000000000093cf62b0e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x27d86bfd849619e96915b4e1711de6c245829def62215bc267e8d9cd6bc92892",
      "signature": {
        "s": "0x230e8b250b90c95704e3e79ff58d4b38ac2d9d172172bcaaaa227edd32fa689a",
        "r": "0xfd2ee37a47455e01d99814955672aabcc656938810963036860b226f7e85a1b0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd03a5bb6665aa23af9e011d2535ecae413f851df7af676bf1bc7f9402fe07ace",
      "signature": {
        "s": "0x429e6c07caf67328b67945f42f6c8fd0f6387d0d06ce48cfd4551ebe6d1ea443",
        "r": "0xb4156f9d87bed067fc83ab2af85ec152d6e86f3bbb8df53455b18e117dba4571",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "39677471502",
    "total": "39677471502"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "39677471502",
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
            "amount": "48981025080"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "39677471"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1ZDVmNTdjMi1mOWEzLTVhZTMtOTE5MS03OWJkOTAwYTI4ODAifQ==",
    "nonce": 7394,
    "balances": {
      "current": "12968689087238151",
      "previous": "12968728804387124"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe1cdb3fa3edf41d6dc890f5403f9de695209428e",
    "nonce": 22,
    "balances": {
      "current": "39677471502",
      "previous": "0"
    }
  },
  "blockNumber": "10114738",
  "created": "2020-05-22T08:56:25.611Z",
  "updated": "2020-05-22T08:56:26.671Z",
  "id": "5ec793b9e5756b00111b88d2"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000093cf62b0e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `39677471502`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`