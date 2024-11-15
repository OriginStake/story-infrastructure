# 🌍 Story Protocol Node Distribution

We are building a **global decentralized network** for Story Protocol, starting with `odyssey-0 testnet` and continuing through to mainnet! Distributing nodes across different regions enhances **reliability**, **performance**, and **diversity** of the system. 🎯

<div align="center">
  <img src="https://res.cloudinary.com/ghostdigital/image/upload/v1731514165/story-take-my-energy_dltk9b.png" width="430" alt="Story Protocol Energy" />
</div>

---

## 🛑 Current Situation and Challenges
Currently, many validators are concentrated in Germany (Hetzner/Contabo), leading to several issues:
- ⚠️ **Reduced performance** in distant regions like Asia and Africa
- 📉 **Decreased uptime** in P2P zones outside Europe
- 🔄 **Centralization** risks to system decentralization

## 🎯 Objectives
**Node distribution across at least 4 continents** helps:
- **Increase stability** of the network, especially for distant regions
- **Ensure high uptime** for P2P zones outside Europe
- **Reduce dependency** on a single region to avoid centralization

## 🎯 Implementation Plan
1. **Phase 1 - Expand P2P Network**
   - Build multi-region peer network
   - Minimize missing blocks and increase uptime
   
2. **Phase 2 - Consensus Migration**
   - Encourage validators to move to new providers/regions with current peer list
   - Ensure system decentralization

---

## 🌐 Current Node Distribution

### 🌎 North America
| 💻 Moniker | ️ Node ID | 🌆 City | 🏳️ Country |
|------------|-----------|----------|------------|
| OriginStake | f0fd504ab1d7466958bd3c12c3f6d1607335dbd4@story-newyork-peer.originstake.com:13656 | New York | United States |
| Card3 | 9047a2903df12ea379ea2952a9ab457c2424caa9@34.73.188.109:26656 | South Carolina | United States |



### 🌍 Europe
| 💻 Moniker | 🖥️ Node ID | 🌆 City | 🏳️ Country |
|------------|-----------|----------|------------|
| OriginStake | c5ece7b0a94d90fbdf6bc8781c397a4538db0b58@story-amterdam-peer.originstake.com:13656 | Amsterdam | Netherlands |

### 🌏 Asia
| 💻 Moniker | 🖥️ Node ID | 🌆 City | 🏳️ Country |
|------------|-----------|----------|------------|
| ValidatorVN | d2a6945f138b48d5ad56ac2352958fa75a3576e4@113.189.15.242:55656 | Ho Chi Minh | Vietnam |

### 🌏 Oceania
| 💻 Moniker | 🖥️ Node ID | 🌆 City | 🏳️ Country |
|------------|-----------|----------|------------|
| OriginStake | 5ad4ded1bb0358b7699480ddcabd73ac6d111825@story-sydney-peer.originstake.com:13656 | Sydney | Australia |

### 🌍 Africa
| 💻 Moniker | 🖥️ Node ID | 🌆 City | 🏳️ Country |
|------------|-----------|----------|------------|
| *No nodes yet* | - | - | - |

---

## 📈 Solutions & Community Call to Action

To help make the network **more decentralized and robust**, we invite community participation by:

1. **Deploying nodes** in regions outside Europe
2. **Contributing node configurations** to this repository to strengthen the global network

### 🔄 Accepted Node Types
You can contribute in one of three forms:
- **Dedicated P2P Peer**: Node set up specifically for peering purposes
- **RPC Server**: Dedicated RPC server in your region (not recommended if you set request limits)
- **Regional Pioneer Node**: If you're running the only node in your region (e.g., Africa), your contribution is especially valuable as it helps other validators establish reliable connections in underserved areas

> 💡 Priority is given to nodes from regions with fewer peers to increase network decentralization.

👉 **By contributing, you'll help** Story Protocol become a more sustainable network, serving more geographical regions!

---

## ⚠️ Important Advisory

### Restricted Regions:
- **Germany**
    - Falkenstein
    - Nuremberg
- **Finland**
    - Helsinki

### Restricted Providers:
- **Hetzner** (not decentralized)
- **Contabo** (poor performance)

### Note:
We will **verify IP providers** before merging to ensure clean peers. If you intentionally provide peers from Germany, Hetzner, or Contabo, we will not merge the PR and block your GitHub account for not following these guidelines.

### 📝 Peer Submission Guide

1. **Fork this repository**

2. **Create `peers.json` in `infrastructure/<moniker>` directory**
   ```json
   {
     "moniker": "ValidatorVN",
     "peers": [
       {
         "id": "d2a6945f138b48d5ad56ac2352958fa75a3576e4",
         "address": "113.189.15.242",
         "port": 55656,
         "location": {
           "continent": "Asia",
           "country": "Vietnam"
         }
       }
     ]
   }
   ```

   If you have multiple peers in different regions, add them to the `peers` array:
   ```json
   {
     "moniker": "YourValidator",
     "peers": [
       {
         "id": "peer-id-1",
         "address": "peer1.yourdomain.com",
         "port": 26656,
         "location": {
           "continent": "North America",
           "country": "United States"
         }
       },
       {
         "id": "peer-id-2",
         "address": "peer2.yourdomain.com",
         "port": 26656,
         "location": {
           "continent": "Europe",
           "country": "Netherlands"
         }
       }
     ]
   }
   ```

   > 💡 Accepted regions:
   > - North America
   > - Europe (except Germany)
   > - Asia
   > - Oceania
   > - Africa

3. **Add node information to the corresponding table in README.md based on your node's region**
   ```markdown
   | ValidatorVN | `d2a6945f138b48d5ad56ac2352958fa75a3576e4@113.189.15.242:55656` | Vietnam |
   ```

4. **Create Pull Request**

---

## 📋 Validator Infrastructure Profile (Optional - Coming Soon)

![Validator Infrastructure Profile](https://res.cloudinary.com/ghostdigital/image/upload/v1731512117/ipworld-validator-profile_hbqoln.jpg)

Standardizing information through JSON files not only helps developers integrate easily but is also part of building the Validator Infrastructure Profile for Story Protocol.

> 🚧 **Note**: This infrastructure monitoring system is currently under development and will be publicly available soon. It will serve as a dedicated monitoring platform for validators to track and manage their infrastructure effectively.

If you want to participate more deeply in the ecosystem, please refer to the standardized JSON file templates at:
- [infrastructure/originstake/infra.json](infrastructure/originstake/infra.json)
- [infrastructure/originstake/metadata.json](infrastructure/originstake/metadata.json)

---

💬 **Let's build a strong and globally distributed Story Protocol together!** We appreciate all validator contributions.
