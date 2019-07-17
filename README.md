### pybitcointools
---
https://github.com/primal100/pybitcointools
https://github.com/vbuterin/pybitcointools

```py
from cryptos import *
c = Bitcoin(testnet=True)
priv = sha256('a big long brainwallet password')
priv
pub = c.privtopub(priv)
pub
addr = c.pubtoaddr(pub)
addr
inputs = c.unspent(addr)
inputs
tx = c.mktx(inputs,outs)
tx
tx2 = c.sign(tx,0,priv)
tx2
tx3 = c.sign(tx2,1,priv)
tx3
tx4 = c.serialize(tx)
tx4
c.push(tx4)


from cryptos import *
dash = Dash(testnet=True)
dash.send("xxx", "xxx", 'network': 'DASHTEST')

from cryptos import *
dash = Dash()
tx = dash.preparesignedtx(priv, "xxx", 'network': 'DASHTEST')

from cryptos import *
dash = Dash()
tx = dash.preparesignedtx(priv, "xxx", 98000000-20000, fee=20000)
tx
dash.pushtx(tx)

from cryptos import *
crypto = BitcoinCash(testnet=True)
tx = crypto.preparesignedtx("xxx", "xxx", 'network': 'DASHTEST')
tx
crypto.pushtx(tx)

from cryptos import *
c = Litecoin(testnet=True)
priv = sha256('a big long brainwallet password')
priv
addr = c.privtop2w(priv)
addr
inputs = c.unspent(addr)
inputs
inputs[0]['segwit']=True
inputs
tx = c.mktx(inputs,outs)
tx
tx2 = c.mktx(inputs,outs)
tx
tx2 = c.sign(tx,0,priv)
tx2
tx3 = serialize(tx)
tx3
c.pushtx(tx3)


from cryptos import *
l = Litecoin()
l.send("<privkey>", "xxx", 23486583, fee=20000, change_addr="xxx", segwit=True)

from cryptos import *
c = Bitcoin()
c.send('<privkey>', 'xxx', 88036480, addr="xxx")

from cryptos import *
c = Bitcoin()
c.send('<privkey>', 'xxx', 88036480, addr="xxx")

from cryptos import *
coin = Bitcoin(testnet=True)
publickeys = ['xxx', 'xxx', 'xxx']
script, address = coin.mk_multsig+address(publickeys, 2)
script
address
tx = coin.preparetx(address, "xxx", 1100000, 50000)
for i in range(0, len(tx['ins'])):
  sig1 = coin.multisign(tx, i, script, "xxx")
  sig3 = coin.multisign(tx, i, script, "xxx")
  tx = apply_multisignatures(tx, i, script, sig1, sig3)
tx
coin.pushtx(tx)


from cryptos imports *
priv = sha256('a big long brainwallet password')
b = Bitcoin()
b.privtoaddr(priv)
b = Bitcoin(testnet=True)
b.privtoaddr(priv)
l = Litecoin()
l.privtoaddr(priv)
l = Litecoin(testnet=True)
l.privtoaddr(priv)
c = Bitcoinaddr(priv)
c.privtoaddr(priv)
d = Dash()
d.privtoaddr(priv)
d = Dash(testnet=True)
d.privtoaddr(priv)
d = Doge()
d.privtoaddr(priv)
bg = Bitcoingold()
bg.privtoaddr(priv)
bg = BitcoionGold(legacy=true)
bg.pribtoaddr(priv)
bg = BitcoinGold(testnet=True)
bg.privtoaddr(priv)


from cryptos import *
words = entropy_to_words(os.urandom(16))
words
keystore.bip39_is_checksum_valid(words)
coin = Bitcoin()
wallet = coin.wallet(words)
wallet.keystore.root_derivation
wallet.keystore.xprv
wallet.keystore.xpub
addr1 = wallet.new_receiving_address()
addr1
wallet.privkey(addr1)
addr2 = wallet.new_change_address()
addr2
wallet.privkey(addr2)
addr3
priv3 = wallet.privkey(addr3)
priv3
assert coin.privtoaddr(priv3) == addr3

from cryptos import *
words = 'practice display use aisle armor salon glue okay sphere rather belt mansion'
coin = Dash()
wallet = coin.wallet(words)
wallet.keystore.root_derivation
wallet.keystore.xprv
wallet.keystore.xpub
addr1 = wallet.new_receiving_address()
addr1
wallet.privkey(addr1)
addr2 = wallet.new_change_address()
addr2
wallet.privkey(addr2)
addr3 = wallet.new_change_address()
addr3
priv3 = wallet.privkey(addr3)
priv3
assert coin.privtoaddr(priv3) == addr3


from cryptos import *
words = entropy_to_words(os.urandom(20))
words
coin = Bitcoin()
wallet = coin.p2wpkh_p2sh_wallet(words)
wallet.keystore.xprv
wallet.keystore.xpub
addr1 = wallet.new_receiving_address()
addr1
wallet.privkey(addr1)
addr2 = wallet.new_change_address()
addr2
wallet.privkey(addr2)
addr3 = wallet.new_change_address()
addr3
wallet.privkey(addr3)

from cryptos import *
words = 'jealous silver churn hedgehog border physical market parent hungry design cage lab drill clay attack'
coin = Bitcoin()
wallet = coin.p2wpkh_wallet(words)
wallet.keystore.root_derivation
wallet.keystore.xprv
wallet.keystore.xpub
addr1 = wallet.new_receiving_address()
addr1
wallet.privkey(addr1)
addr2 = wallet.new_change_address()
addr2
wallet.privkey(addr2)
addr3 = wallet.new_change_address()
addr3
wallet.privkey(addr3)


from cryptos import *
seed_words = 'bitter grass shiver impose acquire brush forget axis eager alone wine silver'
wallet = Bitcoin().electrum_wallet(seed_words)
wallet.keystore.xtype
wallet.keystore.root_derivation
wallet.keystore.xprv
wallet.keystore.xpub
addr1 = wallet.new_receiving_address()
addr1
wallet.privkey(addr1)
addr2 = wallet.new_change_address()
addr2
wallet.privkey(addr2)
addr3 = wallet.new_change_address()
addr3
wallet.privkey(addr3)


from cryptos import *
coin = Dash()
xpub = 'xxx'
wallet = coin.watch_wallet(xpub)
wallet.is_watching_only
wallet.new_receiving_address()
wallet.new_change_address()


import os
from cryptos import *
words = entropy_to_words(os.urandom(6))
words
seed = mnemonic_to_seed(words)
seed
electrum_privkey(seed, 0)
electrum_privkey(seed, 300, 0)
electrum_privkey(seed, 0, 1)











```

```
```

```
```


