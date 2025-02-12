
# Cardano Example Dapp

## **Generate 10 Gift Wallets**

Generate 10 QR Encrypted Gift Wallets for onboarding students in a class. Files will be downloaded as PNG files for printing or showing on screens


## Try it online: 

-  Visit [HTML5 Dapp](https://gamechangerfinance.github.io/gamechanger.wallet/examples/Generate%2010%20Gift%20Wallets.html)
-  Run [Standalone URL dapp connection](https://beta-wallet.gamechanger.finance/api/2/run/1-H4sIAAAAAAAAA2WQT2vDMAzFv4rwDr2M0V5zG2zroFCy9tDjUGOlM7h2ZiukIeS7T86fha03Wf5Jeu91ituKVKZiEUzF6lGxYZsaW3IUkAk2a9iakuGE1hJHQTSNtPHuH_hxgFdXhLZi0n-moPQBvDt7DNq4C0SuNTnpGwcIhcUYn-DNWIrQGGvhTKB946xHLZswQr7fQjn8p01VMI7THqnjl2-G0oHIInJJIt0qH_g5ir7lqvRDLZI7NZ9P9RRAMwidzPggLF597Vhlm3WyXGJteY9XypGZQnJ-HLdAZ5ymW69-sVzsND7oBc3xGE_-oO_QlyXLhR5DG5zONx7uJnfULhOToc876l2CWrDW1xLepA5MhFU3v_qVDH0HlXGoScan9Oe3pQsWrcpKtJH6vv8BvK46JjkCAAA)

## Source code:

- dapp connection code: [GCScript DSL](Generate%2010%20Gift%20Wallets.gcscript)
- frontend (using @gamechanger-finance/gc): [HTML5 dapp](Generate%2010%20Gift%20Wallets.html)
- frontend (without official library): [Native HTML5 dapp](Generate%2010%20Gift%20Wallets_nolib.html)

Dapp code was autogenerated by [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground)

## GCScript code (dapp connection):
```json
{
  "type": "script",
  "title": "Generate 10 Gift Wallets",
  "description": "Generate 10 QR Encrypted Gift Wallets for onboarding students in a class. Files will be downloaded as PNG files for printing or showing on screens",
  "exportAs": "onboarding",
  "run": {
    "students": {
      "type": "walletGenerator",
      "amount": 10,
      "defaultNamePattern": "Student {index}",
      "defaultPasswordPattern": "PaSsWoRd{index}",
      "defaultDescriptionPattern": "Wallet for Student #{index}",
      "defaultKeyPattern": "student_{index}",
      "defaultHintPattern": "your password is '{password}'",
      "qr": true,
      "download": true,
      "legacy": false
    }
  }
}
```

## Run standalone QR dapp connection: 

You can use [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground) in `QR URL Transport` mode to capture results

[![This GCScript/URL is too large! make it shorter uploading parts to GCFS. Unable to generate QR code](Generate%2010%20Gift%20Wallets.png)](https://gamechangerfinance.github.io/gamechanger.wallet/examples/Generate%2010%20Gift%20Wallets.png)

## Resources
- [How to connect?](https://www.npmjs.com/package/@gamechanger-finance/gc)
- [Docs and examples on Github](https://github.com/GameChangerFinance/gamechanger.wallet/)
- [GCScript documentation](https://beta-wallet.gamechanger.finance/doc/api/v2)
- [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground)
- [Tutorials on Youtube](https://www.youtube.com/@gamechanger.finance)
- [Support on Discord](https://discord.gg/vpbfyRaDKG)
- [News on Twitter](https://twitter.com/GameChangerOk)
- [Website](https://gamechanger.finance)

## License
MIT 
    
