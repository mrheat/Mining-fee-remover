# Mining-fee-remover
Remove mining fees from Claymore's miner - mine into your own wallet instead. This currently only works on Linux/EthOS.

# How?

This program catches login packets sent to a ethereum stratum pool and modifies the target wallet address.

# TODO:

- Add config file
- Add support for custom worker names. This doesn't work now as modifying packet lenght forces pool to close connection.
- Windows version?

# Requirements

- Python 2.7
- python-nfqueue
- python-scapy

# installation

Install requrements:

## Ubuntu

```
sudo apt-get install python-nfqueue python-scapy git
```

## EthOS

```
TODO:
```

Clone this repository:
```
git clone git@github.com:tommarek/Mining-fee-remover.git
```

# Configuration

This version of fee remover doesn't support config files so you will need to modify the source code.
You need to change:
- `pool` to the pool you are using
- `port` to the pool connection port
- `eth_wallet` address `0xda3e1e7822589a26e9705E184fC340e0731935eA` to yours (on line 102)
- `password` to your password
and save the modified file.

# Running the program

```
cd Mining-fee-remover
```

and run the program by executing
```
./mining_fee_remover.py
```

If you want the program to run in the background - so you can close the terminal window, run:

```
./mining_fee_remover.py &
```

And then start your miner. Once the miner starts mining the dev fee it should mine to the wallet you've put into the source code.

# Help
If you need any help then let me know and I'll try to help you.

# BTW
I don't encourage you to use this as Claymore deserves all the money he gets from the mining fees for making a great product.
I created this as it was a really interesting thing to do and it might help other people with simillar problems.

# Donations
If you found this useful please consider donating at least a small amount to:
ETH: `0xda3e1e7822589a26e9705E184fC340e0731935eA`
BTC: `3LE91QD9aCoCsM9vF8PXs755Vr7bmnoexQ`



