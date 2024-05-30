# Settlement of ETH
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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000863380000000000000000000000000000000000000000000000000000000000086338000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000863380000000000000000000000000000000000000000000000000000000000086338a1f34d31185af110e25792a9d6084793a0fb743895fe7862be427896787888221ab456463886591145eb99a3183bfe0b5e5e206bc060ad1faea93fc029858473618b8ea08c03ba0913dfe3e0da1c7ae37deedbd86bcf3e1b7db64aa54f6b3987000000000000000000000000000000000000000000000000000000000000001c613948f91436c8d47faae5e2b960a6b5f294df1e271beac1556bcee779d2bda741b72fc84f3d8668be1932f31aa69e790b3ba6a8b80f40cc32cd93e0d148a8f355e0af210781f3904c5b83dd423135bb20e37c317b5512b1d8e1818f4b9eb33a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f0000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007f600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c384e716000000000000000000000000000000000000000000000000002386f2c38d4c7300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000002250000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a583700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d32526b4e5755334d79316d596d597a4c54557a59575574595441314f5330795a4456685a44466b4e5441335a57516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000e1cdb3fa3edf41d6dc890f5403f9de695209428e0000000000000000000000000000000000000000000000000000000000086338000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa1f34d31185af110e25792a9d6084793a0fb743895fe7862be42789678788822",
      "signature": {
        "s": "0x618b8ea08c03ba0913dfe3e0da1c7ae37deedbd86bcf3e1b7db64aa54f6b3987",
        "r": "0x1ab456463886591145eb99a3183bfe0b5e5e206bc060ad1faea93fc029858473",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x613948f91436c8d47faae5e2b960a6b5f294df1e271beac1556bcee779d2bda7",
      "signature": {
        "s": "0x55e0af210781f3904c5b83dd423135bb20e37c317b5512b1d8e1818f4b9eb33a",
        "r": "0x41b72fc84f3d8668be1932f31aa69e790b3ba6a8b80f40cc32cd93e0d148a8f3",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "549688",
    "total": "549688"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "549688",
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
            "amount": "677943"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "549"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxM2RkNWU3My1mYmYzLTUzYWUtYTA1OS0yZDVhZDFkNTA3ZWQifQ==",
    "nonce": 2038,
    "balances": {
      "current": "10000001405347606",
      "previous": "10000001405897843"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe1cdb3fa3edf41d6dc890f5403f9de695209428e",
    "nonce": 20,
    "balances": {
      "current": "549688",
      "previous": "0"
    }
  },
  "blockNumber": "10114544",
  "created": "2020-05-22T08:13:59.450Z",
  "updated": "2020-05-22T08:13:59.528Z",
  "id": "5ec789c7b0c6090011d5ab75"
}
```
* *stageAmount*: `549688`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000086338000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000863380000000000000000000000000000000000000000000000000000000000086338a1f34d31185af110e25792a9d6084793a0fb743895fe7862be427896787888221ab456463886591145eb99a3183bfe0b5e5e206bc060ad1faea93fc029858473618b8ea08c03ba0913dfe3e0da1c7ae37deedbd86bcf3e1b7db64aa54f6b3987000000000000000000000000000000000000000000000000000000000000001c613948f91436c8d47faae5e2b960a6b5f294df1e271beac1556bcee779d2bda741b72fc84f3d8668be1932f31aa69e790b3ba6a8b80f40cc32cd93e0d148a8f355e0af210781f3904c5b83dd423135bb20e37c317b5512b1d8e1818f4b9eb33a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f0000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007f600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c384e716000000000000000000000000000000000000000000000000002386f2c38d4c7300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000002250000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a583700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d32526b4e5755334d79316d596d597a4c54557a59575574595441314f5330795a4456685a44466b4e5441335a57516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000e1cdb3fa3edf41d6dc890f5403f9de695209428e0000000000000000000000000000000000000000000000000000000000086338000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa1f34d31185af110e25792a9d6084793a0fb743895fe7862be42789678788822",
      "signature": {
        "s": "0x618b8ea08c03ba0913dfe3e0da1c7ae37deedbd86bcf3e1b7db64aa54f6b3987",
        "r": "0x1ab456463886591145eb99a3183bfe0b5e5e206bc060ad1faea93fc029858473",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x613948f91436c8d47faae5e2b960a6b5f294df1e271beac1556bcee779d2bda7",
      "signature": {
        "s": "0x55e0af210781f3904c5b83dd423135bb20e37c317b5512b1d8e1818f4b9eb33a",
        "r": "0x41b72fc84f3d8668be1932f31aa69e790b3ba6a8b80f40cc32cd93e0d148a8f3",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "549688",
    "total": "549688"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "549688",
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
            "amount": "677943"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "549"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxM2RkNWU3My1mYmYzLTUzYWUtYTA1OS0yZDVhZDFkNTA3ZWQifQ==",
    "nonce": 2038,
    "balances": {
      "current": "10000001405347606",
      "previous": "10000001405897843"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe1cdb3fa3edf41d6dc890f5403f9de695209428e",
    "nonce": 20,
    "balances": {
      "current": "549688",
      "previous": "0"
    }
  },
  "blockNumber": "10114544",
  "created": "2020-05-22T08:13:59.450Z",
  "updated": "2020-05-22T08:13:59.528Z",
  "id": "5ec789c7b0c6090011d5ab75"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000863380000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `549688`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``