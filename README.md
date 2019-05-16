# TV Wallet Generator
This tool generates TV wallet file with 15-word seed phrase. The output is exported to 'wallet.dat' which can be used with full node,  as well as a CSV file 'addresses.csv', which contains the list of all generated addresses with seeds, private keys and public keys.


## Usage Sbt

```
$ sbt
sbt:walletgenerator> run --testnet
```

## Usage Sbt Console

```
$ sbt console
scala> WalletGenerator.main(Array("--testnet", "--count", "10"))
```

## Examples

Generate testnet addresses. Output to screen, wallet.dat and addresses.csv (optional).
```
sbt:walletgenerator> run --testnet --count 2
[info] Running WalletGenerator --testnet --count 2
------------------------------------------------------------------------------------------------------------------------------------------------------
IMPORTANT - COPY OR MEMORIZE THE SEED PHRASE BELOW FOR KEY RECOVERY!!!
seed         : endorse clutch flower world cost elder cover proof stem zoo weasel another moment aunt drill
------------------------------------------------------------------------------------------------------------------------------------------------------
address #    : 0
address      : u65smELZtCcUtmg4UbcDssKzcRcPpc5zN1A
public key   : BccMMvANfMWt6JfDCMfCr2GeE5cMKLpuAphAamCnUjbZ
private key  : 29MNEoGhZTa3bHh3NNAEdsq5UL4KuoLy6bF8n9i9LJwe
account seed : 9nKdFGicscZaVD5awKosLzCkGgdCUn18Wuwk8yiWxiA9
------------------------------------------------------------------------------------------------------------------------------------------------------
address #    : 1
address      : u6P1UEQy4ETu4RWjcNbQ9d4tW7cDHRtaAzX
public key   : H1zxPJ8cWqkZTKam1uUHj67xyxnhU1AysvRyuyCa3HSK
private key  : CrFQzVLwruWHM7D73MgBS3nUak76mrAoLT5G7nxNCah2
account seed : 6eEg9BoR7RyaTavoJCiS7etwLfKNi8qZgHchnJiW6jN4
------------------------------------------------------------------------------------------------------------------------------------------------------
```

Generate mainnet addresses. Output to screen, wallet.dat and addresses.csv (optional).
```
sbt:walletgenerator> run --count 2
[info] Running WalletGenerator --count 2
------------------------------------------------------------------------------------------------------------------------------------------------------
IMPORTANT - COPY OR MEMORIZE THE SEED PHRASE BELOW FOR KEY RECOVERY!!!
seed         : grape nominee section ivory faint priority shrug hour neck uncle spend barrel shiver crumble lottery
------------------------------------------------------------------------------------------------------------------------------------------------------
address #    : 0
address      : tv3rtm9hS8G3goTN7N7xJob4UjgxY999C3H
public key   : HdpMUac7zQ1zwxGshJKFVA7eeTDuXDLXdbnP98f8Pfk4
private key  : DScAbwTrDNwFtVJWe5jSZdgrr85wA9YmmpVehH6rponN
account seed : Do5Dhmi48mEigneLSzMVF8b4brTanj3qDGDM5eQykSHH
------------------------------------------------------------------------------------------------------------------------------------------------------
address #    : 1
address      : tv1P9yVGDTPuKZnSNsJTeMUQA946sRWfoz6
public key   : 1owTJQd8E1aBFjvfU5wAR6E6ybtJMFu8YMNHoUF8zzt
private key  : BGoLEdqUbHa97Qd6rAFwza9YKWuitESsWwkyF6mBRWcy
account seed : BZXe51xt17TydFFxHovSEVs7PxrVprGCReHFeBe2ZBaD
------------------------------------------------------------------------------------------------------------------------------------------------------
```

Recover wallet with a seed phrase.
```
sbt:walletgenerator> run --testnet --count 3 --seed "welcome scheme bargain boring enable include slogan announce girl rough mention thought ski script vague"
```

Decrypt and print JSON wallet (with empty password).
```
sbt:walletgenerator> run --decrypt
```