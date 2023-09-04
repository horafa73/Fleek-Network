
<div align="center">
  <h1>Fleek-Network </h1>
</div>

![ghjklz](https://github.com/molla202/Fleek-Network/assets/91562185/83355aab-fdc4-46c8-bbe4-14f2cc19e76b)

* [CoreNode Telegram](https://t.me/corenodechat)<br>
* [CoreNode Twitter](https://twitter.com/corenodeHQ)<br>
* [Fleek Network](https://fleek.network/)<br>
* [Fleek Network Twitter](https://twitter.com/fleek_net)<br>
* [Fleek Network DOC](https://docs.fleek.network/docs)<br>


 ## 💻 Sistem Gereksinimleri
| Bileşenler | Minimum Gereksinimler | 
| ------------ | ------------ |
| ✔️ CPU |	4 |
| ✔️ RAM	| 8 GB |
| ✔️ Storage	| ~GB SSD |

## OTO Kurulum.
```
curl -o fleek.sh -fsSL https://raw.githubusercontent.com/molla202/Fleek-Network/main/fleek.sh && chmod +x fleek.sh && ./fleek.sh
```
### 🏠 Update edelim
```bash
sudo apt update; sudo apt upgrade 
```
### 🤖 Gerekli olanlar
```
sudo apt install screen curl tar wget jq build-essential make clang pkg-config libssl-dev cmake gcc
```
### 🤖 Rustup kuruyoruz
✏️ Not: 1 seçeceksiniz. daha önce kuruluysa kurmanıza gerek yok.
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
```
source ~/.profile
source ~/.cargo/env
```
### 🤖 Protobuf ve sccache Kuruyoruz
```
cargo install sccache
```
```
sudo apt-get install protobuf-compiler
```
### Docker kurulumu (gerekli değil kurmayın )
```bash
sudo apt-get update && sudo apt install jq git && sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin && sudo apt-get install docker-compose-plugin 
```
### 👷 `fleek-network/lightning.git` 'i klonluyoruz.
```
cd $HOME 
git clone https://github.com/fleek-network/lightning.git
cd lightning
```
```
make install
```
* `make install` uzun sürer.
* daha sonra version kontrol edin: 📖`lightning --version`
* version: `lightning 0.1.0`✅
### 🚀 Screen'de node'u çalıştıralım.
```
screen -S light
```
```
cd $HOME
cd lightning 
lightning
```
* Loglar akıyorsa sorun yok.
* Loglar aktıktan sonra CTRL + A + D ile çıkın.
* Screen'e Tekrar Girmek için
```
screen -ar light
```

### ♻️ Key dosyası yedekleme
* Dosyalarınız bu konumda yer alıyor. ~/.lightning/keystore  yedekleyiniz.alttaki kod port değişikliği için deneyeceğiz :D
```
nano ~/.lightning/config.toml
```

