# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x64406A467612A53e69d49bB53e3714D42d254588`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000001a7d28e0000000000000000000000000000000000000000000000000000000001a7d28e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000001a7d28e0000000000000000000000000000000000000000000000000000000001a7d28e0c46ff99289702dc5dea1c7f96d9e1de06ded96280d313a36576fe7d6548e27636cc10062f2f3fdf3f0c392b32bb53ea944f7d3545931a6727d861d54b9d1b330e2204ef219f1c79ff77be93b1985123fa31a82707c8c79cecb6f0dfd6f7f60e000000000000000000000000000000000000000000000000000000000000001bb143f22a87a4614a73892694c2d57df7219381f8c076934eae29dbb0930dd045a6149abd324360ef43340556cf0508381f08121e139912b0a05e4ef6c04baf1a536dd8ab35b1ef30590a20dfde3166a0797da52ca97bbb6ed42496b9294e6201000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56890000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000188b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ab90d355c85000000000000000000000000000000000000000000000000002e1ab90edd9b9200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000006c7f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000096addc5c0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784e444669597a4e6c4e5330794e3249794c5455794d4745744f546332597930344f544d355a6a67335a6a646b4f57456966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000064406a467612a53e69d49bb53e3714d42d2545880000000000000000000000000000000000000000000000000000000001a7d28e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0c46ff99289702dc5dea1c7f96d9e1de06ded96280d313a36576fe7d6548e276",
      "signature": {
        "s": "0x0e2204ef219f1c79ff77be93b1985123fa31a82707c8c79cecb6f0dfd6f7f60e",
        "r": "0x36cc10062f2f3fdf3f0c392b32bb53ea944f7d3545931a6727d861d54b9d1b33",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb143f22a87a4614a73892694c2d57df7219381f8c076934eae29dbb0930dd045",
      "signature": {
        "s": "0x536dd8ab35b1ef30590a20dfde3166a0797da52ca97bbb6ed42496b9294e6201",
        "r": "0xa6149abd324360ef43340556cf0508381f08121e139912b0a05e4ef6c04baf1a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "27775630",
    "total": "27775630"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "27775630",
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
            "amount": "40447624640"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "27775"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxNDFiYzNlNS0yN2IyLTUyMGEtOTc2Yy04OTM5Zjg3ZjdkOWEifQ==",
    "nonce": 6283,
    "balances": {
      "current": "12977231021563013",
      "previous": "12977231049366418"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x64406a467612a53e69d49bb53e3714d42d254588",
    "nonce": 22,
    "balances": {
      "current": "27775630",
      "previous": "0"
    }
  },
  "blockNumber": "10114697",
  "created": "2020-05-22T08:47:52.761Z",
  "updated": "2020-05-22T08:47:52.842Z",
  "id": "5ec791b8005df800101bca67"
}
```
* *stageAmount*: `27775630`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000001a7d28e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000001a7d28e0000000000000000000000000000000000000000000000000000000001a7d28e0c46ff99289702dc5dea1c7f96d9e1de06ded96280d313a36576fe7d6548e27636cc10062f2f3fdf3f0c392b32bb53ea944f7d3545931a6727d861d54b9d1b330e2204ef219f1c79ff77be93b1985123fa31a82707c8c79cecb6f0dfd6f7f60e000000000000000000000000000000000000000000000000000000000000001bb143f22a87a4614a73892694c2d57df7219381f8c076934eae29dbb0930dd045a6149abd324360ef43340556cf0508381f08121e139912b0a05e4ef6c04baf1a536dd8ab35b1ef30590a20dfde3166a0797da52ca97bbb6ed42496b9294e6201000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56890000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000188b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ab90d355c85000000000000000000000000000000000000000000000000002e1ab90edd9b9200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000006c7f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000096addc5c0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784e444669597a4e6c4e5330794e3249794c5455794d4745744f546332597930344f544d355a6a67335a6a646b4f57456966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000064406a467612a53e69d49bb53e3714d42d2545880000000000000000000000000000000000000000000000000000000001a7d28e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0c46ff99289702dc5dea1c7f96d9e1de06ded96280d313a36576fe7d6548e276",
      "signature": {
        "s": "0x0e2204ef219f1c79ff77be93b1985123fa31a82707c8c79cecb6f0dfd6f7f60e",
        "r": "0x36cc10062f2f3fdf3f0c392b32bb53ea944f7d3545931a6727d861d54b9d1b33",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb143f22a87a4614a73892694c2d57df7219381f8c076934eae29dbb0930dd045",
      "signature": {
        "s": "0x536dd8ab35b1ef30590a20dfde3166a0797da52ca97bbb6ed42496b9294e6201",
        "r": "0xa6149abd324360ef43340556cf0508381f08121e139912b0a05e4ef6c04baf1a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "27775630",
    "total": "27775630"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "27775630",
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
            "amount": "40447624640"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "27775"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxNDFiYzNlNS0yN2IyLTUyMGEtOTc2Yy04OTM5Zjg3ZjdkOWEifQ==",
    "nonce": 6283,
    "balances": {
      "current": "12977231021563013",
      "previous": "12977231049366418"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x64406a467612a53e69d49bb53e3714d42d254588",
    "nonce": 22,
    "balances": {
      "current": "27775630",
      "previous": "0"
    }
  },
  "blockNumber": "10114697",
  "created": "2020-05-22T08:47:52.761Z",
  "updated": "2020-05-22T08:47:52.842Z",
  "id": "5ec791b8005df800101bca67"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000001a7d28e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `27775630`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`