# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xBF0d1C02aC8eDa6E6c24b5203BbF7e92298d10B0`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000c6ac1ed000000000000000000000000000000000000000000000000000000000c6ac1ed0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000c6ac1ed000000000000000000000000000000000000000000000000000000000c6ac1ed01cca55589247514b95fef0e550f098b9fbc2636805a9ba46b5c4225bcf24e7d72930463c859542d0d90d320f845d5f05a1dd639f4b451e868d345ac4969cf42e2dfb1106e79834bcd389d3c222610b048be6febceea3b52b3b2c458fb9b7a6aa000000000000000000000000000000000000000000000000000000000000001ccc766e78d127ee18bc3f5947226ca376c7c7ae3bbcc9ddd5e89bf1504e8a88a3e863705ff6136cca6953ab556f5a19d9f370c7e4607cd6ff929cf598d33c5e392c79cbef6bd6a6a73823677229fecfbc320aacda7ea5c17097872ede65dbe122000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a566a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000159d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d540e4aac23000000000000000000000000000000000000000000000000002e1d54d529a72300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000032dc30000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008c048a838000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e7a6b305a57526b5969307a4e7a56694c5456684e4459744f5449775969316a596a466d5a474e69596a49774d44596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000bf0d1c02ac8eda6e6c24b5203bbf7e92298d10b000000000000000000000000000000000000000000000000000000000c6ac1ed0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1cca55589247514b95fef0e550f098b9fbc2636805a9ba46b5c4225bcf24e7d7",
      "signature": {
        "s": "0x2dfb1106e79834bcd389d3c222610b048be6febceea3b52b3b2c458fb9b7a6aa",
        "r": "0x2930463c859542d0d90d320f845d5f05a1dd639f4b451e868d345ac4969cf42e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcc766e78d127ee18bc3f5947226ca376c7c7ae3bbcc9ddd5e89bf1504e8a88a3",
      "signature": {
        "s": "0x2c79cbef6bd6a6a73823677229fecfbc320aacda7ea5c17097872ede65dbe122",
        "r": "0xe863705ff6136cca6953ab556f5a19d9f370c7e4607cd6ff929cf598d33c5e39",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3333168848",
    "total": "3333168848"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3333168848",
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
            "amount": "37585725496"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3333168"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiNzk0ZWRkYi0zNzViLTVhNDYtOTIwYi1jYjFmZGNiYjIwMDYifQ==",
    "nonce": 5533,
    "balances": {
      "current": "12980095782923299",
      "previous": "12980099119425315"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbf0d1c02ac8eda6e6c24b5203bbf7e92298d10b0",
    "nonce": 22,
    "balances": {
      "current": "3333168848",
      "previous": "0"
    }
  },
  "blockNumber": "10114666",
  "created": "2020-05-22T08:41:53.508Z",
  "updated": "2020-05-22T08:41:53.577Z",
  "id": "5ec79051005df800101bc972"
}
```
* *stageAmount*: `3333168848`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000c6ac1ed0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000c6ac1ed000000000000000000000000000000000000000000000000000000000c6ac1ed01cca55589247514b95fef0e550f098b9fbc2636805a9ba46b5c4225bcf24e7d72930463c859542d0d90d320f845d5f05a1dd639f4b451e868d345ac4969cf42e2dfb1106e79834bcd389d3c222610b048be6febceea3b52b3b2c458fb9b7a6aa000000000000000000000000000000000000000000000000000000000000001ccc766e78d127ee18bc3f5947226ca376c7c7ae3bbcc9ddd5e89bf1504e8a88a3e863705ff6136cca6953ab556f5a19d9f370c7e4607cd6ff929cf598d33c5e392c79cbef6bd6a6a73823677229fecfbc320aacda7ea5c17097872ede65dbe122000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a566a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000159d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d540e4aac23000000000000000000000000000000000000000000000000002e1d54d529a72300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000032dc30000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008c048a838000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e7a6b305a57526b5969307a4e7a56694c5456684e4459744f5449775969316a596a466d5a474e69596a49774d44596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000bf0d1c02ac8eda6e6c24b5203bbf7e92298d10b000000000000000000000000000000000000000000000000000000000c6ac1ed0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1cca55589247514b95fef0e550f098b9fbc2636805a9ba46b5c4225bcf24e7d7",
      "signature": {
        "s": "0x2dfb1106e79834bcd389d3c222610b048be6febceea3b52b3b2c458fb9b7a6aa",
        "r": "0x2930463c859542d0d90d320f845d5f05a1dd639f4b451e868d345ac4969cf42e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcc766e78d127ee18bc3f5947226ca376c7c7ae3bbcc9ddd5e89bf1504e8a88a3",
      "signature": {
        "s": "0x2c79cbef6bd6a6a73823677229fecfbc320aacda7ea5c17097872ede65dbe122",
        "r": "0xe863705ff6136cca6953ab556f5a19d9f370c7e4607cd6ff929cf598d33c5e39",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3333168848",
    "total": "3333168848"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3333168848",
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
            "amount": "37585725496"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3333168"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiNzk0ZWRkYi0zNzViLTVhNDYtOTIwYi1jYjFmZGNiYjIwMDYifQ==",
    "nonce": 5533,
    "balances": {
      "current": "12980095782923299",
      "previous": "12980099119425315"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbf0d1c02ac8eda6e6c24b5203bbf7e92298d10b0",
    "nonce": 22,
    "balances": {
      "current": "3333168848",
      "previous": "0"
    }
  },
  "blockNumber": "10114666",
  "created": "2020-05-22T08:41:53.508Z",
  "updated": "2020-05-22T08:41:53.577Z",
  "id": "5ec79051005df800101bc972"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000c6ac1ed0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3333168848`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`