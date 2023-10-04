
# Cardano Example Dapp

## **Native asset minter and burner**

    Native asset minter and later burner of previously minted assets, in 2 secuential transactions


## Try it online: 

-  Visit [HTML5 Dapp](https://raw.githubusercontent.com/GameChangerFinance/gamechanger.wallet/main/examples/Native%20asset%20minter%20and%20burner.html)
-  Run [Standalone URL dapp connection](https://beta-wallet.gamechanger.finance/api/2/run/1-H4sIAAAAAAAAA81UTW_bMAz9L7p0A1zbw26-ddihRbciWDPsMPSgWGwiVJY8id4cBP7vI_0V56NLMwzofLFFUo-PT8_aCFyXIDIRcq9LFJHwgJW3X798mklE8JZyK8QySxLjcmlWLmD2Pk3TREHhElnqRMmy5I0V1W6EghKsAptrCLw-wO_KdAgV-EmBAq9_wi2sAxU98Sv7vhFWFpzsqymhrWI07kFLmeeusnhDDWuRpRRQykMIQ6B5aCJRaIvaLmfO6Hw96WglUsf7gVjPkPJltSAe1zKsrhlFbJaAby5yma8gno4Xd7TiNN7ZcfG2EQ09kVhU2qjP1H7StY3Na2rYz8YBvGSSFMOaS3nRzV-2pG_Un1jszBd3Y0yokCghQI_Xft51jb9pYz5qmLsnsFT1o5KEg6SQeJemookOq-8cPrNBkNIPkfil0ZL83clP9Q3DWCPRXvdz55rKG_TS7qnLoXkdenW3FuY4qK3KrMZO5_GoYqz7JjSPApTagJqBL-iwtbO08VGaANy-WhQa9wm0waMU2gzusdghMQzUjtjb50Pl7Wn7LLjqf7HPZeufVzLEnl4nDDHqdtwQDHauIfYJvMAQUxYHhmC83hCP2kpj1seuVahL5_GKAdhBV7YzzvP3bSFz74b8X11x0cRe58KeMN2IfT9eyv8Af8Tm7Lx-Eer2J4_T8bf09qzdrYvSwabNbxFoaXN0BwAA)

## Source code:

- dapp connection code: [GCScript](Native%20asset%20minter%20and%20burner.gcscript)
- frontend + dapp connection code : [HTML5 dapp](Native%20asset%20minter%20and%20burner.html)

Dapp code was autogenerated by [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground)

## GCScript code (dapp connection):
```json
{
  "type": "script",
  "returnURLPattern": "http://localhost:3000/demo/api/dapp",
  "run": {
    "dependencies": {
      "type": "script",
      "run": {
        "issuer": {
          "type": "deriveKeys",
          "keys": [
            {
              "name": "issuer",
              "kind": "spend",
              "accountIndex": 0,
              "addressIndex": 0
            }
          ]
        },
        "mintingPolicy": {
          "type": "nativeScript",
          "script": {
            "pubKeyHashHex": "{get('cache.dependencies.issuer.0.pubKeyHashHex')}"
          }
        }
      }
    },
    "buildMint": {
      "type": "buildTx",
      "name": "built-mint",
      "tx": {
        "mints": [
          {
            "policyId": "{get('cache.dependencies.mintingPolicy.scriptHashHex')}",
            "assets": [
              {
                "assetName": "WillDieToken",
                "quantity": "100"
              },
              {
                "assetName": "WillNotDieToken",
                "quantity": "1"
              }
            ]
          }
        ],
        "witnesses": {
          "nativeScripts": {
            "mintingPolicyScript": "{get('cache.dependencies.mintingPolicy.scriptHex')}"
          }
        }
      }
    },
    "signMint": {
      "type": "signTxs",
      "namePattern": "signed-mint",
      "txs": [
        "{get('cache.buildMint.txHex')}"
      ],
      "detailedPermissions": false
    },
    "submitMint": {
      "type": "submitTxs",
      "namePattern": "submitted-mint",
      "txs": "{get('cache.signMint')}"
    },
    "buildBurn": {
      "type": "buildTx",
      "name": "built-burn",
      "tx": {
        "mints": [
          {
            "policyId": "{get('cache.dependencies.mintingPolicy.scriptHashHex')}",
            "assets": [
              {
                "assetName": "WillDieToken",
                "quantity": "-100"
              }
            ]
          }
        ],
        "witnesses": {
          "nativeScripts": {
            "mintingPolicyScript": "{get('cache.dependencies.mintingPolicy.scriptHex')}"
          }
        }
      }
    },
    "signBurn": {
      "type": "signTxs",
      "namePattern": "signed-burn",
      "txs": [
        "{get('cache.buildBurn.txHex')}"
      ],
      "detailedPermissions": false
    },
    "submitBurn": {
      "type": "submitTxs",
      "namePattern": "submitted-burn",
      "txs": "{get('cache.signBurn')}"
    },
    "finally": {
      "type": "script",
      "exportAs": "MintAndBurn",
      "run": {
        "issuer": {
          "type": "macro",
          "run": "{get('cache.dependencies.issuer.0.pubKeyHashHex')}"
        },
        "policyId": {
          "type": "macro",
          "run": "{get('cache.dependencies.mintingPolicy.scriptHashHex')}"
        },
        "policyScript": {
          "type": "macro",
          "run": "{get('cache.dependencies.mintingPolicy.scriptHex')}"
        },
        "mintTx": {
          "type": "macro",
          "run": "{get('cache.submitMint.0')}"
        },
        "burnTx": {
          "type": "macro",
          "run": "{get('cache.submitBurn.0')}"
        }
      }
    }
  }
}
```

## Run standalone QR dapp connection: 

You can use [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground) in `QR URL Transport` mode to capture results

[![QR URL Transport](Native%20asset%20minter%20and%20burner.png)](https://beta-wallet.gamechanger.finance/api/2/run/1-H4sIAAAAAAAAA81UTW_bMAz9L7p0A1zbw26-ddihRbciWDPsMPSgWGwiVJY8id4cBP7vI_0V56NLMwzofLFFUo-PT8_aCFyXIDIRcq9LFJHwgJW3X798mklE8JZyK8QySxLjcmlWLmD2Pk3TREHhElnqRMmy5I0V1W6EghKsAptrCLw-wO_KdAgV-EmBAq9_wi2sAxU98Sv7vhFWFpzsqymhrWI07kFLmeeusnhDDWuRpRRQykMIQ6B5aCJRaIvaLmfO6Hw96WglUsf7gVjPkPJltSAe1zKsrhlFbJaAby5yma8gno4Xd7TiNN7ZcfG2EQ09kVhU2qjP1H7StY3Na2rYz8YBvGSSFMOaS3nRzV-2pG_Un1jszBd3Y0yokCghQI_Xft51jb9pYz5qmLsnsFT1o5KEg6SQeJemookOq-8cPrNBkNIPkfil0ZL83clP9Q3DWCPRXvdz55rKG_TS7qnLoXkdenW3FuY4qK3KrMZO5_GoYqz7JjSPApTagJqBL-iwtbO08VGaANy-WhQa9wm0waMU2gzusdghMQzUjtjb50Pl7Wn7LLjqf7HPZeufVzLEnl4nDDHqdtwQDHauIfYJvMAQUxYHhmC83hCP2kpj1seuVahL5_GKAdhBV7YzzvP3bSFz74b8X11x0cRe58KeMN2IfT9eyv8Af8Tm7Lx-Eer2J4_T8bf09qzdrYvSwabNbxFoaXN0BwAA)

## Resources
- [GCScript documentation](https://beta-wallet.gamechanger.finance/doc/api/v2/api.html)
- [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground)
- [Youtube Tutorials](https://www.youtube.com/@gamechanger.finance)
- [Discord Support](https://discord.gg/vpbfyRaDKG)
- [Twitter News](https://twitter.com/GameChangerOk)
- [Website](https://gamechanger.finance)

## License
MIT 
    