
# Cardano Example Dapp

## **Key derivation formats**

    Explore the different ways to derive/obtain keys and obtain all results under the same format


## Try it online: 

-  Visit [HTML5 Dapp](https://raw.githubusercontent.com/GameChangerFinance/gamechanger.wallet/main/examples/Key%20derivation%20formats.html)
-  Run [Standalone URL dapp connection](https://beta-wallet.gamechanger.finance/api/2/run/1-H4sIAAAAAAAAA61V0YriMBT9lZDngtZdYfFN3H2Qhd2BfZiHRSQ2txpsk5Lc7lik_743bbWpo6PCiFRzcnLuSXKSHjlWBfAZd4lVBfKIo8LMAz-hYhKs-idQGc1SY3OBjggSWi6hRPtxKDJjgeEOmFRpChY0sjdROYamFYCR2aBQmu2BUKEl69oiy5gFV2boWKmJ26g4kUNXjqrBoTAW545KSYGCEFtS3SPPSeFPAVr6RjeJLWADKb19KTeZSmgSvI5aLoo9XHAJuqS2js-QC0a0XQ0Y8X3Xt3a-YDz2_zU590vZIURS3l4LUFMkiSk1LmmqBz6bEiAlzd91QDym-mvnfQ71OqTXa6byqF7rZmGK6r3HBo14IXBHYD6Kv00nO3rG092IvuMRlQ1MXYoE6G2RSSNSk0zpaLVfjd27QiQQLm1mhFwYnaotCZUF7TQsZbPkuSEkExVY4v89DzirUK9CyNtO7-tFIILVp_1q0utOue47vw86g0z3lFfKJyBzgEi-HduCBkvOJNtUTDDvjbXDfNQRHPqEs7Bsvaqjs2efsIi_nZwvpTc9cLmKLqZwVH4r6_WRhP2TmvQT7rtvBrtef7Ae7fB39OdD-qTw42l9RDhIW0-8ldzPE5ycBO_w4tF92tj767b2Ljl-hjx5hvzlGfLXAXnlg83pZPTnsD_MBC9K698D4SkNcn9xNuv2Nl3qq2Kn91J37dOZvLiW6SIPruv6HLTfOqtu0pqSQS781H1mU5UR5IcpN291-AxtCf7-MqQ4D1IcPywvLKpUJPiL0jgsMzwV8bUy008o02ythVQdroXWX8_0-Q8LoIT6DQgAAA)

## Source code:

- dapp connection code: [GCScript](Key%20derivation%20formats.gcscript)
- frontend + dapp connection code : [HTML5 dapp](Key%20derivation%20formats.html)

Dapp code was autogenerated by [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground)

## GCScript code (dapp connection):
```json
{
  "type": "script",
  "title": "Key derivation formats",
  "description": "Explore the different ways to derive/obtain keys and obtain all results under the same format",
  "exportAs": "data",
  "run": {
    "mainSpend": {
      "type": "getSpendingPublicKey"
    },
    "mainStake": {
      "type": "getStakingPublicKey"
    },
    "derivePublicKeys": {
      "type": "deriveKeys",
      "keys": {
        "_spend10": {
          "name": "spend10",
          "kind": "spend",
          "accountIndex": 5,
          "addressIndex": 10
        },
        "_stake10": {
          "name": "stake10",
          "kind": "stake",
          "accountIndex": 5,
          "addressIndex": 10
        },
        "_spend10Copy": {
          "name": "spend10Copy",
          "path": "m/1852h/1815h/5h/0/10"
        },
        "_stake10Copy": {
          "name": "stake10Copy",
          "path": "m/1852h/1815h/5h/2/10"
        }
      }
    },
    "usingWorkspaces": {
      "type": "loadConfig",
      "updateId": "demo",
      "layers": [
        {
          "type": "Workspace",
          "items": [
            {
              "namePattern": "derivations",
              "titlePattern": "Derivations",
              "descriptionPattern": "Wallet settings generated by a demo script to test key derivations"
            }
          ]
        },
        {
          "type": "Key",
          "workspaceIds": [
            "derivations"
          ],
          "namePattern": "{index}_{key}_{kind}_{accountIndex}_{addressIndex}",
          "items": [
            {
              "namePattern": "{kind}{addressIndex}",
              "kind": "spend",
              "accountIndex": 5,
              "addressIndex": 10
            },
            {
              "namePattern": "{kind}{addressIndex}",
              "kind": "stake",
              "accountIndex": 5,
              "addressIndex": 10
            },
            {
              "namePattern": "{kind}{addressIndex}Copy",
              "pathPattern": "m/1852h/1815h/5h/0/10"
            },
            {
              "namePattern": "{kind}{addressIndex}Copy",
              "pathPattern": "m/1852h/1815h/5h/2/10"
            },
            {
              "pathPattern": "m/1852h/1815h/5h/1/0"
            },
            {
              "pathPattern": "m/1852h/1815h/0h/0/{index}"
            },
            {
              "pathPattern": "m/1852h/1815h/1h/0/{index}"
            },
            {
              "pathPattern": "m/1852h/1815h/2h/0/{index}"
            },
            {
              "pathPattern": "m/1852h/1815h/3h/0/{index}"
            },
            {
              "pathPattern": "m/1852h/1815h/4h/0/{index}"
            }
          ]
        }
      ]
    },
    "setWorkspace": {
      "type": "setCurrentWorkspace",
      "workspaceId": "derivations"
    },
    "keysInWorkspace": {
      "type": "script",
      "run": {
        "allKeys": {
          "type": "getPublicKeys"
        },
        "accountOnly": {
          "type": "getPublicKeys",
          "keyPattern": "{path}",
          "filter": {
            "isAccount": true
          }
        },
        "onlyAccountIndex1": {
          "type": "getPublicKeys",
          "keyPattern": "{artifactName}",
          "filter": {
            "accountIndex": 1
          }
        },
        "onlyAccountIndex5": {
          "type": "getPublicKeys",
          "keyPattern": "{artifactName}",
          "filter": {
            "pathPrefix": "m/1852h/1815h/5h/"
          }
        }
      }
    }
  }
}
```

## Run standalone QR dapp connection: 

You can use [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground) in `QR URL Transport` mode to capture results

[![QR URL Transport](Key%20derivation%20formats.png)](https://beta-wallet.gamechanger.finance/api/2/run/1-H4sIAAAAAAAAA61V0YriMBT9lZDngtZdYfFN3H2Qhd2BfZiHRSQ2txpsk5Lc7lik_743bbWpo6PCiFRzcnLuSXKSHjlWBfAZd4lVBfKIo8LMAz-hYhKs-idQGc1SY3OBjggSWi6hRPtxKDJjgeEOmFRpChY0sjdROYamFYCR2aBQmu2BUKEl69oiy5gFV2boWKmJ26g4kUNXjqrBoTAW545KSYGCEFtS3SPPSeFPAVr6RjeJLWADKb19KTeZSmgSvI5aLoo9XHAJuqS2js-QC0a0XQ0Y8X3Xt3a-YDz2_zU590vZIURS3l4LUFMkiSk1LmmqBz6bEiAlzd91QDym-mvnfQ71OqTXa6byqF7rZmGK6r3HBo14IXBHYD6Kv00nO3rG092IvuMRlQ1MXYoE6G2RSSNSk0zpaLVfjd27QiQQLm1mhFwYnaotCZUF7TQsZbPkuSEkExVY4v89DzirUK9CyNtO7-tFIILVp_1q0utOue47vw86g0z3lFfKJyBzgEi-HduCBkvOJNtUTDDvjbXDfNQRHPqEs7Bsvaqjs2efsIi_nZwvpTc9cLmKLqZwVH4r6_WRhP2TmvQT7rtvBrtef7Ae7fB39OdD-qTw42l9RDhIW0-8ldzPE5ycBO_w4tF92tj767b2Ljl-hjx5hvzlGfLXAXnlg83pZPTnsD_MBC9K698D4SkNcn9xNuv2Nl3qq2Kn91J37dOZvLiW6SIPruv6HLTfOqtu0pqSQS781H1mU5UR5IcpN291-AxtCf7-MqQ4D1IcPywvLKpUJPiL0jgsMzwV8bUy008o02ythVQdroXWX8_0-Q8LoIT6DQgAAA)

## Resources
- [GCScript documentation](https://beta-wallet.gamechanger.finance/doc/api/v2/api.html)
- [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground)
- [Youtube Tutorials](https://www.youtube.com/@gamechanger.finance)
- [Discord Support](https://discord.gg/vpbfyRaDKG)
- [Twitter News](https://twitter.com/GameChangerOk)
- [Website](https://gamechanger.finance)

## License
MIT 
    