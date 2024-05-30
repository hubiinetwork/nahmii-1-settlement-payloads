# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xa19e79a873b509C7851A49cdaF9a0e7B1501ec77`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000077ef00000000000000000000000000000000000000000000000000000000000077ef000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000077ef00000000000000000000000000000000000000000000000000000000000077efaab7bae54deaaf3bfe2eb0dd638b4d2b72cb2e7f8c47391e31077cce5c6e21adcbf9f35780750a388394c216176f53e060161bc54d26ddd8125e3bdd6b70a16003259b42f6404ea2a23d6eb11756ad217497bfb4f78e97ac691f1c7b3926c157000000000000000000000000000000000000000000000000000000000000001ccc48c7d8b8c89224675051db4dede9674f45b6aa5c40cddf929a915bfed496370435e6e17d45108eff08cd94088486fb820ee4a808a95233e54c910a735562b210e581f048bb4292dbe79da4edd33d2c91eb8db90778eae1bf38cd795377ce53000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f0000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007ef00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3912f31000000000000000000000000000000000000000000000000002386f2c391a73e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a551700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d6a41785954557a4e4331684e7a41334c5456694f574974596d59334d7930304d32553259574d31595463344e57496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000a19e79a873b509c7851a49cdaf9a0e7b1501ec7700000000000000000000000000000000000000000000000000000000000077ef000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xaab7bae54deaaf3bfe2eb0dd638b4d2b72cb2e7f8c47391e31077cce5c6e21ad",
      "signature": {
        "s": "0x03259b42f6404ea2a23d6eb11756ad217497bfb4f78e97ac691f1c7b3926c157",
        "r": "0xcbf9f35780750a388394c216176f53e060161bc54d26ddd8125e3bdd6b70a160",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcc48c7d8b8c89224675051db4dede9674f45b6aa5c40cddf929a915bfed49637",
      "signature": {
        "s": "0x10e581f048bb4292dbe79da4edd33d2c91eb8db90778eae1bf38cd795377ce53",
        "r": "0x0435e6e17d45108eff08cd94088486fb820ee4a808a95233e54c910a735562b2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "30703",
    "total": "30703"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "30703",
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
            "amount": "677143"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "30"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzMjAxYTUzNC1hNzA3LTViOWItYmY3My00M2U2YWM1YTc4NWIifQ==",
    "nonce": 2031,
    "balances": {
      "current": "10000001406152497",
      "previous": "10000001406183230"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa19e79a873b509c7851a49cdaf9a0e7b1501ec77",
    "nonce": 20,
    "balances": {
      "current": "30703",
      "previous": "0"
    }
  },
  "blockNumber": "10114544",
  "created": "2020-05-22T08:13:53.035Z",
  "updated": "2020-05-22T08:13:53.100Z",
  "id": "5ec789c1e5756b00111b8203"
}
```
* *stageAmount*: `30703`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000077ef000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000077ef00000000000000000000000000000000000000000000000000000000000077efaab7bae54deaaf3bfe2eb0dd638b4d2b72cb2e7f8c47391e31077cce5c6e21adcbf9f35780750a388394c216176f53e060161bc54d26ddd8125e3bdd6b70a16003259b42f6404ea2a23d6eb11756ad217497bfb4f78e97ac691f1c7b3926c157000000000000000000000000000000000000000000000000000000000000001ccc48c7d8b8c89224675051db4dede9674f45b6aa5c40cddf929a915bfed496370435e6e17d45108eff08cd94088486fb820ee4a808a95233e54c910a735562b210e581f048bb4292dbe79da4edd33d2c91eb8db90778eae1bf38cd795377ce53000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f0000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007ef00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3912f31000000000000000000000000000000000000000000000000002386f2c391a73e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a551700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d6a41785954557a4e4331684e7a41334c5456694f574974596d59334d7930304d32553259574d31595463344e57496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000a19e79a873b509c7851a49cdaf9a0e7b1501ec7700000000000000000000000000000000000000000000000000000000000077ef000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xaab7bae54deaaf3bfe2eb0dd638b4d2b72cb2e7f8c47391e31077cce5c6e21ad",
      "signature": {
        "s": "0x03259b42f6404ea2a23d6eb11756ad217497bfb4f78e97ac691f1c7b3926c157",
        "r": "0xcbf9f35780750a388394c216176f53e060161bc54d26ddd8125e3bdd6b70a160",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcc48c7d8b8c89224675051db4dede9674f45b6aa5c40cddf929a915bfed49637",
      "signature": {
        "s": "0x10e581f048bb4292dbe79da4edd33d2c91eb8db90778eae1bf38cd795377ce53",
        "r": "0x0435e6e17d45108eff08cd94088486fb820ee4a808a95233e54c910a735562b2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "30703",
    "total": "30703"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "30703",
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
            "amount": "677143"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "30"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzMjAxYTUzNC1hNzA3LTViOWItYmY3My00M2U2YWM1YTc4NWIifQ==",
    "nonce": 2031,
    "balances": {
      "current": "10000001406152497",
      "previous": "10000001406183230"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa19e79a873b509c7851a49cdaf9a0e7b1501ec77",
    "nonce": 20,
    "balances": {
      "current": "30703",
      "previous": "0"
    }
  },
  "blockNumber": "10114544",
  "created": "2020-05-22T08:13:53.035Z",
  "updated": "2020-05-22T08:13:53.100Z",
  "id": "5ec789c1e5756b00111b8203"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000077ef0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `30703`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``