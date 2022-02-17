## Sudo
Sudo module store an admin account to do some important settings.

### Available Commands

|Name   |Description   |
| :------------ | :------------ |
|admin   |query the admin address of the chain    |
|update-admin   |update the admin address of the chain    |
|add-denom   |query the metadata for a new rToken    |


#### stafid query sudo admin
```
stafid query sudo admin
```

#### stafid tx sudo update-admin
Only the current admin can do this.
```
stafid tx sudo update-admin [address] [flags]
```
eg.
```
stafid tx sudo add-denom --metadata="path/metadata.json" --from mykey
```


