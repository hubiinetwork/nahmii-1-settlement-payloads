# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd03F1fC3f80B65BBA30063185614C972697A3294`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000e799300000000000000000000000000000000000000000000000000000000000e7993000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000e799300000000000000000000000000000000000000000000000000000000000e7993ab4e3621c343f42bc59ee2db351fe11cbb6a8c29245f8a3048e136e1caaddd27e7aecf4e2ad6449f513ab505a16d066d45d214bfd472db46fd4287c540b1424c3eb81fbfb45e175610a6b04c938e448453d687a299969dc453c8532ac0fd24d6000000000000000000000000000000000000000000000000000000000000001c42f85361f318e919554e1ccd101e2d05fa80c1c498682d7ddc8d82aef1f9556b14e24da607291a2290de3b37e1a67028d127ce02bf486c19e3978cd1642ac0ee00b8155fe887048f82a7596f546c402797a5de94da9461a5fa632a75345979c4000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56c200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e8e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b032f0bf8f3000000000000000000000000000000000000000000000000002e0b032f1a763a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000003b4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6f6f93dc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d5759344e5455334e69316b4f57517a4c54566d4e445574595449314e79303059325a694d4755784e575a6b4f57556966513d3d0000000000000000000000000000000000000000000000000000000000000005000000000000000000000000d03f1fc3f80b65bba30063185614c972697a329400000000000000000000000000000000000000000000000000000000000e7993000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xab4e3621c343f42bc59ee2db351fe11cbb6a8c29245f8a3048e136e1caaddd27",
      "signature": {
        "s": "0x3eb81fbfb45e175610a6b04c938e448453d687a299969dc453c8532ac0fd24d6",
        "r": "0xe7aecf4e2ad6449f513ab505a16d066d45d214bfd472db46fd4287c540b1424c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x42f85361f318e919554e1ccd101e2d05fa80c1c498682d7ddc8d82aef1f9556b",
      "signature": {
        "s": "0x00b8155fe887048f82a7596f546c402797a5de94da9461a5fa632a75345979c4",
        "r": "0x14e24da607291a2290de3b37e1a67028d127ce02bf486c19e3978cd1642ac0ee",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "948627",
    "total": "948627"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "948627",
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
            "amount": "57704158172"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "948"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MWY4NTU3Ni1kOWQzLTVmNDUtYTI1Ny00Y2ZiMGUxNWZkOWUifQ==",
    "nonce": 7822,
    "balances": {
      "current": "12959957230811379",
      "previous": "12959957231760954"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd03f1fc3f80b65bba30063185614c972697a3294",
    "nonce": 5,
    "balances": {
      "current": "948627",
      "previous": "0"
    }
  },
  "blockNumber": "10114754",
  "created": "2020-05-22T08:59:49.748Z",
  "updated": "2020-05-22T08:59:49.817Z",
  "id": "5ec79485005df800101bcc7b"
}
```
* *stageAmount*: `948627`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000e7993000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000e799300000000000000000000000000000000000000000000000000000000000e7993ab4e3621c343f42bc59ee2db351fe11cbb6a8c29245f8a3048e136e1caaddd27e7aecf4e2ad6449f513ab505a16d066d45d214bfd472db46fd4287c540b1424c3eb81fbfb45e175610a6b04c938e448453d687a299969dc453c8532ac0fd24d6000000000000000000000000000000000000000000000000000000000000001c42f85361f318e919554e1ccd101e2d05fa80c1c498682d7ddc8d82aef1f9556b14e24da607291a2290de3b37e1a67028d127ce02bf486c19e3978cd1642ac0ee00b8155fe887048f82a7596f546c402797a5de94da9461a5fa632a75345979c4000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56c200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e8e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b032f0bf8f3000000000000000000000000000000000000000000000000002e0b032f1a763a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000003b4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6f6f93dc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d5759344e5455334e69316b4f57517a4c54566d4e445574595449314e79303059325a694d4755784e575a6b4f57556966513d3d0000000000000000000000000000000000000000000000000000000000000005000000000000000000000000d03f1fc3f80b65bba30063185614c972697a329400000000000000000000000000000000000000000000000000000000000e7993000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xab4e3621c343f42bc59ee2db351fe11cbb6a8c29245f8a3048e136e1caaddd27",
      "signature": {
        "s": "0x3eb81fbfb45e175610a6b04c938e448453d687a299969dc453c8532ac0fd24d6",
        "r": "0xe7aecf4e2ad6449f513ab505a16d066d45d214bfd472db46fd4287c540b1424c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x42f85361f318e919554e1ccd101e2d05fa80c1c498682d7ddc8d82aef1f9556b",
      "signature": {
        "s": "0x00b8155fe887048f82a7596f546c402797a5de94da9461a5fa632a75345979c4",
        "r": "0x14e24da607291a2290de3b37e1a67028d127ce02bf486c19e3978cd1642ac0ee",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "948627",
    "total": "948627"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "948627",
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
            "amount": "57704158172"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "948"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MWY4NTU3Ni1kOWQzLTVmNDUtYTI1Ny00Y2ZiMGUxNWZkOWUifQ==",
    "nonce": 7822,
    "balances": {
      "current": "12959957230811379",
      "previous": "12959957231760954"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd03f1fc3f80b65bba30063185614c972697a3294",
    "nonce": 5,
    "balances": {
      "current": "948627",
      "previous": "0"
    }
  },
  "blockNumber": "10114754",
  "created": "2020-05-22T08:59:49.748Z",
  "updated": "2020-05-22T08:59:49.817Z",
  "id": "5ec79485005df800101bcc7b"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000e7993000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `948627`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`