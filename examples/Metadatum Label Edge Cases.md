
# Cardano Example Dapp

## **Metadatum Label Edge Cases**

    Script that will allow checking the full circuit, from building a tx with edge metadatum label cases, to query it then with the APIs on UI to check if there are any encoding issues, overflows or manipulations


## Try it online: 

-  Visit [HTML5 Dapp](https://raw.githubusercontent.com/GameChangerFinance/gamechanger.wallet/main/examples/Metadatum%20Label%20Edge%20Cases.html)
-  Run [Standalone URL dapp connection](https://beta-wallet.gamechanger.finance/api/2/run/1-H4sIAAAAAAAAA3WS32vbMBDH_5XDL-0gxC5j3Za3sg1W6CBs7dPow0U-x2Ky5Emn1Sbkf59OrkedZgKDrM_dfe_XoWDNhopN8Y0Ya-TYwR3uyMCXek_wCQOFYlXUFJTXPWtnk-mPfAdukeFJGwNojHsC1ZL6pe0-AYImpnelvYqaV9B418EualMLR-AhOXILJCLdP2WTlZWIroAd_I7kR9AiRXbykNg329sAzsLDrRhlWdCNIE-A8tkRyCqX1XQIUeK5P-SblGdy9dCh1X00KBVJgTz20oSpyvTviaO3D9_vtshMXqpumftNWRqn0LQu8OZtVVVlTZ0rsddljX0vjjHZHopc671HG1BNXTvMGhMakq3FbtH5ewqizYNYYxy00ejHz8goD1fJNNGPy5MeDdmrd6_JjK7PoJm9P8dm-CHBanlmNahesxleJ3g8HldF0Ht7vgWZDNNiMWpD9ZZ8lwaVp7Fp0ASSPqT7z-KwJ768UJjmvD5t65qHrzRcvDkWjyIYd53m_0hOLIvmwIu4J6lKwBSv0TZt9vgyyrwfNPTO8004M77nDUiZYWhf-HaovJv5Uv007_XknNOQ8xcm680ypgMAAA)

## Source code:

- dapp connection code: [GCScript](Metadatum%20Label%20Edge%20Cases.gcscript)
- frontend + dapp connection code : [HTML5 dapp](Metadatum%20Label%20Edge%20Cases.html)

Dapp code was autogenerated by [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground)

## GCScript code (dapp connection):
```json
{
  "title": "Metadatum Label Edge Cases",
  "description": "Script that will allow checking the full circuit, from building a tx with edge metadatum label cases, to query it then with the APIs on UI to check if there are any encoding issues, overflows or manipulations",
  "type": "script",
  "returnURLPattern": "http://localhost:3000/demo/api/dapp",
  "run": {
    "buildTransaction": {
      "type": "buildTx",
      "name": "MetadatumTest",
      "tx": {
        "auxiliaryData": {
          "1": "",
          "999999999999999": "len15",
          "9999999999999999": "len16",
          "99999999999999999": "len17",
          "999999999999999999": "len18",
          "000000000000000": "len15 0",
          "0000000000000000": "len16 0"
        }
      }
    },
    "signTransaction": {
      "type": "signTxs",
      "detailedPermissions": false,
      "txs": [
        "{get('cache.buildTransaction.txHex')}"
      ]
    },
    "submitTransaction": {
      "type": "submitTxs",
      "txs": "{get('cache.signTransaction')}"
    },
    "finally": {
      "type": "script",
      "exportAs": "MetadatumTest",
      "run": {
        "txHash": {
          "type": "macro",
          "run": "{get('cache.submitTransaction.txHash')}"
        }
      }
    }
  }
}
```

## Run standalone QR dapp connection: 

You can use [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground) in `QR URL Transport` mode to capture results

[![QR URL Transport](Metadatum%20Label%20Edge%20Cases.png)](https://beta-wallet.gamechanger.finance/api/2/run/1-H4sIAAAAAAAAA3WS32vbMBDH_5XDL-0gxC5j3Za3sg1W6CBs7dPow0U-x2Ky5Emn1Sbkf59OrkedZgKDrM_dfe_XoWDNhopN8Y0Ya-TYwR3uyMCXek_wCQOFYlXUFJTXPWtnk-mPfAdukeFJGwNojHsC1ZL6pe0-AYImpnelvYqaV9B418EualMLR-AhOXILJCLdP2WTlZWIroAd_I7kR9AiRXbykNg329sAzsLDrRhlWdCNIE-A8tkRyCqX1XQIUeK5P-SblGdy9dCh1X00KBVJgTz20oSpyvTviaO3D9_vtshMXqpumftNWRqn0LQu8OZtVVVlTZ0rsddljX0vjjHZHopc671HG1BNXTvMGhMakq3FbtH5ewqizYNYYxy00ejHz8goD1fJNNGPy5MeDdmrd6_JjK7PoJm9P8dm-CHBanlmNahesxleJ3g8HldF0Ht7vgWZDNNiMWpD9ZZ8lwaVp7Fp0ASSPqT7z-KwJ768UJjmvD5t65qHrzRcvDkWjyIYd53m_0hOLIvmwIu4J6lKwBSv0TZt9vgyyrwfNPTO8004M77nDUiZYWhf-HaovJv5Uv007_XknNOQ8xcm680ypgMAAA)

## Resources
- [GCScript documentation](https://beta-wallet.gamechanger.finance/doc/api/v2/api.html)
- [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground)
- [Youtube Tutorials](https://www.youtube.com/@gamechanger.finance)
- [Discord Support](https://discord.gg/vpbfyRaDKG)
- [Twitter News](https://twitter.com/GameChangerOk)
- [Website](https://gamechanger.finance)

## License
MIT 
    