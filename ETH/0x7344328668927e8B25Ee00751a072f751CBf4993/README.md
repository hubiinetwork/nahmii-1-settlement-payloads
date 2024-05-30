# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7344328668927e8B25Ee00751a072f751CBf4993`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000002aa68500000000000000000000000000000000000000000000000000000000002aa685000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000002aa68500000000000000000000000000000000000000000000000000000000002aa6858a3ad8462827b005059f63e5b746e56d9d96b2f98d3f3868cc9e25e8d28330017862a0140e9b78532c09b680482e4c24a486a2a7d745fc6f123d74359964d322353b131cb1419fd4cd41691d655cac4ca263c1284856844b85ecd045fc53be6f000000000000000000000000000000000000000000000000000000000000001b193cc547fd311a66336e1ee38b6bf8db01e0b1b015949415600771766a7566c5f998e7a2962abcc3620733bbc77e57a2db233d8d1fcf4f4281ffc15b8a2c068e4382a22b7c01bb3490472a0f489cab9de418d4e28a9ef43a6d67360bfe420c8d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55b90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000006800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d61746e4000000000000000000000000000000000000000000000000002386f2d641f85400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000aeb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000059a9c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934596d517759574e695a533169597a41784c54566859324574595445324d6930355a57457a4d6a49775a4455354e7a496966513d3d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000007344328668927e8b25ee00751a072f751cbf499300000000000000000000000000000000000000000000000000000000002aa685000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8a3ad8462827b005059f63e5b746e56d9d96b2f98d3f3868cc9e25e8d2833001",
      "signature": {
        "s": "0x353b131cb1419fd4cd41691d655cac4ca263c1284856844b85ecd045fc53be6f",
        "r": "0x7862a0140e9b78532c09b680482e4c24a486a2a7d745fc6f123d74359964d322",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x193cc547fd311a66336e1ee38b6bf8db01e0b1b015949415600771766a7566c5",
      "signature": {
        "s": "0x4382a22b7c01bb3490472a0f489cab9de418d4e28a9ef43a6d67360bfe420c8d",
        "r": "0xf998e7a2962abcc3620733bbc77e57a2db233d8d1fcf4f4281ffc15b8a2c068e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2795141",
    "total": "2795141"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2795141",
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
            "amount": "367260"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2795"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4YmQwYWNiZS1iYzAxLTVhY2EtYTE2Mi05ZWEzMjIwZDU5NzIifQ==",
    "nonce": 104,
    "balances": {
      "current": "10000001716930276",
      "previous": "10000001719728212"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7344328668927e8b25ee00751a072f751cbf4993",
    "nonce": 28,
    "balances": {
      "current": "2795141",
      "previous": "0"
    }
  },
  "blockNumber": "10114489",
  "created": "2020-05-22T07:59:37.974Z",
  "updated": "2020-05-22T07:59:38.049Z",
  "id": "5ec78669b0c6090011d5a8f7"
}
```
* *stageAmount*: `2795141`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000002aa685000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000002aa68500000000000000000000000000000000000000000000000000000000002aa6858a3ad8462827b005059f63e5b746e56d9d96b2f98d3f3868cc9e25e8d28330017862a0140e9b78532c09b680482e4c24a486a2a7d745fc6f123d74359964d322353b131cb1419fd4cd41691d655cac4ca263c1284856844b85ecd045fc53be6f000000000000000000000000000000000000000000000000000000000000001b193cc547fd311a66336e1ee38b6bf8db01e0b1b015949415600771766a7566c5f998e7a2962abcc3620733bbc77e57a2db233d8d1fcf4f4281ffc15b8a2c068e4382a22b7c01bb3490472a0f489cab9de418d4e28a9ef43a6d67360bfe420c8d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55b90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000006800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d61746e4000000000000000000000000000000000000000000000000002386f2d641f85400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000aeb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000059a9c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934596d517759574e695a533169597a41784c54566859324574595445324d6930355a57457a4d6a49775a4455354e7a496966513d3d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000007344328668927e8b25ee00751a072f751cbf499300000000000000000000000000000000000000000000000000000000002aa685000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8a3ad8462827b005059f63e5b746e56d9d96b2f98d3f3868cc9e25e8d2833001",
      "signature": {
        "s": "0x353b131cb1419fd4cd41691d655cac4ca263c1284856844b85ecd045fc53be6f",
        "r": "0x7862a0140e9b78532c09b680482e4c24a486a2a7d745fc6f123d74359964d322",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x193cc547fd311a66336e1ee38b6bf8db01e0b1b015949415600771766a7566c5",
      "signature": {
        "s": "0x4382a22b7c01bb3490472a0f489cab9de418d4e28a9ef43a6d67360bfe420c8d",
        "r": "0xf998e7a2962abcc3620733bbc77e57a2db233d8d1fcf4f4281ffc15b8a2c068e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2795141",
    "total": "2795141"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2795141",
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
            "amount": "367260"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2795"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4YmQwYWNiZS1iYzAxLTVhY2EtYTE2Mi05ZWEzMjIwZDU5NzIifQ==",
    "nonce": 104,
    "balances": {
      "current": "10000001716930276",
      "previous": "10000001719728212"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7344328668927e8b25ee00751a072f751cbf4993",
    "nonce": 28,
    "balances": {
      "current": "2795141",
      "previous": "0"
    }
  },
  "blockNumber": "10114489",
  "created": "2020-05-22T07:59:37.974Z",
  "updated": "2020-05-22T07:59:38.049Z",
  "id": "5ec78669b0c6090011d5a8f7"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000002aa6850000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2795141`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``