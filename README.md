# Instalasi Otomatis: Solana + Rust + Bitz

Salin dan jalankan script berikut ini untuk menginstal Rust, Solana CLI, dan Bitz dalam satu langkah:
```bash
cd $HOME
```
```bash
apt update && apt install sudo -y
````
```bash
sudo apt install curl nano screen -y
```
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
. "$HOME/.cargo/env"
```
```bash
curl --proto '=https' --tlsv1.2 -sSfL https://solana-install.solana.workers.dev | bash
```
```bash
echo 'export PATH="$HOME/.local/share/solana/install/active_release/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
```bash
solana-keygen new
```
```bash
solana config set --url https://bitz-000.eclipserpc.xyz/
```
```bash
cargo install bitz
```
```bash
bitz benchmark 
```
```bash 
bitz collect -c 8
```
