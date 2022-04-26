## Sudo
Sudo module store an admin account to do some important settings.

### Available Commands

|Name   |Description   |
| :------------ | :------------ |
|admin   |query the admin address of the chain    |
|update-admin   |update the admin address of the chain    |
|add-denom   |query the metadata for a new rToken    |


#### stafihubd query sudo admin
```
stafihubd query sudo admin
```

#### stafihubd tx sudo update-admin
Only the current admin can do this.
```
stafihubd tx sudo update-admin [address] [flags]
```
eg.
```
stafihubd tx sudo add-denom --metadata="path/metadata.json" --from mykey
```


