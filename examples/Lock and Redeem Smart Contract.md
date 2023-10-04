
# Cardano Example Dapp

## **Lock and Redeem Smart Contract**

    Coin locking transaction ( 5 eUTXOs) and later an unlocking one of previously locked coin, in 2 secuential transactions. Using deployed smart contract.


## Try it online: 

-  Visit [HTML5 Dapp](https://raw.githubusercontent.com/GameChangerFinance/gamechanger.wallet/main/examples/Lock%20and%20Redeem%20Smart%20Contract.html)
-  Run [Standalone URL dapp connection](https://beta-wallet.gamechanger.finance/api/2/run/1-H4sIAAAAAAAAA81YS2_bOBD-K4IubQGvQ5HUK7ds99Big7ZoEqDAolgMyWEiVJa8EtV1Gvi_71CSY8dxGifIwvXJIuf1DedF3oSucCWGx-Fprb8FUJngMxrEWXA2g8YFb-vKNaBdOAkNtrop5q6oKyJ_WxdVUBJPUV0GRFK1REVbwesgDvDi_MvH9k0vrgSHDf0LumpFXlcY1DaYN_i9qLu2vO4FoQk0CZ0EJJgHLeoOK1dAuSm9nQYXrRdhcF7W18TS9mbq0cwp2emu5x7PYCx9N-i6prr4fPoJHJnijb9ybn58dERaobyqW3csGGNHBmf1EcyLIwPzuWfsiPaGcM-xMljpAlv_fU_-QOYhbO4bcEC736Hs6POvm9CDo3WeMP_zDgXXzWglAsZ4ClreLr6D9oo2lLEIdBhKcx5HVsYABlQcKZNbyyODKktybiCBNMY4jnNlYiKATDMAHotwOblVK_gutYIZybbVGmUxtpxpnSbGcJ5jJo3IMGG51akSNpY8EjbVhttU8oynKtEQcSHSXAmebKqVO9HKRDC9rRZ1nGCE0uQZiCzKWW6sSqSNUqkVqFSAUVGcpNoKC4KL1KoUJJfcSGOtTDfVJnKX2iSC7B5arTBKU8Y9BNQpQysUZ1nC81yijrTNMibJmMQmPJZKMBGZmEskL5jM5nxTbbbTyamhs9tWmyeIRqtcgTCJSWPJVMo15HSYqKUWOst0znnKBY8Yj7kVschyliQebKaicPl1OQlbB9_wbUMZ26fKg-EXgmECJKCMFY9szKzBJM3jRCSxtjaXRslIaZYB15ywSyYM_Rcy9Ep8it0WgrWKedm5rj1b5cGYELQ__HuHCx8AKYVA5L3COZd5ToQlVJe37H9_Jw9uKzkxpsF2M5tUV5RmtTwJK5j1ObiLaUJgTdPb4RN3sM97fTDo5hLd61ca9BVON1N7ekfYtN1ke_VmGY7O_tSpP_F6H3F3j8aLWC490h6Kr7bb8M4Xa2SnQ6k8_-IL2sJT1p2bd67tSwms_LMnmtE1A4wxNG_W4fgIkr6yTdn0lr7HQm5uW3TDIdW_42lfwv3XvC4Lff3e9GHng7An_DAAG1b-6YC84q73Uetza_Te5DDQo8NAj34B6Pww0PkvAF0cBrr4BaDLw0CXm9C_TsK6HzZ7rfqKmgZ-pIVZ8QOpuocfPvYOCtvistqqpn7pfLHqE-uxz6-j-c0r68uqL6Z3bLotzVO3GMv-Vz_4OihKNJ-wmRVtO5hkoWzRq-_UrHDbBvSLO03od9yWFXeMWAEaPd_bdNHPzj9rGBer6XqjZRTVbccgPMPc8SDc8awnxGV8jDAffE9ni57Hxp_HJp7HJn10NWixofjD9zvclKQcM6CRL7fKyIwp5ApsJGlWounVWAm5TrIcaE9pGo8hy2IaDEFmKc1XTGz6kXT9W7iKknK4QAyDz3pQGlS3LzanjPPVngI89co55Ic-xv4PL3g30DWt7WbYvDTizTIHT5lmxhxr-isvNpsp7Fm8_Q5n7806gW_8wjnRLI9Z2BfoQ8KIXgBGdHgY_AVg8MPDEC8AQxwehnwBGHRxpAvq8m4Pr8v-MQhK_3h0hiXq8THp9OTs9OSPdT-_1-4e6ejD09JPevog8Kld_b4Ze_T1u7bc6-yDzNG3tqigLK93vSrhYl437qQd74InlRne5R5-cJqBburV9iNnPOp_6Ga_p6idsTc4eFv40FBeRME6uB9_NniOno0BmhR4d50v9hK5a-QgCUNAPEXGOlpXUvzvP-M2SoirFQAA)

## Source code:

- dapp connection code: [GCScript](Lock%20and%20Redeem%20Smart%20Contract.gcscript)
- frontend + dapp connection code : [HTML5 dapp](Lock%20and%20Redeem%20Smart%20Contract.html)

Dapp code was autogenerated by [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground)

## GCScript code (dapp connection):
```json
{
  "title": "Lock and Redeem Smart Contract",
  "description": "Coin locking transaction ( 5 eUTXOs) and later an unlocking one of previously locked coin, in 2 secuential transactions. Using deployed smart contract.",
  "type": "script",
  "returnURLPattern": "http://localhost:3000/demo/api/dapp",
  "run": {
    "dependencies": {
      "type": "script",
      "run": {
        "locks": {
          "type": "data",
          "value": [
            {
              "coin": "2600000",
              "datum": "1a0027ac40",
              "datumHash": "bdfeadeebc2251f45aadab51bd9ff21deb8692da6a75e5559bd5daba8c0aa253"
            },
            {
              "coin": "3200000",
              "datum": "1a0030d400",
              "datumHash": "dbfe5f20cc76dd229e84d38e609fc7b3f54213f7cd2f742827b6ca123379b326"
            },
            {
              "coin": "4600000",
              "datum": "1a004630c0",
              "datumHash": "ec56e1e4d98a381909dfb64f174cbab73adb1567cf3fa3237fb7a4242d4dff47"
            },
            {
              "coin": "6400000",
              "datum": "1a0061a800",
              "datumHash": "cbe177026ca1ec70ef3b20862994ec1cf88049096f6254b3031d524ef54d8f92"
            },
            {
              "coin": "8200000",
              "datum": "1a007d1f40",
              "datumHash": "96eedcb9ba3d6d7540b72ca9a6aec4c3c88c922723210252f353890664dff8b1"
            }
          ]
        },
        "stakeCredential": {
          "type": "data",
          "value": "ad03a4ae45b21f50fde67956365cff94db41bc08a2c2862403d8a234"
        },
        "smartContract": {
          "type": "plutusScript",
          "script": {
            "scriptHex": "4746010000222499",
            "lang": "plutus_v2"
          }
        },
        "smartContractAddress": {
          "type": "buildAddress",
          "name": "smartContractAddress",
          "addr": {
            "spendScriptHashHex": "{get('cache.dependencies.smartContract.scriptHashHex')}",
            "stakePubKeyHashHex": "{get('cache.dependencies.stakeCredential')}"
          }
        }
      }
    },
    "buildLock": {
      "type": "buildTx",
      "name": "LockingTX",
      "tx": {
        "outputs": [
          {
            "address": "{get('cache.dependencies.smartContractAddress')}",
            "datum": {
              "datumHashHex": "{get('cache.dependencies.locks.0.datumHash')}"
            },
            "assets": {
              "toBeLocked": {
                "policyId": "ada",
                "assetName": "ada",
                "quantity": "{get('cache.dependencies.locks.0.coin')}"
              }
            }
          },
          {
            "address": "{get('cache.dependencies.smartContractAddress')}",
            "datum": {
              "datumHashHex": "{get('cache.dependencies.locks.1.datumHash')}"
            },
            "assets": {
              "toBeLocked": {
                "policyId": "ada",
                "assetName": "ada",
                "quantity": "{get('cache.dependencies.locks.1.coin')}"
              }
            }
          },
          {
            "address": "{get('cache.dependencies.smartContractAddress')}",
            "datum": {
              "datumHashHex": "{get('cache.dependencies.locks.2.datumHash')}"
            },
            "assets": {
              "toBeLocked": {
                "policyId": "ada",
                "assetName": "ada",
                "quantity": "{get('cache.dependencies.locks.2.coin')}"
              }
            }
          },
          {
            "address": "{get('cache.dependencies.smartContractAddress')}",
            "datum": {
              "datumHashHex": "{get('cache.dependencies.locks.3.datumHash')}"
            },
            "assets": {
              "toBeLocked": {
                "policyId": "ada",
                "assetName": "ada",
                "quantity": "{get('cache.dependencies.locks.3.coin')}"
              }
            }
          },
          {
            "address": "{get('cache.dependencies.smartContractAddress')}",
            "datum": {
              "datumHashHex": "{get('cache.dependencies.locks.4.datumHash')}"
            },
            "assets": {
              "toBeLocked": {
                "policyId": "ada",
                "assetName": "ada",
                "quantity": "{get('cache.dependencies.locks.4.coin')}"
              }
            }
          }
        ],
        "options": {
          "changeOptimizer": "NO"
        }
      }
    },
    "signLock": {
      "type": "signTxs",
      "namePattern": "signed-lock",
      "txs": [
        "{get('cache.buildLock.txHex')}"
      ],
      "detailedPermissions": false
    },
    "submitLock": {
      "type": "submitTxs",
      "namePattern": "submitted-lock",
      "txs": "{get('cache.signLock')}"
    },
    "buildUnlock": {
      "type": "buildTx",
      "name": "UnlockingTX",
      "tx": {
        "inputs": [
          {
            "txHash": "{get('cache.buildLock.txHash')}",
            "index": 0
          },
          {
            "txHash": "{get('cache.buildLock.txHash')}",
            "index": 1
          },
          {
            "txHash": "{get('cache.buildLock.txHash')}",
            "index": 2
          },
          {
            "txHash": "{get('cache.buildLock.txHash')}",
            "index": 3
          },
          {
            "txHash": "{get('cache.buildLock.txHash')}",
            "index": 4
          }
        ],
        "referenceInputs": [
          {
            "txHash": "672e8af629fbd480be2baf14ff9046df4a9c689ad48bc84da88531da48721f03",
            "index": 0
          }
        ],
        "witnesses": {
          "plutus": {
            "scripts": [
              {
                "scriptHashHex": "{get('cache.dependencies.smartContract.scriptHashHex')}",
                "lang": "{get('cache.dependencies.smartContract.lang')}",
                "input": {
                  "txHash": "672e8af629fbd480be2baf14ff9046df4a9c689ad48bc84da88531da48721f03",
                  "index": 0
                }
              }
            ],
            "consumers": [
              {
                "scriptHashHex": "{get('cache.dependencies.smartContract.scriptHashHex')}",
                "datum": {
                  "dataHex": "{get('cache.dependencies.locks.0.datum')}"
                },
                "redeemer": {
                  "type": "spend",
                  "itemIdPattern": "{itemType}:0"
                }
              },
              {
                "scriptHashHex": "{get('cache.dependencies.smartContract.scriptHashHex')}",
                "datum": {
                  "dataHex": "{get('cache.dependencies.locks.1.datum')}"
                },
                "redeemer": {
                  "type": "spend",
                  "itemIdPattern": "{itemType}:1"
                }
              },
              {
                "scriptHashHex": "{get('cache.dependencies.smartContract.scriptHashHex')}",
                "datum": {
                  "dataHex": "{get('cache.dependencies.locks.2.datum')}"
                },
                "redeemer": {
                  "type": "spend",
                  "itemIdPattern": "{itemType}:2"
                }
              },
              {
                "scriptHashHex": "{get('cache.dependencies.smartContract.scriptHashHex')}",
                "datum": {
                  "dataHex": "{get('cache.dependencies.locks.3.datum')}"
                },
                "redeemer": {
                  "type": "spend",
                  "itemIdPattern": "{itemType}:3"
                }
              },
              {
                "scriptHashHex": "{get('cache.dependencies.smartContract.scriptHashHex')}",
                "datum": {
                  "dataHex": "{get('cache.dependencies.locks.4.datum')}"
                },
                "redeemer": {
                  "type": "spend",
                  "itemIdPattern": "{itemType}:4"
                }
              }
            ]
          }
        },
        "options": {
          "collateralCoinSelection": "LASLAD"
        }
      }
    },
    "signUnlock": {
      "type": "signTxs",
      "namePattern": "signed-unlock",
      "txs": [
        "{get('cache.buildUnlock.txHex')}"
      ],
      "detailedPermissions": false
    },
    "submitUnlock": {
      "type": "submitTxs",
      "namePattern": "submitted-unlock",
      "txs": "{get('cache.signUnlock')}"
    },
    "finally": {
      "type": "script",
      "exportAs": "LockAndRedeem",
      "run": {
        "locks": {
          "type": "macro",
          "run": "{get('cache.dependencies.locks')}"
        },
        "smartContract": {
          "type": "macro",
          "run": "{get('cache.dependencies.smartContract.scriptHex')}"
        },
        "smartContractHash": {
          "type": "macro",
          "run": "{get('cache.dependencies.smartContract.scriptHashHex')}"
        },
        "smartContractAddress": {
          "type": "macro",
          "run": "{get('cache.dependencies.smartContractAddress')}"
        },
        "lockTx": {
          "type": "macro",
          "run": "{get('cache.buildLock.txHash')}"
        },
        "unlockTx": {
          "type": "macro",
          "run": "{get('cache.buildUnlock.txHash')}"
        }
      }
    }
  }
}
```

## Run standalone QR dapp connection: 

You can use [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground) in `QR URL Transport` mode to capture results

[![QR URL Transport](Lock%20and%20Redeem%20Smart%20Contract.png)](https://beta-wallet.gamechanger.finance/api/2/run/1-H4sIAAAAAAAAA81YS2_bOBD-K4IubQGvQ5HUK7ds99Big7ZoEqDAolgMyWEiVJa8EtV1Gvi_71CSY8dxGifIwvXJIuf1DedF3oSucCWGx-Fprb8FUJngMxrEWXA2g8YFb-vKNaBdOAkNtrop5q6oKyJ_WxdVUBJPUV0GRFK1REVbwesgDvDi_MvH9k0vrgSHDf0LumpFXlcY1DaYN_i9qLu2vO4FoQk0CZ0EJJgHLeoOK1dAuSm9nQYXrRdhcF7W18TS9mbq0cwp2emu5x7PYCx9N-i6prr4fPoJHJnijb9ybn58dERaobyqW3csGGNHBmf1EcyLIwPzuWfsiPaGcM-xMljpAlv_fU_-QOYhbO4bcEC736Hs6POvm9CDo3WeMP_zDgXXzWglAsZ4ClreLr6D9oo2lLEIdBhKcx5HVsYABlQcKZNbyyODKktybiCBNMY4jnNlYiKATDMAHotwOblVK_gutYIZybbVGmUxtpxpnSbGcJ5jJo3IMGG51akSNpY8EjbVhttU8oynKtEQcSHSXAmebKqVO9HKRDC9rRZ1nGCE0uQZiCzKWW6sSqSNUqkVqFSAUVGcpNoKC4KL1KoUJJfcSGOtTDfVJnKX2iSC7B5arTBKU8Y9BNQpQysUZ1nC81yijrTNMibJmMQmPJZKMBGZmEskL5jM5nxTbbbTyamhs9tWmyeIRqtcgTCJSWPJVMo15HSYqKUWOst0znnKBY8Yj7kVschyliQebKaicPl1OQlbB9_wbUMZ26fKg-EXgmECJKCMFY9szKzBJM3jRCSxtjaXRslIaZYB15ywSyYM_Rcy9Ep8it0WgrWKedm5rj1b5cGYELQ__HuHCx8AKYVA5L3COZd5ToQlVJe37H9_Jw9uKzkxpsF2M5tUV5RmtTwJK5j1ObiLaUJgTdPb4RN3sM97fTDo5hLd61ca9BVON1N7ekfYtN1ke_VmGY7O_tSpP_F6H3F3j8aLWC490h6Kr7bb8M4Xa2SnQ6k8_-IL2sJT1p2bd67tSwms_LMnmtE1A4wxNG_W4fgIkr6yTdn0lr7HQm5uW3TDIdW_42lfwv3XvC4Lff3e9GHng7An_DAAG1b-6YC84q73Uetza_Te5DDQo8NAj34B6Pww0PkvAF0cBrr4BaDLw0CXm9C_TsK6HzZ7rfqKmgZ-pIVZ8QOpuocfPvYOCtvistqqpn7pfLHqE-uxz6-j-c0r68uqL6Z3bLotzVO3GMv-Vz_4OihKNJ-wmRVtO5hkoWzRq-_UrHDbBvSLO03od9yWFXeMWAEaPd_bdNHPzj9rGBer6XqjZRTVbccgPMPc8SDc8awnxGV8jDAffE9ni57Hxp_HJp7HJn10NWixofjD9zvclKQcM6CRL7fKyIwp5ApsJGlWounVWAm5TrIcaE9pGo8hy2IaDEFmKc1XTGz6kXT9W7iKknK4QAyDz3pQGlS3LzanjPPVngI89co55Ic-xv4PL3g30DWt7WbYvDTizTIHT5lmxhxr-isvNpsp7Fm8_Q5n7806gW_8wjnRLI9Z2BfoQ8KIXgBGdHgY_AVg8MPDEC8AQxwehnwBGHRxpAvq8m4Pr8v-MQhK_3h0hiXq8THp9OTs9OSPdT-_1-4e6ejD09JPevog8Kld_b4Ze_T1u7bc6-yDzNG3tqigLK93vSrhYl437qQd74InlRne5R5-cJqBburV9iNnPOp_6Ga_p6idsTc4eFv40FBeRME6uB9_NniOno0BmhR4d50v9hK5a-QgCUNAPEXGOlpXUvzvP-M2SoirFQAA)

## Resources
- [GCScript documentation](https://beta-wallet.gamechanger.finance/doc/api/v2/api.html)
- [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground)
- [Youtube Tutorials](https://www.youtube.com/@gamechanger.finance)
- [Discord Support](https://discord.gg/vpbfyRaDKG)
- [Twitter News](https://twitter.com/GameChangerOk)
- [Website](https://gamechanger.finance)

## License
MIT 
    