
# Cardano Example Dapp

## **Stake Withdrawal**

    Script that withdraw stake rewards from custom child derivation in a transaction


## Try it online: 

-  Visit [HTML5 Dapp](https://raw.githubusercontent.com/GameChangerFinance/gamechanger.wallet/main/examples/Stake%20Withdrawal.html)
-  Run [Standalone URL dapp connection](https://beta-wallet.gamechanger.finance/api/2/run/1-H4sIAAAAAAAAA41STW-CQBD9L3uxTQjQ9MbNm017MNqm55EdZSMs22UoGMN_784qCNV-eCDy5s2b92Y4CjoYFImoUqsMiUBYpNrqt9XLEojQalfLiEwSRXmZQp6VFSWPcRxHEosyAqMiCcZwY-24RyHRoJaoU4UVv1_pn2h7PIzLEq36xGcGg6G2Jtgzxv81FMwbIMdSWrIwI-4V0rSsNT252a1IYgdIabGqeqALxBIOBWqaKo7AiyZH-I9m51RX2ICV81NlFGlTq3yAg37clH1S5CYfY1lvnI8FVNmC9cVxh3Q3SyHNMBzvNeQNhf0uQjNum913ovPGqP3tAN7eu6JMWmi-235tL457jseoZWpzhiD3E-b8gH4BP7ueZGefgfioQZMidxDxEPvf2XyldvqGO4bPRq5X5AKHk1ihZ_mNOMV6Uyi6pekLXjUH98mLZOuCYSAaUCQSsjX-PG_sczSOI2yVhjw_3LoBtqa0NOdtrZXe5TjYGu7jtNxBR82Mn6t_unCd_XfQfQFhycVQ4wMAAA)

## Source code:

- dapp connection code: [GCScript](Stake%20Withdrawal.gcscript)
- frontend + dapp connection code : [HTML5 dapp](Stake%20Withdrawal.html)

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
        "keys": {
          "type": "deriveKeys",
          "keys": {
            "StakeKey": {
              "name": "StakeKey",
              "kind": "stake",
              "accountIndex": 0,
              "addressIndex": 0
            },
            "PaymentKey": {
              "name": "PaymentKey",
              "kind": "spend",
              "accountIndex": 0,
              "addressIndex": 0
            }
          }
        },
        "RewardAddress": {
          "type": "buildAddress",
          "name": "RewardAddress",
          "addr": {
            "stakePubKeyHashHex": "{get('cache.dependencies.keys.StakeKey.pubKeyHashHex')}"
          }
        }
      }
    },
    "txs": {
      "type": "script",
      "run": {
        "buildWithdraw": {
          "type": "buildTx",
          "name": "WithdrawTx",
          "tx": {
            "withdrawals": {
              "A": {
                "address": "{get('cache.dependencies.RewardAddress')}",
                "quantity": "1000000"
              }
            }
          }
        },
        "signWithdraw": {
          "type": "signTx",
          "txHex": "{get('cache.txs.buildWithdraw.txHex')}"
        },
        "submitWithdraw": {
          "type": "submitTx",
          "later": false,
          "wait": true,
          "txHex": "{get('cache.txs.signWithdraw.txHex')}"
        }
      }
    },
    "finally": {
      "type": "script",
      "exportAs": "SingleWithdraw",
      "run": {
        "txHash": {
          "type": "run",
          "run": "{get('cache.txs.signWithdraw.txHash')}"
        }
      }
    }
  }
}
```

## Run standalone QR dapp connection: 

You can use [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground) in `QR URL Transport` mode to capture results

[![QR URL Transport](Stake%20Withdrawal.png)](https://beta-wallet.gamechanger.finance/api/2/run/1-H4sIAAAAAAAAA41STW-CQBD9L3uxTQjQ9MbNm017MNqm55EdZSMs22UoGMN_784qCNV-eCDy5s2b92Y4CjoYFImoUqsMiUBYpNrqt9XLEojQalfLiEwSRXmZQp6VFSWPcRxHEosyAqMiCcZwY-24RyHRoJaoU4UVv1_pn2h7PIzLEq36xGcGg6G2Jtgzxv81FMwbIMdSWrIwI-4V0rSsNT252a1IYgdIabGqeqALxBIOBWqaKo7AiyZH-I9m51RX2ICV81NlFGlTq3yAg37clH1S5CYfY1lvnI8FVNmC9cVxh3Q3SyHNMBzvNeQNhf0uQjNum913ovPGqP3tAN7eu6JMWmi-235tL457jseoZWpzhiD3E-b8gH4BP7ueZGefgfioQZMidxDxEPvf2XyldvqGO4bPRq5X5AKHk1ihZ_mNOMV6Uyi6pekLXjUH98mLZOuCYSAaUCQSsjX-PG_sczSOI2yVhjw_3LoBtqa0NOdtrZXe5TjYGu7jtNxBR82Mn6t_unCd_XfQfQFhycVQ4wMAAA)

## Resources
- [GCScript documentation](https://beta-wallet.gamechanger.finance/doc/api/v2/api.html)
- [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground)
- [Youtube Tutorials](https://www.youtube.com/@gamechanger.finance)
- [Discord Support](https://discord.gg/vpbfyRaDKG)
- [Twitter News](https://twitter.com/GameChangerOk)
- [Website](https://gamechanger.finance)

## License
MIT 
    