
# Cardano Example Dapp

## **Governance key derivation paths**

Explore Conway Era key derivation


## Try it online: 

-  Visit [HTML5 Dapp](https://gamechangerfinance.github.io/gamechanger.wallet/examples/Governance%20key%20derivation%20paths.html)
-  Run [Standalone URL dapp connection](https://beta-wallet.gamechanger.finance/api/2/run/1-H4sIAAAAAAAAA52OywrCMBBFfyXMulBfBXEntSi4EX9AxnagwTYJyVQt4r87sQriSswiIWfOvcwNuHcECwil144hAdbcRLC2Z_IGTUnqRL2qyOszsrZGOeQ6iFnREBImfnF1jfWkcmsu2KvC41dOEnR11vMyiF4hoxDfSfYGT4t23bHR5Zb6ENlrsWH0hAmcXrPVnlx8DbbRid9Di9ocRBAtbii4TcfzbFLLPc7qdFSn03QE9wTyPLdN9ZEfwC8Ns3fDxvJfBVksiOcB_ZtrvXoBAAA)

## Source code:

- dapp connection code: [GCScript DSL](Governance%20key%20derivation%20paths.gcscript)
- frontend (using @gamechanger-finance/gc): [HTML5 dapp](Governance%20key%20derivation%20paths.html)
- frontend (without official library): [Native HTML5 dapp](Governance%20key%20derivation%20paths_nolib.html)

Dapp code was autogenerated by [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground)

## GCScript code (dapp connection):
```json
{
  "type": "script",
  "title": "Governance key derivation paths",
  "description": "Explore Conway Era key derivation",
  "exportAs": "data",
  "run": {
    "derivePublicKeys": {
      "type": "deriveKeys",
      "keys": {
        "DRep": {
          "name": "DRep_main_key",
          "path": "m/1852h/1815h/0h/3/0"
        },
        "CCCold": {
          "name": "CCCold_main_key",
          "path": "m/1852h/1815h/0h/4/0"
        },
        "CCHot": {
          "name": "CCCold_main_key",
          "path": "m/1852h/1815h/0h/5/0"
        }
      }
    }
  }
}
```

## Run standalone QR dapp connection: 

You can use [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground) in `QR URL Transport` mode to capture results

[![This GCScript/URL is too large! make it shorter uploading parts to GCFS. Unable to generate QR code](Governance%20key%20derivation%20paths.png)](https://gamechangerfinance.github.io/gamechanger.wallet/examples/Governance%20key%20derivation%20paths.png)

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
    
