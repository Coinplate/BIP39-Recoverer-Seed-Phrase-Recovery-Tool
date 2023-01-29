# BIP39 Recoverer: seed phrase recovery tool

Getting any of the following errors...

Trezor: Recovery failed. Error details: Mnemonic is not valid
<br>Ledger: Invalid recovery phrase
<br>Invalid mnemonic...

Any of the above errors can really ruin your day, especially if you have lost/damanged/reset your hardware wallet. The aim of this tool is to be a 1st (and hopefully only) step required to recover your 24 word seed. It is quick and easy to understand and will work on any system with nothing more than a browser. If you don't have success with this tool, then you can try BTCRecover, (https://github.com/gurnec/btcrecover) though it hasn't been updated in some time.

## How to use
Enter your 12 or 24 words BIP39 seed phrase. Use the tool OFFLINE for recovery.
If one of your words is incorrect, the tool will try to suggest similar, correct words. Try them out.
If you are unsure about one of the words, replace it with ? . The tool will calculate all possible words that work. Check them in your wallet or check if any of the calculated addressess is yours.
To calculate the checksum (last word - either 12th or 24th), put ? instead of last word. The tool will calculate all correct checksum words - 8 potenial words for 24th and 128 words for 12th.

example: enter a 12 or 24 words seed phrase: "phrase brief ceiling dream rack install fault insane panic surround glory ? library brother hill sauce access child notice picnic dinner panda purity poem"

Note: 12 word seed phrases will take significantly longer to process due to the large number of possibilities for a unknown word.

Enter your seed phrase into the 'BIP39 Phrase' field. If a word is missing or unknown, please type "?" instead and the tool will find all relevant options. If a word is wrong, the tool will try to suggest the closest option.

The tool will suggest all relevant options for the missing word and the derived public addresses for Bitcoin anmd Ethereum. To find out if one of the suggested addresses is actually the right one, you can click on the suggested address  tocheck the address' transaction history on a block explorer.

**If you found this tool useful, you can tip us or buy a metal crypto wallet from [our store](https://getcoinplate.com/).**

- BTC: bc1q4tq9mz6dz78qgxvrlfvpg2yp0hxn4wmtfq6rmm
- ETH: 0x77fa426AB714995a34D20A4d61fDcE2AB829c54F
- LTC: ltc1qk5s74tx445hzjgxm5xtyp2wth7f0q969leefyx
- XLM: GDXZ7YE2QZN2FT4CDY2QREQ6ZV3A76CJQIYZZQ4CTX6XU7PBO3JOKTKS
- ADA: addr1q88l806507plwz0gl3e44mw78fkjn4jekk4st8tk2yaca7u09dknhhq52pqmg70v2h45g3spnr0jxd9yz4w9a5v2j0kq0sg74f

**See the tool in action - online version -  [BIP39 Recoverer](https://getcoinplate.com/bip39-recoverer-seed-phrase-recovery-tool/)**

## Security notes & offline use

You can use this tool 100% offline. For security it is preferable to use offline fresh system install or system on live usb. Download `BIP39_Recoverer_standalone_offline.html` file and open it in a browser.


**It's important to have a proper [seed phrase storage](https://getcoinplate.com/blog/the-best-crypto-seed-phrase-storage-the-ultimate-guide/).**


## Check out our other tools:
**[BIP39 Seed Phrase Generator - online/offline](https://getcoinplate.com/bip39-seed-phrase-mnemonics-generator-offline-online-tool/)**



## Making changes

Please do not make modifications to `mnemonic-standalone.html`, since they will
be overwritten by `compile.py`.

Make changes in `src/*`.

Changes are applied during release using the command `python compile.py`, so
please do not commit changes to `mnemonic.html`

Source code: You can see the full source code in standalone, offline html file. Alternatively you can check the individual css and js files in the online version folder, where the direct copy of website version is stored. This is free and opensource tool.



<details><summary> License (click to expand) </summary
<p>The MIT License (MIT) Copyright (c) 2022 Coinplate</p>

<p>Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.</p>

</details>

The tool is based on the bip39 project by Ian Coleman https://github.com/iancoleman/bip39 and is a minimally modifed version of the Seed Savior Tool found here: https://github.com/KZen-networks/mnemonic-recovery. Changes involves mostly making the tool responsive to display size and small improvements in UX.
