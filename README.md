# Instalasi Otomatis: Solana + Rust + Bitz

Salin dan jalankan script berikut ini untuk menginstal Rust, Solana CLI, dan Bitz dalam satu langkah:

```bash
apt update && apt install sudo -y
````
```bash
sudo apt install curl -y
```
# Instal Rust
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
. "$HOME/.cargo/env"
```
# Instal Solana CLI
```bash
curl --proto '=https' --tlsv1.2 -sSfL https://solana-install.solana.workers.dev | bash
```
# Tambahkan Solana ke PATH (untuk pengguna zsh)
```bash
echo 'export PATH="$HOME/.local/share/solana/install/active_release/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```
# Generate keypair Solana baru
```bash
solana-keygen new
```
# Set RPC URL ke Eclipse by Helius
```bash
solana config set --url https://eclipse.helius-rpc.com
```
# Instal Bitz via Cargo
```bash
cargo install bitz
```
