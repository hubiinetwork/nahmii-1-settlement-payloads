# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xfBA7EDDb0B113d2638773A73B56eEF98C1a3c82d`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000900000000000000000000000000000000000000000000000000000000000000090000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000900000000000000000000000000000000000000000000000000000000000000090e198c7af0f8bc3f220a95634ef72014ad48bfa196c0e1a542f1538adac0c55d6da463a16934805c466082d374cd79165c4339c1d60ef55fa7586821b74e938802f9ed38f86c8101b3bcbc9d2ec4328e685faf38014e2b3199ebb208961186b09000000000000000000000000000000000000000000000000000000000000001cf5519a3b01f6fb7c927cc6c004a0f5a6647f5114247ab5d6d1ce51b9454d0e8eeb43690954994dea362f1ecd5bb8b9cc54be492859af5ea353567162a3fde67f7f17df3ac6f08b827057b30115ae73179aec5c8fb166ea9dc6ffdf2819da5d7a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56700000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000160e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1cfdd42353e2000000000000000000000000000000000000000000000000002e1cfdd423547300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008d655fead000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e3251774e4464694e4330304e44646d4c54566b59546374596d5530595330315a5446684d5755774e7a45324e574d6966513d3d0000000000000000000000000000000000000000000000000000000000000015000000000000000000000000fba7eddb0b113d2638773a73b56eef98c1a3c82d0000000000000000000000000000000000000000000000000000000000000090000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe198c7af0f8bc3f220a95634ef72014ad48bfa196c0e1a542f1538adac0c55d6",
      "signature": {
        "s": "0x2f9ed38f86c8101b3bcbc9d2ec4328e685faf38014e2b3199ebb208961186b09",
        "r": "0xda463a16934805c466082d374cd79165c4339c1d60ef55fa7586821b74e93880",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf5519a3b01f6fb7c927cc6c004a0f5a6647f5114247ab5d6d1ce51b9454d0e8e",
      "signature": {
        "s": "0x7f17df3ac6f08b827057b30115ae73179aec5c8fb166ea9dc6ffdf2819da5d7a",
        "r": "0xeb43690954994dea362f1ecd5bb8b9cc54be492859af5ea353567162a3fde67f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "144",
    "total": "144"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "144",
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
            "amount": "37955698349"
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
    "data": "eyJyZWYiOiJlN2QwNDdiNC00NDdmLTVkYTctYmU0YS01ZTFhMWUwNzE2NWMifQ==",
    "nonce": 5646,
    "balances": {
      "current": "12979725440078818",
      "previous": "12979725440078963"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfba7eddb0b113d2638773a73b56eef98c1a3c82d",
    "nonce": 21,
    "balances": {
      "current": "144",
      "previous": "0"
    }
  },
  "blockNumber": "10114672",
  "created": "2020-05-22T08:42:49.805Z",
  "updated": "2020-05-22T08:42:49.878Z",
  "id": "5ec79089e5756b00111b86a6"
}
```
* *stageAmount*: `144`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000090000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000900000000000000000000000000000000000000000000000000000000000000090e198c7af0f8bc3f220a95634ef72014ad48bfa196c0e1a542f1538adac0c55d6da463a16934805c466082d374cd79165c4339c1d60ef55fa7586821b74e938802f9ed38f86c8101b3bcbc9d2ec4328e685faf38014e2b3199ebb208961186b09000000000000000000000000000000000000000000000000000000000000001cf5519a3b01f6fb7c927cc6c004a0f5a6647f5114247ab5d6d1ce51b9454d0e8eeb43690954994dea362f1ecd5bb8b9cc54be492859af5ea353567162a3fde67f7f17df3ac6f08b827057b30115ae73179aec5c8fb166ea9dc6ffdf2819da5d7a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56700000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000160e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1cfdd42353e2000000000000000000000000000000000000000000000000002e1cfdd423547300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008d655fead000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e3251774e4464694e4330304e44646d4c54566b59546374596d5530595330315a5446684d5755774e7a45324e574d6966513d3d0000000000000000000000000000000000000000000000000000000000000015000000000000000000000000fba7eddb0b113d2638773a73b56eef98c1a3c82d0000000000000000000000000000000000000000000000000000000000000090000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe198c7af0f8bc3f220a95634ef72014ad48bfa196c0e1a542f1538adac0c55d6",
      "signature": {
        "s": "0x2f9ed38f86c8101b3bcbc9d2ec4328e685faf38014e2b3199ebb208961186b09",
        "r": "0xda463a16934805c466082d374cd79165c4339c1d60ef55fa7586821b74e93880",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf5519a3b01f6fb7c927cc6c004a0f5a6647f5114247ab5d6d1ce51b9454d0e8e",
      "signature": {
        "s": "0x7f17df3ac6f08b827057b30115ae73179aec5c8fb166ea9dc6ffdf2819da5d7a",
        "r": "0xeb43690954994dea362f1ecd5bb8b9cc54be492859af5ea353567162a3fde67f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "144",
    "total": "144"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "144",
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
            "amount": "37955698349"
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
    "data": "eyJyZWYiOiJlN2QwNDdiNC00NDdmLTVkYTctYmU0YS01ZTFhMWUwNzE2NWMifQ==",
    "nonce": 5646,
    "balances": {
      "current": "12979725440078818",
      "previous": "12979725440078963"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfba7eddb0b113d2638773a73b56eef98c1a3c82d",
    "nonce": 21,
    "balances": {
      "current": "144",
      "previous": "0"
    }
  },
  "blockNumber": "10114672",
  "created": "2020-05-22T08:42:49.805Z",
  "updated": "2020-05-22T08:42:49.878Z",
  "id": "5ec79089e5756b00111b86a6"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000090000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `144`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`