# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4BFDe1b7906DCdF8fb7E779Cb199Fd65Bf8004Ff`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000052578b0f0000000000000000000000000000000000000000000000000000000052578b0f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000052578b0f0000000000000000000000000000000000000000000000000000000052578b0f0d73c2e0b0e636fcc7643756e1e3b0571a3e6f9658efa53fd972469163e62b104e39c1e83f3be88370db6455c3fdce296fb675b087c104460db59dd546a41d563565609048d526670d6ec9ce2b8712baf4f43393d029dce62016840d1c623769000000000000000000000000000000000000000000000000000000000000001b73571878e650234424d488eaf740ae9910a3e3a1f7f65c435290ec0e404e2fd6a3a6e7f1f32bfb45fea87d4d54beeaa6b7f59fb362c62bfd0b406d308f779a1249f23d0ca17f17eb2f35ce24e77431bcd27f54b5ad961f17b237dd99cd79535b000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ba00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001dfe00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b1215b359a2000000000000000000000000000000000000000000000000002e0b12681ff90d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000015145c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6ba000b7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949305a6a49305a47517a4f43316d4d6d55334c5455324e3249745957557a4d533077597a59774e6a41774e6d4e6b5a47456966513d3d000000000000000000000000000000000000000000000000000000000000000f0000000000000000000000004bfde1b7906dcdf8fb7e779cb199fd65bf8004ff0000000000000000000000000000000000000000000000000000000052578b0f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0d73c2e0b0e636fcc7643756e1e3b0571a3e6f9658efa53fd972469163e62b10",
      "signature": {
        "s": "0x3565609048d526670d6ec9ce2b8712baf4f43393d029dce62016840d1c623769",
        "r": "0x4e39c1e83f3be88370db6455c3fdce296fb675b087c104460db59dd546a41d56",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x73571878e650234424d488eaf740ae9910a3e3a1f7f65c435290ec0e404e2fd6",
      "signature": {
        "s": "0x49f23d0ca17f17eb2f35ce24e77431bcd27f54b5ad961f17b237dd99cd79535b",
        "r": "0xa3a6e7f1f32bfb45fea87d4d54beeaa6b7f59fb362c62bfd0b406d308f779a12",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1381468943",
    "total": "1381468943"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1381468943",
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
            "amount": "57640222903"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1381468"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0ZjI0ZGQzOC1mMmU3LTU2N2ItYWUzMS0wYzYwNjAwNmNkZGEifQ==",
    "nonce": 7678,
    "balances": {
      "current": "12960021230082466",
      "previous": "12960022612932877"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4bfde1b7906dcdf8fb7e779cb199fd65bf8004ff",
    "nonce": 15,
    "balances": {
      "current": "1381468943",
      "previous": "0"
    }
  },
  "blockNumber": "10114746",
  "created": "2020-05-22T08:58:40.113Z",
  "updated": "2020-05-22T08:58:40.187Z",
  "id": "5ec79440b0c6090011d5b2db"
}
```
* *stageAmount*: `1381468943`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000052578b0f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000052578b0f0000000000000000000000000000000000000000000000000000000052578b0f0d73c2e0b0e636fcc7643756e1e3b0571a3e6f9658efa53fd972469163e62b104e39c1e83f3be88370db6455c3fdce296fb675b087c104460db59dd546a41d563565609048d526670d6ec9ce2b8712baf4f43393d029dce62016840d1c623769000000000000000000000000000000000000000000000000000000000000001b73571878e650234424d488eaf740ae9910a3e3a1f7f65c435290ec0e404e2fd6a3a6e7f1f32bfb45fea87d4d54beeaa6b7f59fb362c62bfd0b406d308f779a1249f23d0ca17f17eb2f35ce24e77431bcd27f54b5ad961f17b237dd99cd79535b000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ba00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001dfe00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b1215b359a2000000000000000000000000000000000000000000000000002e0b12681ff90d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000015145c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6ba000b7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949305a6a49305a47517a4f43316d4d6d55334c5455324e3249745957557a4d533077597a59774e6a41774e6d4e6b5a47456966513d3d000000000000000000000000000000000000000000000000000000000000000f0000000000000000000000004bfde1b7906dcdf8fb7e779cb199fd65bf8004ff0000000000000000000000000000000000000000000000000000000052578b0f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0d73c2e0b0e636fcc7643756e1e3b0571a3e6f9658efa53fd972469163e62b10",
      "signature": {
        "s": "0x3565609048d526670d6ec9ce2b8712baf4f43393d029dce62016840d1c623769",
        "r": "0x4e39c1e83f3be88370db6455c3fdce296fb675b087c104460db59dd546a41d56",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x73571878e650234424d488eaf740ae9910a3e3a1f7f65c435290ec0e404e2fd6",
      "signature": {
        "s": "0x49f23d0ca17f17eb2f35ce24e77431bcd27f54b5ad961f17b237dd99cd79535b",
        "r": "0xa3a6e7f1f32bfb45fea87d4d54beeaa6b7f59fb362c62bfd0b406d308f779a12",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1381468943",
    "total": "1381468943"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1381468943",
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
            "amount": "57640222903"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1381468"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0ZjI0ZGQzOC1mMmU3LTU2N2ItYWUzMS0wYzYwNjAwNmNkZGEifQ==",
    "nonce": 7678,
    "balances": {
      "current": "12960021230082466",
      "previous": "12960022612932877"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4bfde1b7906dcdf8fb7e779cb199fd65bf8004ff",
    "nonce": 15,
    "balances": {
      "current": "1381468943",
      "previous": "0"
    }
  },
  "blockNumber": "10114746",
  "created": "2020-05-22T08:58:40.113Z",
  "updated": "2020-05-22T08:58:40.187Z",
  "id": "5ec79440b0c6090011d5b2db"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000052578b0f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1381468943`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`