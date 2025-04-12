# Instalasi Otomatis: Solana + Rust + Bitz

Salin dan jalankan script berikut ini untuk menginstal Rust, Solana CLI, dan Bitz dalam satu langkah:

```bash
# Update sistem dan instal sudo
apt update && apt install sudo -y

# Instal curl
sudo apt install curl -y

# Instal Rust
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
source $HOME/.cargo/env

# Instal Solana CLI
curl --proto '=https' --tlsv1.2 -sSfL https://solana-install.solana.workers.dev | bash

# Tambahkan Solana ke PATH (untuk pengguna zsh)
echo 'export PATH="$HOME/.local/share/solana/install/active_release/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc

# Jika menggunakan bash, gunakan ini:
# echo 'export PATH="$HOME/.local/share/solana/install/active_release/bin:$PATH"' >> ~/.bashrc
# source ~/.bashrc

# Generate keypair Solana baru
solana-keygen new

# Set RPC URL ke Eclipse by Helius
solana config set --url https://eclipse.helius-rpc.com

# Instal Bitz via Cargo
cargo install bitz
