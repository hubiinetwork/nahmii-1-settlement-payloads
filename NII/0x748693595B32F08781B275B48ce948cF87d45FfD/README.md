# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x748693595B32F08781B275B48ce948cF87d45FfD`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000013e152c1a885476dbb00000000000000000000000000000000000000000000000078a97f795c3d2a000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000078a97f795c3d2a0000000000000000000000000000000000000000000000000d39e5589131bc321989b9b4a5b77525059c39a786a6b54b0078c0be79f5d8678e5e9d825b07120beeb2c871f9dc07b93b8850cd419a728f11294a17c1eb2241c0f834a3e3e4a2af2d0606ab2b6a23d3721de1a241679e84a2a600fabf0ca633cd1bfa1437396caf24000000000000000000000000000000000000000000000000000000000000001cc3d768fddd55a5293b12ce6c47481fd7826327dbc8f6a8e31b21054c276b423c1777be24ee0ddd07ff0d82af3d1efb1b5e4bc70de15e5ba1ccd7e15427e0da49478c3f475ec8b191206e4cd57257b6e18e25c628b978850c1e53efba9232b7f9000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b212000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000049820f08d368979ba5c000000000000000000000000000000000000000000000498287d136981702db4f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001ee3b6232a0b8f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d99561cebc7375abc70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d7a6b7a4f474d324e53316d4e5467774c54566b4e7a55744f5756684d53316b4e54686b4d6a63344e6d5a6c596d456966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000748693595b32f08781b275b48ce948cf87d45ffd000000000000000000000000000000000000000000000013e152c1a885476dbb00000000000000000000000000000000000000000000001368a9422f290a43bb00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x89b9b4a5b77525059c39a786a6b54b0078c0be79f5d8678e5e9d825b07120bee",
      "signature": {
        "s": "0x0606ab2b6a23d3721de1a241679e84a2a600fabf0ca633cd1bfa1437396caf24",
        "r": "0xb2c871f9dc07b93b8850cd419a728f11294a17c1eb2241c0f834a3e3e4a2af2d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc3d768fddd55a5293b12ce6c47481fd7826327dbc8f6a8e31b21054c276b423c",
      "signature": {
        "s": "0x478c3f475ec8b191206e4cd57257b6e18e25c628b978850c1e53efba9232b7f9",
        "r": "0x1777be24ee0ddd07ff0d82af3d1efb1b5e4bc70de15e5ba1ccd7e15427e0da49",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8694620714830735872",
    "total": "243979510968680722969"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8694620714830735872",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27625539990236377230279"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8694620714830735"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxMzkzOGM2NS1mNTgwLTVkNzUtOWVhMS1kNThkMjc4NmZlYmEifQ==",
    "nonce": 111122,
    "balances": {
      "current": "347131913327222898533824",
      "previous": "347140616642558444100431"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x748693595b32f08781b275b48ce948cf87d45ffd",
    "nonce": 46,
    "balances": {
      "current": "366724389936640257467",
      "previous": "358029769221809521595"
    }
  },
  "blockNumber": "14709974",
  "created": "2022-05-04T08:56:40.150Z",
  "updated": "2022-05-04T08:56:40.229Z",
  "id": "62723fc8bbd75600116d064f"
}
```
* *stageAmount*: `366724389936640257467`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000078a97f795c3d2a000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000078a97f795c3d2a0000000000000000000000000000000000000000000000000d39e5589131bc321989b9b4a5b77525059c39a786a6b54b0078c0be79f5d8678e5e9d825b07120beeb2c871f9dc07b93b8850cd419a728f11294a17c1eb2241c0f834a3e3e4a2af2d0606ab2b6a23d3721de1a241679e84a2a600fabf0ca633cd1bfa1437396caf24000000000000000000000000000000000000000000000000000000000000001cc3d768fddd55a5293b12ce6c47481fd7826327dbc8f6a8e31b21054c276b423c1777be24ee0ddd07ff0d82af3d1efb1b5e4bc70de15e5ba1ccd7e15427e0da49478c3f475ec8b191206e4cd57257b6e18e25c628b978850c1e53efba9232b7f9000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b212000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000049820f08d368979ba5c000000000000000000000000000000000000000000000498287d136981702db4f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001ee3b6232a0b8f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d99561cebc7375abc70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d7a6b7a4f474d324e53316d4e5467774c54566b4e7a55744f5756684d53316b4e54686b4d6a63344e6d5a6c596d456966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000748693595b32f08781b275b48ce948cf87d45ffd000000000000000000000000000000000000000000000013e152c1a885476dbb00000000000000000000000000000000000000000000001368a9422f290a43bb00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x89b9b4a5b77525059c39a786a6b54b0078c0be79f5d8678e5e9d825b07120bee",
      "signature": {
        "s": "0x0606ab2b6a23d3721de1a241679e84a2a600fabf0ca633cd1bfa1437396caf24",
        "r": "0xb2c871f9dc07b93b8850cd419a728f11294a17c1eb2241c0f834a3e3e4a2af2d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc3d768fddd55a5293b12ce6c47481fd7826327dbc8f6a8e31b21054c276b423c",
      "signature": {
        "s": "0x478c3f475ec8b191206e4cd57257b6e18e25c628b978850c1e53efba9232b7f9",
        "r": "0x1777be24ee0ddd07ff0d82af3d1efb1b5e4bc70de15e5ba1ccd7e15427e0da49",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8694620714830735872",
    "total": "243979510968680722969"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8694620714830735872",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27625539990236377230279"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8694620714830735"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxMzkzOGM2NS1mNTgwLTVkNzUtOWVhMS1kNThkMjc4NmZlYmEifQ==",
    "nonce": 111122,
    "balances": {
      "current": "347131913327222898533824",
      "previous": "347140616642558444100431"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x748693595b32f08781b275b48ce948cf87d45ffd",
    "nonce": 46,
    "balances": {
      "current": "366724389936640257467",
      "previous": "358029769221809521595"
    }
  },
  "blockNumber": "14709974",
  "created": "2022-05-04T08:56:40.150Z",
  "updated": "2022-05-04T08:56:40.229Z",
  "id": "62723fc8bbd75600116d064f"
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
0x0f200f9b000000000000000000000000000000000000000000000013e152c1a885476dbb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `366724389936640257467`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`