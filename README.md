# mining-monero-on-pi
Mining Monero on Raspberry Pi (Not profitable, but it's fun)

1. Execute the following commands on your raspberry pi terminal (might need 64bit version of RPiOS)
```shell
sudo apt get update
sudo apt install git build-essential cmake libuv1-dev libssl-dev libhwloc-dev
git clone https://github.com/xmrig/xmrig.git
cd xmrig/
mkdir build
cd build
cmake ..
make
```

2. Create Monero Wallet
   * On windows you can download [Monero GUI wallet](https://www.getmonero.org/downloads/)
   * Copy Wallet Address > Account > Click on Copy icon.
3. Execute the following
```shell
./xmrig -o gulf.moneroocean.stream:10128 -u [YOUR_WALLET_ADDRESS] -p pi1
```
Example:
```shell
./xmrig -o gulf.moneroocean.stream:10128 -u 48Mio4s3suvgGkzwgNhSwwDvaCTCFWkXPZqokNBuoj2z531P4iXqt2y1SbLuwFRCsKWm7zGkL5wgc7fqHBACgzXR5V7uFwQ -p pi1
```
Note: 
* Instead of using gulf.moneroocean.stream:10128 you can use any other mining pool
* Check your share [here](https://moneroocean.stream/) by copy and pasting your wallet address.


References:
- [NetworkChuck](https://www.youtube.com/watch?v=hHtGN_JzoP8)