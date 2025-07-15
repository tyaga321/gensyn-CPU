
## 📍 Jika sudah menjalankan GENSYN sebelumnya

remove Data

```bash
sudo pkill screen
sudo rm -rf rl-swarm
```

---


### 1. Base Setup Script

```bash
curl -sL https://gist.githubusercontent.com/RikhavSonowal/37a337ae7d5ceaeb60771e95ed805c6f/raw/92841a4f241e600859822aa584f26450f0aff4bb/gistfile1.txt | bash
```

### 2. Screen Session Start

```bash
screen -S gensyn
```

### 3. Node Config File Download karo:

```bash
curl -sL https://raw.githubusercontent.com/RikhavSonowal/gensyn-smooth-/main/grpo-qwen-2.5-0.5b-deepseek-r1.yaml -o rl-swarm/hivemind_exp/configs/mac/grpo-qwen-2.5-0.5b-deepseek-r1.yaml
```

### 4. layout.tsx File Add karo:

```bash
curl -sL https://raw.githubusercontent.com/RikhavSonowal/rl-swarm/main/layout.tsx -o rl-swarm/modal-login/app/layout.tsx
```

### 5. Project Directory

```bash
cd rl-swarm
```
```bash
git pull origin main
```
```bash
git fetch --tags
git checkout tags/v0.5.0 -b v0.5.0
```


### 6. Python Virtual Environment Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
```
* Open -
 ```
nano ~/.zshrc
```

* Paste in the file

```
export PYTORCH_MPS_HIGH_WATERMARK_RATIO=0.0
export PYTORCH_ENABLE_MPS_FALLBACK=1
```
* Reload with

```
  source ~/.zshrc
```

### 7. Node Start

```bash
./run_rl_swarm.sh
```

---

## 🌐 Install Cloudflare Tunnel (Optional)

Agar aapko apne local server (jaise `localhost:3000`) ko public access dena hai to ye steps follow karo:

### 1. Cloudflare Tunnel Script Install

```bash
curl -sL https://raw.githubusercontent.com/RikhavSonowal/cloudflare/main/install-firewall-cloudflared.sh | bash
```

### 3. Tunnel Start

```bash
cloudflared tunnel --url http://localhost:3000
```

---

## ✅ Tips

- `screen` ko detach 
  Press `Ctrl + A` then `D`
  
- Wapas join
  ```bash
  screen -r gensyn
  ```

- Node ko band  
  ```bash
  sudo pkill screen
  ```
  ```bash
  cd rl-swarm
  ```
  ```bash
  rm -rf .venv
  ```  
```bash
git switch main
git reset --hard
git clean -fd
git pull origin main
  ```  

  ```bash
  rm /tmp/gensyn_last_line_status.txt
  ```
