# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xa43D2dE181edf0602D1Db046814dFB92EC786960`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000001aa9ca67eba8e3780e0000000000000000000000000000000000000000000000000000000e8e218b850000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000e8e218b8500000000000000000000000000000000000000000000000000000153b0a092ee6cabd9d41c668ccce697caba8350c55cba292b03cf3784030119a090e7647f040416b830b2366fdb692e3a9305c0e25a7ee6038b491e97f17ba5a5edb83bd24853e7b9ddf6b4266da3282526a391a00626fcfbff5c069ac7a6ceddb59b84e22e000000000000000000000000000000000000000000000000000000000000001ce4a658ee6c85a8ec1f2309660bba61a03a6b2eef636e294e51a5c538ef1990875f7168aca2cd3d14e5f2293b4cddda1f24046471edbb4bc5afc4a7a3ec16856d149079208cbe67e26a2cd652a3430a2c13725bd6287c3c461a704ba5e0fc7051000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b204000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000049c3306947a722cecfca0000000000000000000000000000000000000000000049c3306947b5b4aa3f0800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000003b9e3b90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d984b9afee4237badb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e6d4978593255794d69307a4f5745784c5455344d6a45745954426a5a6930314d324d305a5463305a4755344e6a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000024000000000000000000000000a43d2de181edf0602d1db046814dfb92ec78696000000000000000000000000000000000000000000000001aa9ca67eba8e3780e00000000000000000000000000000000000000000000001aa9ca67dd1ac1ec8900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6cabd9d41c668ccce697caba8350c55cba292b03cf3784030119a090e7647f04",
      "signature": {
        "s": "0x53e7b9ddf6b4266da3282526a391a00626fcfbff5c069ac7a6ceddb59b84e22e",
        "r": "0x0416b830b2366fdb692e3a9305c0e25a7ee6038b491e97f17ba5a5edb83bd248",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe4a658ee6c85a8ec1f2309660bba61a03a6b2eef636e294e51a5c538ef199087",
      "signature": {
        "s": "0x149079208cbe67e26a2cd652a3430a2c13725bd6287c3c461a704ba5e0fc7051",
        "r": "0x5f7168aca2cd3d14e5f2293b4cddda1f24046471edbb4bc5afc4a7a3ec16856d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "62514105221",
    "total": "1458957226734"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "62514105221",
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
            "amount": "27624339747064744753883"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "62514105"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1NmIxY2UyMi0zOWExLTU4MjEtYTBjZi01M2M0ZTc0ZGU4NjMifQ==",
    "nonce": 111108,
    "balances": {
      "current": "348333356742027007414218",
      "previous": "348333356742089584033544"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa43d2de181edf0602d1db046814dfb92ec786960",
    "nonce": 36,
    "balances": {
      "current": "491850051516002170894",
      "previous": "491850051453488065673"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:35.951Z",
  "updated": "2022-05-04T08:56:36.034Z",
  "id": "62723fc3bbd75600116d064a"
}
```
* *stageAmount*: `491850051516002170894`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000e8e218b850000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000e8e218b8500000000000000000000000000000000000000000000000000000153b0a092ee6cabd9d41c668ccce697caba8350c55cba292b03cf3784030119a090e7647f040416b830b2366fdb692e3a9305c0e25a7ee6038b491e97f17ba5a5edb83bd24853e7b9ddf6b4266da3282526a391a00626fcfbff5c069ac7a6ceddb59b84e22e000000000000000000000000000000000000000000000000000000000000001ce4a658ee6c85a8ec1f2309660bba61a03a6b2eef636e294e51a5c538ef1990875f7168aca2cd3d14e5f2293b4cddda1f24046471edbb4bc5afc4a7a3ec16856d149079208cbe67e26a2cd652a3430a2c13725bd6287c3c461a704ba5e0fc7051000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b204000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000049c3306947a722cecfca0000000000000000000000000000000000000000000049c3306947b5b4aa3f0800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000003b9e3b90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d984b9afee4237badb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e6d4978593255794d69307a4f5745784c5455344d6a45745954426a5a6930314d324d305a5463305a4755344e6a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000024000000000000000000000000a43d2de181edf0602d1db046814dfb92ec78696000000000000000000000000000000000000000000000001aa9ca67eba8e3780e00000000000000000000000000000000000000000000001aa9ca67dd1ac1ec8900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6cabd9d41c668ccce697caba8350c55cba292b03cf3784030119a090e7647f04",
      "signature": {
        "s": "0x53e7b9ddf6b4266da3282526a391a00626fcfbff5c069ac7a6ceddb59b84e22e",
        "r": "0x0416b830b2366fdb692e3a9305c0e25a7ee6038b491e97f17ba5a5edb83bd248",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe4a658ee6c85a8ec1f2309660bba61a03a6b2eef636e294e51a5c538ef199087",
      "signature": {
        "s": "0x149079208cbe67e26a2cd652a3430a2c13725bd6287c3c461a704ba5e0fc7051",
        "r": "0x5f7168aca2cd3d14e5f2293b4cddda1f24046471edbb4bc5afc4a7a3ec16856d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "62514105221",
    "total": "1458957226734"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "62514105221",
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
            "amount": "27624339747064744753883"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "62514105"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1NmIxY2UyMi0zOWExLTU4MjEtYTBjZi01M2M0ZTc0ZGU4NjMifQ==",
    "nonce": 111108,
    "balances": {
      "current": "348333356742027007414218",
      "previous": "348333356742089584033544"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa43d2de181edf0602d1db046814dfb92ec786960",
    "nonce": 36,
    "balances": {
      "current": "491850051516002170894",
      "previous": "491850051453488065673"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:35.951Z",
  "updated": "2022-05-04T08:56:36.034Z",
  "id": "62723fc3bbd75600116d064a"
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
0x0f200f9b00000000000000000000000000000000000000000000001aa9ca67eba8e3780e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `491850051516002170894`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`