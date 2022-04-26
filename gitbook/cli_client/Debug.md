# Debug
A tool for simple debugging.

## Available Commands

|Name   |Description   |
| :------------ | :------------ |
|[addr](#daddr)   |Convert an address between hex and bech32    |
|[pubkey](#dpubkey)   |Decode a pubkey from proto JSON    |
|[raw-bytes](#drawbytes)   |Convert raw bytes output (eg. [10 21 13 127]) to hex    |

### stafihubd debug addr<span id='daddr'></span>
```
stafihubd debug addr stafi1m3uxpmweefjdj9kcy3aserws5ggkjsyv50rsh4
```
returns
```
Address: [220 120 96 237 217 202 100 217 22 216 36 123 12 141 208 162 17 105 64 140]
Address (hex): DC7860EDD9CA64D916D8247B0C8DD0A21169408C
Bech32 Acc: stafi1m3uxpmweefjdj9kcy3aserws5ggkjsyv50rsh4
Bech32 Val: stafivaloper1m3uxpmweefjdj9kcy3aserws5ggkjsyvv5uecu
```

### stafihubd debug pubkey<span id='dpubkey'></span>
```
stafihubd debug pubkey '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"AurroA7jvfPd1AadmmOvWM2rJSwipXfRf8yD6pLbA2DJ"}'
```
returns
```
Address: 620B7D22188F8BDBA267DAF89A857081092A6A6C
PubKey Hex: 02eaeba00ee3bdf3ddd4069d9a63af58cdab252c22a577d17fcc83ea92db0360c9
```

### stafihubd debug raw-bytes<span id='drawbytes'></span>
```
stafihubd debug raw-bytes '[72 101 108 108 111 44 32 112 108 97 121 103 114 111 117 110 100]'
```
returns
```
48656C6C6F2C20706C617967726F756E64
```