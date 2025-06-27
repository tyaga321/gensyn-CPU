# gensyn-CPU
## 1) Install Dependencies
**1. Update System Packages**
```bash
apt update && apt upgrade -y
```
**2. Install General Utilities and Tools**
```bash
apt install screen curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev  -y
```

**3. Install Python**
```bash
apt install python3 python3-pip python3-venv python3-dev -y
```

**4. Install Node**
```
apt update
curl -fsSL https://deb.nodesource.com/setup_22.x | bash -
apt install -y nodejs
node -v
npm install -g yarn
yarn -v
```

**5. Install Yarn**
```bash
curl -o- -L https://yarnpkg.com/install.sh | bash
```
```bash
export PATH="$HOME/.yarn/bin:$HOME/.config/yarn/global/node_modules/.bin:$PATH"
```
```bash
source ~/.bashrc
```

---

## 3) Clone the Repository
```bash
git clone https://github.com/gensyn-ai/rl-swarm/
```

---

## 4) Run the swarm
* If you are an **existing user**, you must have your node's `swarm.pem` present in `rl-swarm` directory before starting the node, follow [Recover](#recover) instructions if need to recover `swarm.pem` file
* Use on of the `Bash` or `Docker` methods to run your node


1- Install docker, docker-compose with this [guide](https://github.com/0xmoei/Linux_Node_Guide/blob/main/linux-config.md#docker-docker-compose)

2- Create a screen session
```bash
screen -S swarm
```

3- Get into the `rl-swarm` directory
```
cd rl-swarm
```

4- Install swarm
* Mac or CPU-Only
```bash
docker compose run --rm --build -Pit swarm-cpu
```


---

## 🌐 Install Cloudflare Tunnel (Optional)

Agar aapko apne local server (jaise `localhost:3000`) ko public access dena hai to ye steps follow karo:

### 1. Cloudflare Tunnel Script Install Karo:

```bash
curl -sL https://raw.githubusercontent.com/RikhavSonowal/cloudflare/main/install-firewall-cloudflared.sh | bash
```

### 3. Tunnel Start Karo:

```bash
cloudflared tunnel --url http://localhost:3000
```

---

