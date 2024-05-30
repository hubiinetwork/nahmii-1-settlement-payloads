# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x02Ae62ec4D42618Ae587ba1409E279350Ea7f7B5`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000069f50c830000000000000000000000000000000000000000000000000000000069f50c83000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000069f50c830000000000000000000000000000000000000000000000000000000069f50c83500201c9f12ca023fdece0e3daefecafe3f516ad66af1b31be6da3e894c213a218d312f510e6c489d862ca650db7e782fd2ca84868dc7909258418a33d49fe3660bc6f2dda99012cb8d31202676ef428c5278ce4afd85ddd29c4b4db18846cfd000000000000000000000000000000000000000000000000000000000000001c4c6fd36e68a7c5c1fdb6d7f76e15a287807aecefd8c43ef9815c4035b5b1aa2c2dddda75697eabec38bff4e0063f17f93af9e73825e9d72c31667f301392861f23000cfd54f8591aaa1a56c9d9b7361c03b16f332b677bb50e0a9cd840123420000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5676000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000016fb00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b41964a8a9d000000000000000000000000000000000000000000000000002e1b42005ab72300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001b2003000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000947f2b9ab000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694f546b344d4759794f4330784f4445314c54566c4e4745744f5755314d5330314d7a52694e4451795a5451305a44636966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000002ae62ec4d42618ae587ba1409e279350ea7f7b50000000000000000000000000000000000000000000000000000000069f50c83000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x500201c9f12ca023fdece0e3daefecafe3f516ad66af1b31be6da3e894c213a2",
      "signature": {
        "s": "0x60bc6f2dda99012cb8d31202676ef428c5278ce4afd85ddd29c4b4db18846cfd",
        "r": "0x18d312f510e6c489d862ca650db7e782fd2ca84868dc7909258418a33d49fe36",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4c6fd36e68a7c5c1fdb6d7f76e15a287807aecefd8c43ef9815c4035b5b1aa2c",
      "signature": {
        "s": "0x23000cfd54f8591aaa1a56c9d9b7361c03b16f332b677bb50e0a9cd840123420",
        "r": "0x2dddda75697eabec38bff4e0063f17f93af9e73825e9d72c31667f301392861f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1777667203",
    "total": "1777667203"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1777667203",
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
            "amount": "39861795243"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1777667"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiOTk4MGYyOC0xODE1LTVlNGEtOWU1MS01MzRiNDQyZTQ0ZDcifQ==",
    "nonce": 5883,
    "balances": {
      "current": "12977817436981917",
      "previous": "12977819216426787"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x02ae62ec4d42618ae587ba1409e279350ea7f7b5",
    "nonce": 22,
    "balances": {
      "current": "1777667203",
      "previous": "0"
    }
  },
  "blockNumber": "10114678",
  "created": "2020-05-22T08:44:43.739Z",
  "updated": "2020-05-22T08:44:44.814Z",
  "id": "5ec790fbe5756b00111b86fc"
}
```
* *stageAmount*: `1777667203`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000069f50c83000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000069f50c830000000000000000000000000000000000000000000000000000000069f50c83500201c9f12ca023fdece0e3daefecafe3f516ad66af1b31be6da3e894c213a218d312f510e6c489d862ca650db7e782fd2ca84868dc7909258418a33d49fe3660bc6f2dda99012cb8d31202676ef428c5278ce4afd85ddd29c4b4db18846cfd000000000000000000000000000000000000000000000000000000000000001c4c6fd36e68a7c5c1fdb6d7f76e15a287807aecefd8c43ef9815c4035b5b1aa2c2dddda75697eabec38bff4e0063f17f93af9e73825e9d72c31667f301392861f23000cfd54f8591aaa1a56c9d9b7361c03b16f332b677bb50e0a9cd840123420000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5676000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000016fb00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b41964a8a9d000000000000000000000000000000000000000000000000002e1b42005ab72300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001b2003000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000947f2b9ab000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694f546b344d4759794f4330784f4445314c54566c4e4745744f5755314d5330314d7a52694e4451795a5451305a44636966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000002ae62ec4d42618ae587ba1409e279350ea7f7b50000000000000000000000000000000000000000000000000000000069f50c83000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x500201c9f12ca023fdece0e3daefecafe3f516ad66af1b31be6da3e894c213a2",
      "signature": {
        "s": "0x60bc6f2dda99012cb8d31202676ef428c5278ce4afd85ddd29c4b4db18846cfd",
        "r": "0x18d312f510e6c489d862ca650db7e782fd2ca84868dc7909258418a33d49fe36",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4c6fd36e68a7c5c1fdb6d7f76e15a287807aecefd8c43ef9815c4035b5b1aa2c",
      "signature": {
        "s": "0x23000cfd54f8591aaa1a56c9d9b7361c03b16f332b677bb50e0a9cd840123420",
        "r": "0x2dddda75697eabec38bff4e0063f17f93af9e73825e9d72c31667f301392861f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1777667203",
    "total": "1777667203"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1777667203",
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
            "amount": "39861795243"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1777667"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiOTk4MGYyOC0xODE1LTVlNGEtOWU1MS01MzRiNDQyZTQ0ZDcifQ==",
    "nonce": 5883,
    "balances": {
      "current": "12977817436981917",
      "previous": "12977819216426787"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x02ae62ec4d42618ae587ba1409e279350ea7f7b5",
    "nonce": 22,
    "balances": {
      "current": "1777667203",
      "previous": "0"
    }
  },
  "blockNumber": "10114678",
  "created": "2020-05-22T08:44:43.739Z",
  "updated": "2020-05-22T08:44:44.814Z",
  "id": "5ec790fbe5756b00111b86fc"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000069f50c83000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1777667203`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`