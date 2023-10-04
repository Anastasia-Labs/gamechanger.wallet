
# Cardano Example Dapp

## **Arithmetic Macros**

    This demo will test and explore basic arithmetic macros


## Try it online: 

-  Visit [HTML5 Dapp](https://raw.githubusercontent.com/GameChangerFinance/gamechanger.wallet/main/examples/Arithmetic%20Macros.html)
-  Run [Standalone URL dapp connection](https://beta-wallet.gamechanger.finance/api/2/run/1-H4sIAAAAAAAAA6WSUWuDMBSF_0rIix0IRvfmW8ceuzHG9lxSDTUQTUiubEP870uqxsUJrVTwxkvu-U44psPAQTCc473mUNUMeIFeaKGlwTEumSk0V8BlYyc-Km5QyWqJvrgQCJgBRJsSsW8lpGboRI0V05lTTxz4Uc5igNneKqSGvQlsB9dny7cTmkGrm8_3wxsFYNrZVwAqTxIhCyoqaSB_JIQk7jwJVTwpqVJO2NrZDtOyfOLn17Z2zdJ-nEmPVJ__7F-OO23jziN2URo99LiPcbZBEUcpGWXNVpkrY50Wv84fAf7o2OZWk5SMFo7kDQZsiO-tQd2Ke8P0iF2U3RZmoIi96kqW_1Rr74bYQl4WL-qUkGlP9ybkEfYHDc9tOa3o4gXhSmbrBEJWb11wK_1t3RLpmt3oNpulc3tpBqN0yLvvfwFtghP4twQAAA)

## Source code:

- dapp connection code: [GCScript](Arithmetic%20Macros.gcscript)
- frontend + dapp connection code : [HTML5 dapp](Arithmetic%20Macros.html)

Dapp code was autogenerated by [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground)

## GCScript code (dapp connection):
```json
{
  "title": "Arithmetic Macros",
  "description": "This demo will test and explore basic arithmetic macros",
  "type": "script",
  "exportAs": "ArithmeticMacrosDemo",
  "returnURLPattern": "http://localhost:3000/demo/api/dapp",
  "run": {
    "addBigNum": {
      "type": "script",
      "run": {
        "1_arg": {
          "type": "macro",
          "run": "{addBigNum('1')}"
        },
        "2_arg": {
          "type": "macro",
          "run": "{addBigNum('1','10')}"
        },
        "n_arg": {
          "type": "macro",
          "run": "{addBigNum('1','10','100','1000','10000','100000','1000000')}"
        },
        "n_arg_types": {
          "type": "macro",
          "run": "{addBigNum('1',10,'100',1000,'10000',100000,'1000000')}"
        }
      }
    },
    "mulBigNum": {
      "type": "script",
      "run": {
        "1_arg": {
          "type": "macro",
          "run": "{mulBigNum('2')}"
        },
        "2_arg": {
          "type": "macro",
          "run": "{mulBigNum('2','2')}"
        },
        "n_arg": {
          "type": "macro",
          "run": "{mulBigNum('2','2','2','2','2','2','2')}"
        },
        "n_arg_types": {
          "type": "macro",
          "run": "{mulBigNum('2',2,'2',2,'2',2,'2')}"
        }
      }
    },
    "subBigNum": {
      "type": "script",
      "run": {
        "1_arg": {
          "type": "macro",
          "run": "{subBigNum('1111111')}"
        },
        "2_arg": {
          "type": "macro",
          "run": "{subBigNum('1111111','1111111')}"
        },
        "n_arg": {
          "type": "macro",
          "run": "{subBigNum('1111111','1000000','100000','10000','1000','100','10','1')}"
        },
        "n_arg_types": {
          "type": "macro",
          "run": "{subBigNum('1111111',1000000,'100000',10000,'1000',100,'10',1)}"
        }
      }
    }
  }
}
```

## Run standalone QR dapp connection: 

You can use [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground) in `QR URL Transport` mode to capture results

[![QR URL Transport](Arithmetic%20Macros.png)](https://beta-wallet.gamechanger.finance/api/2/run/1-H4sIAAAAAAAAA6WSUWuDMBSF_0rIix0IRvfmW8ceuzHG9lxSDTUQTUiubEP870uqxsUJrVTwxkvu-U44psPAQTCc473mUNUMeIFeaKGlwTEumSk0V8BlYyc-Km5QyWqJvrgQCJgBRJsSsW8lpGboRI0V05lTTxz4Uc5igNneKqSGvQlsB9dny7cTmkGrm8_3wxsFYNrZVwAqTxIhCyoqaSB_JIQk7jwJVTwpqVJO2NrZDtOyfOLn17Z2zdJ-nEmPVJ__7F-OO23jziN2URo99LiPcbZBEUcpGWXNVpkrY50Wv84fAf7o2OZWk5SMFo7kDQZsiO-tQd2Ke8P0iF2U3RZmoIi96kqW_1Rr74bYQl4WL-qUkGlP9ybkEfYHDc9tOa3o4gXhSmbrBEJWb11wK_1t3RLpmt3oNpulc3tpBqN0yLvvfwFtghP4twQAAA)

## Resources
- [GCScript documentation](https://beta-wallet.gamechanger.finance/doc/api/v2/api.html)
- [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground)
- [Youtube Tutorials](https://www.youtube.com/@gamechanger.finance)
- [Discord Support](https://discord.gg/vpbfyRaDKG)
- [Twitter News](https://twitter.com/GameChangerOk)
- [Website](https://gamechanger.finance)

## License
MIT 
    