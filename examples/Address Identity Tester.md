
# Cardano Example Dapp

## **Address Identity Tester**

    This demo will test addresses default native scripts or 'Identities', and explore differencies between ways to obtain them


## Try it online: 

-  Visit [HTML5 Dapp](https://raw.githubusercontent.com/GameChangerFinance/gamechanger.wallet/main/examples/Address%20Identity%20Tester.html)
-  Run [Standalone URL dapp connection](https://beta-wallet.gamechanger.finance/api/2/run/1-H4sIAAAAAAAAA9WRMWvDMBCF_8qhxQmE2NAtW0iXQgulpFPpoFjnWlSWjHSua4L_e0-1lYYEOrebT3rv6bvnoyBNBsVGbJXyGALcKbR8NsAeA6EXK6EwlF63pJ1l3b7WARQ2DnptDBCrQE5ejBeV7AyBlaQ_ECZjAOchm4M1hmwF0irAz9Y4j6B0VaFHW_IVHJB6RAu9HAKQA3cgqS1QjQ2j0NBG1imWZ45wnrbhhz_h3zIhCzxS5-3z0_2jJN4mLlATtZs8N66UpnaBNjdFUeRxo1y2OleybaOxY-1R9JrqBwaY0-PRJYMOzkjCnSxrPiffYXo2qhunvtWuQda-48AZL2IuLLpt5RJzHNPn63hikFdvvyGdQ41TzJmgkaV3aQtxZH2qh3ULHhdZGXnXc3a2XI4p5kTzW1zyR8M6QWdzyHXADHyKHkfWxW53nec_T3-u3guuf9HwzHxe8jh-AfOnTzrhAwAA)

## Source code:

- dapp connection code: [GCScript](Address%20Identity%20Tester.gcscript)
- frontend + dapp connection code : [HTML5 dapp](Address%20Identity%20Tester.html)

Dapp code was autogenerated by [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground)

## GCScript code (dapp connection):
```json
{
  "title": "Address Identity Tester",
  "description": "This demo will test addresses default native scripts or 'Identities', and explore differencies between ways to obtain them",
  "type": "script",
  "exportAs": "AddressIdentityDemo",
  "returnURLPattern": "http://localhost:3000/demo/api/dapp",
  "run": {
    "withMainAddress": {
      "type": "script",
      "isolateCache": true,
      "return": {
        "mode": "some",
        "keys": [
          "address",
          "infoIdentity",
          "identity"
        ]
      },
      "run": {
        "address": {
          "type": "getMainAddress"
        },
        "info": {
          "type": "macro",
          "run": "{getAddressInfo(get('cache.address'))}"
        },
        "infoIdentity": {
          "type": "macro",
          "run": "{get('cache.info.identity')}"
        },
        "identity": {
          "type": "getMainIdentity"
        }
      }
    },
    "withCurrentAddress": {
      "type": "script",
      "isolateCache": true,
      "return": {
        "mode": "some",
        "keys": [
          "address",
          "infoIdentity",
          "identity"
        ]
      },
      "run": {
        "address": {
          "type": "getCurrentAddress"
        },
        "info": {
          "type": "macro",
          "run": "{getAddressInfo(get('cache.address'))}"
        },
        "infoIdentity": {
          "type": "macro",
          "run": "{get('cache.info.identity')}"
        },
        "identity": {
          "type": "getCurrentIdentity"
        }
      }
    }
  }
}
```

## Run standalone QR dapp connection: 

You can use [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground) in `QR URL Transport` mode to capture results

[![QR URL Transport](Address%20Identity%20Tester.png)](https://beta-wallet.gamechanger.finance/api/2/run/1-H4sIAAAAAAAAA9WRMWvDMBCF_8qhxQmE2NAtW0iXQgulpFPpoFjnWlSWjHSua4L_e0-1lYYEOrebT3rv6bvnoyBNBsVGbJXyGALcKbR8NsAeA6EXK6EwlF63pJ1l3b7WARQ2DnptDBCrQE5ejBeV7AyBlaQ_ECZjAOchm4M1hmwF0irAz9Y4j6B0VaFHW_IVHJB6RAu9HAKQA3cgqS1QjQ2j0NBG1imWZ45wnrbhhz_h3zIhCzxS5-3z0_2jJN4mLlATtZs8N66UpnaBNjdFUeRxo1y2OleybaOxY-1R9JrqBwaY0-PRJYMOzkjCnSxrPiffYXo2qhunvtWuQda-48AZL2IuLLpt5RJzHNPn63hikFdvvyGdQ41TzJmgkaV3aQtxZH2qh3ULHhdZGXnXc3a2XI4p5kTzW1zyR8M6QWdzyHXADHyKHkfWxW53nec_T3-u3guuf9HwzHxe8jh-AfOnTzrhAwAA)

## Resources
- [GCScript documentation](https://beta-wallet.gamechanger.finance/doc/api/v2/api.html)
- [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground)
- [Youtube Tutorials](https://www.youtube.com/@gamechanger.finance)
- [Discord Support](https://discord.gg/vpbfyRaDKG)
- [Twitter News](https://twitter.com/GameChangerOk)
- [Website](https://gamechanger.finance)

## License
MIT 
    