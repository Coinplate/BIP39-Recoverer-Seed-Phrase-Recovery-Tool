# Seed Savior-Iteration

A fork of tool for recovering BIP39 seed phrases.

Getting any of the following errors...

Trezor: Recovery failed. Error details: Mnemonic is not valid
<br>Ledger: Invalid recovery phrase
<br>Invalid mnemonic...

Any of the above errors can really ruin your day, especially if you have lost/damanged/reset your hardware wallet. The aim of this tool is to be a 1st (and hopefully only) step required to recover your 24 word seed. It is quick and easy to understand and will work on any system with nothing more than a browser. If you don't have success with this tool, then you can try BTCRecover, (https://github.com/gurnec/btcrecover) though it hasn't been updated in some time.

The tool is based on the bip39 project by Ian Coleman https://github.com/iancoleman/bip39 and is a minimally modifed version of the Seed Savior Tool found here: https://github.com/KZen-networks/mnemonic-recovery It's possible the changes I added will be merged into the main project, but I have forked it in the mean time while I add some interface tweaks to make it a bit more n00b friendly, useful for more coins as-is and with examples of extra coins that are easy to extend as required. I can also look at adding the 1st public address for other coins to the UI as long as they are already included in the bitcoinjs library, though you will notice that all the extra address generation makes this tool take far longer to test addresses than the original seed-savior. (Though still quick enough to be useful in my opinion)

For more context and background of the original tool, please see the blog post https://medium.com/kzen-networks/the-wallet-seed-saviors-2cad8ae542f3 

<b><i>If this was helpful, feel free to send me a tip:</b></i>
<br>BTC: 37hiiSB1Poj6Shs8WawPS2HjT2jzHkFSQi
<br>LTC: MRWnUcsyofisVp5GvX7nxMog5caneycKZ6
<br>ETH: 0x14b2E26021d0Ce8E2cE6a2Eb6E2690714bB18E17
<br>VTC: vtc1qxauv20r2ux2vttrjmm9eylshl508q04uju936n
<br>ZEN: znUihTHfwm5UJS1ywo911mdNEzd9WY9vBP7

## Online Version

https://3rditeration.github.io/mnemonic-recovery/src/index.html

## Standalone offline version

Download `mnemonic-standalone.html`

Open the file in a browser by double clicking it.

This can be compiled from source using the command `python compile.py`

## Usage

Enter your seed phrase into the 'BIP39 Phrase' field. If a word is missing or unknown, please type "?" instead and the tool will find all relevant options. If a word is wrong, the tool will try to suggest the closest option.

The tool will suggest all relevant options for the missing word and the derived public addresses for Bitcoin anmd Ethereum. To find out if one of the suggested addresses is actually the right one, you can click on the suggested address  tocheck the address' transaction history on a block explorer.

## Demo

In this demo we enter "phrase brief ceiling dream rack install fault insane panic surround glory ? library brother hill sauce access child notice picnic dinner panda purity poem"

The tool suggests several options for the missing word and the relevant one will be "asset". We can verify that by clicking on the link of the dervied Ethereum address ("0x2dfF20b40504f99c6314ac30e8DF5c02dd8058e7" listed in the "BIP44 ETH Address" column) and checking the address has transaction history.

![Demo](/src/img/seed%20demo%20annotated.gif "Demo")


## Making changes

Please do not make modifications to `mnemonic-standalone.html`, since they will
be overwritten by `compile.py`.

Make changes in `src/*`.

Changes are applied during release using the command `python compile.py`, so
please do not commit changes to `mnemonic.html`



# License

This Seed Svior tool is released under the terms of the MIT license. See LICENSE for
more information or see https://opensource.org/licenses/MIT.
