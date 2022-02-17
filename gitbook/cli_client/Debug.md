## Debug
A tool for simple debugging.

### Available Commands

|Name   |Description   |
| :------------ | :------------ |
|addr   |Convert an address between hex and bech32    |
|pubkey   |Decode a ED25519 pubkey from hex, base64, or bech32    |
|raw-bytes   |Convert raw bytes output (eg. [10 21 13 127]) to hex    |

#### stafid debug addr
```
stafid debug addr fis1afnrl54grrvdpx8udn5cldt6enkqp2ndra25rf
```
returns
```
Address: [234 102 63 210 168 24 216 208 152 252 108 233 143 181 122 204 236 0 170 109]
Address (hex): EA663FD2A818D8D098FC6CE98FB57ACCEC00AA6D
Bech32 Acc: fis1afnrl54grrvdpx8udn5cldt6enkqp2ndra25rf
Bech32 Val: fisvaloper1afnrl54grrvdpx8udn5cldt6enkqp2ndu3x3tl
```

#### stafid debug pubkey
The following give the same result:
```
```