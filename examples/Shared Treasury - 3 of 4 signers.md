
# Cardano Example Dapp

## **Shared Treasury - 3 of 4 signers**

Creates a workspace named 'DAO' with a 'Shared Treasury' address where at least 3 of 4 signer wallets are required for spending and staking operations. A second address on the workspace is caller main address as 'Signer'. To manage the treasury set 'Shared Treasury' address as current. To sign as a member, set 'Signer' address instead. Please customize this code with real public key hashes, you can use 'Share your public key information' example on each member to obtain them. Please use 'saveConfig' function to save this setup on GCFS to avoid losing funds and data


## Try it online: 

-  Visit [HTML5 Dapp](https://gamechangerfinance.github.io/gamechanger.wallet/examples/Shared%20Treasury%20-%203%20of%204%20signers.html)
-  Run [Standalone URL dapp connection](https://beta-wallet.gamechanger.finance/api/2/run/1-H4sIAAAAAAAAA51VS2_bOBD-K4QuuaQBxYdI5ha0hwbd7RZIgB6KIBiRw1iILXlFetMg8H_fofyI89p0ezI1j2_mm49DP1T5fonVaZX82C1zdVzlLs-L4WIGIwZ2OSKk1XjPPjDJhsgUS91Nj2Oi0ICbrG7oKeEjRWZMDNjdMN6mJXhkPSwI4-jT2V9H7K7LM3IePQM-YhDCiCmxuxmOyCCzOXny03LsDuZzzIROISP-veoKRhxGlpbYh66_YdAHljLclvOwxBFKX-mEnbGEfiDnrs7QszzDgy67xHyBH9kCun4fB4manaofnbDLgZw93OCUm3dTSZj_gxEh-NU4Yp8ngEKl2IAtcNHieLxN39TYZ3V9ygjhhCaMP5fDmM8SjfcTDGQYMa9GmvZDtRhCkakfeqzW5FhN1s2YLihqWT634s4HCB-HPnY3BLFaBtLpPOwx53Bf9Dz9sY__vhsNebuMi42ziPkNcsbSQBWm3Om2PBpJ6Kf34tH1feqsMM6kUKIxktJ-f2fSZob7wZL2r9-E9CuqV-ur9fGezhe8p672ep-HwmcicPU2v6nCh41QlE0Fws5Kn-D9sOrzeR_wZ3XKybARb2co1Z_hUZP4Eq9YfwXvkM9XIvkPXuw29g1iL-S6frjF-_X1ftO3zB-2pOgA-Y8y8OpUHldDvJxhwmL-c2r6mpfzctXSOD9Dmn0ujVW1RCdBWd80UohgXPTByqBtHYVUttWN4dJBK4OzNkYbGmEb-ip3dotbv4arfOAREKTgIC0qrxxKEbziIdYtqNbSirQco_Ky1kJ46b1uYn2AK17DtRK01HUw1tW10qbhMboGhfPSaFBSat1yq4PmspYtiqYJyhlz2K98DddoHaPRXoLwvm6M5LV0xsk2erBRg2iN9cJpZQzn3PIgFQphZLVeE_LmGvyeAl5IHSBYDrGJTptaQ4jBoPcyRm-V8pqLSMRQmhZ47UCbtnb2PQW8Ba4tOhcKhjJRGd9y5WnuDkGDiYWakiIa5Fo1UgtHQpn3FIDWg_PBBdm2RgcTsQ1UhH5spP4IS3Pg0lIV7gRvwNLseBPfU8DWKoDTgNE2og4KVUtd8mhIWeKsSXmItVAKI1eiofqRLqSbFFgfbNfZZvP-_4uxeccpb9qnb1N7Xyni5WMyyf004PB1ePl4PPuH2dU4fAi2QGXPJ9_jnk_Yb4UW3y6UHpkrGsW_1sOdZxQIAAA)

## Source code:

- dapp connection code: [GCScript DSL](Shared%20Treasury%20-%203%20of%204%20signers.gcscript)
- frontend (using @gamechanger-finance/gc): [HTML5 dapp](Shared%20Treasury%20-%203%20of%204%20signers.html)
- frontend (without official library): [Native HTML5 dapp](Shared%20Treasury%20-%203%20of%204%20signers_nolib.html)

Dapp code was autogenerated by [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground)

## GCScript code (dapp connection):
```json
{
  "type": "script",
  "title": "Shared Treasury - 3 of 4 signers",
  "description": "Creates a workspace named 'DAO' with a 'Shared Treasury' address where at least 3 of 4 signer wallets are required for spending and staking operations. A second address on the workspace is caller main address as 'Signer'. To manage the treasury set 'Shared Treasury' address as current. To sign as a member, set 'Signer' address instead.",
  "exportAs": "Dao",
  "return": {
    "mode": "none"
  },
  "run": {
    "walletSetup": {
      "type": "loadConfig",
      "updateId": "Dao",
      "layers": [
        {
          "type": "Workspace",
          "items": [
            {
              "namePattern": "dao",
              "titlePattern": "DAO",
              "descriptionPattern": "Wallet settings that creates a shared treasury of at least 3 of 4 signers for spending and staking operations"
            }
          ]
        },
        {
          "type": "Key",
          "workspaceIds": [
            "dao"
          ],
          "items": [
            {
              "namePattern": "spend-member",
              "kind": "spend",
              "accountIndex": 0,
              "addressIndex": 0
            },
            {
              "namePattern": "stake-member",
              "kind": "stake",
              "accountIndex": 0,
              "addressIndex": 0
            }
          ]
        },
        {
          "type": "NativeScript",
          "workspaceIds": [
            "dao"
          ],
          "namePattern": "dao_{key}_script",
          "items": {
            "spend": {
              "atLeast": 3,
              "ofThese": {
                "Member_0": {
                  "pubKeyHashHex": "13e93a48c66322d79fcd83d581f2348b567039ab3d988ff8d6286b3d"
                },
                "Member_1": {
                  "pubKeyHashHex": "4cd0faea320a38e4c49e32dc40df1ba4b8eadb0ef4c31522c3cc56f1"
                },
                "Member_2": {
                  "pubKeyHashHex": "83a5351d7891145760ff96e29c375a43355b085d50313be266d4977d"
                },
                "Member_3": {
                  "pubKeyHashHex": "755ff75c3a2cc16730139793bfca8f5a2b78c29547700080d34e2273"
                }
              }
            },
            "stake": {
              "atLeast": 3,
              "ofThese": {
                "Member_0": {
                  "pubKeyHashHex": "c235dad80af6f95715adfd7ecc3ffc844c502f335e37ba019a57b198"
                },
                "Member_1": {
                  "pubKeyHashHex": "c8a058e99d844c47f47cb04cead9ea5a7ffca8432f7e054635298e47"
                },
                "Member_2": {
                  "pubKeyHashHex": "abca9cd9d3bb75d7febd99dfeb8fba0e0550a038d9e09206a82b706f"
                },
                "Member_3": {
                  "pubKeyHashHex": "814da95aef8621d4e4ba5a0f7c379a5583aaf1244ef04269d3f8ff93"
                }
              }
            }
          }
        },
        {
          "type": "Address",
          "workspaceIds": [
            "dao"
          ],
          "items": [
            {
              "namePattern": "Signer",
              "spendPubKeyName": "spend-member",
              "stakePubKeyName": "stake-member"
            },
            {
              "namePattern": "Shared Treasury",
              "spendNativeScriptName": "dao_spend_script",
              "stakeNativeScriptName": "dao_stake_script"
            }
          ]
        }
      ]
    }
  }
}
```

## Run standalone QR dapp connection: 

You can use [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground) in `QR URL Transport` mode to capture results

[![This GCScript/URL is too large! make it shorter uploading parts to GCFS. Unable to generate QR code](Shared%20Treasury%20-%203%20of%204%20signers.png)](https://gamechangerfinance.github.io/gamechanger.wallet/examples/Shared%20Treasury%20-%203%20of%204%20signers.png)

## Resources
- [How to connect?](https://www.npmjs.com/package/@gamechanger-finance/gc)
- [Github Docs and examples](https://github.com/GameChangerFinance/gamechanger.wallet/)
- [GCScript documentation](https://beta-wallet.gamechanger.finance/doc/api/v2/api.html)
- [Playground IDE in GameChanger Wallet ](https://beta-wallet.gamechanger.finance/playground)
- [Youtube Tutorials](https://www.youtube.com/@gamechanger.finance)
- [Discord Support](https://discord.gg/vpbfyRaDKG)
- [Twitter News](https://twitter.com/GameChangerOk)
- [Website](https://gamechanger.finance)

## License
MIT 
    