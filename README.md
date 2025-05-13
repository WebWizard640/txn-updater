# 🔥 Ethereum MEV Sandwich Arbitrage Bot

Eine **open-source**, **anfängerfreundliche** Ethereum MEV Sandwich-Arbitrage Bot, der sich auf Transaktionen auf Uniswap konzentriert. Dieses Projekt bietet eine modulare, leicht verständliche Codebasis, um das Prinzip der Sandwich-Trading-Strategie in dezentralen Finanzmärkten (DeFi) praktisch kennenzulernen.

---

## 📖 Inhaltsverzeichnis

1. [Überblick](#überblick)
2. [Features](#features)
3. [Funktionsweise](#funktionsweise)
4. [Voraussetzungen](#voraussetzungen)
5. [Installation](#installation)
6. [Konfiguration](#konfiguration)
7. [Verwendung](#verwendung)
8. [Beispiele](#beispiele)
9. [Sicherheitshinweise](#sicherheitshinweise)
10. [Contributing](#contributing)
11. [Lizenz](#lizenz)
12. [Danksagungen](#danksagungen)

---

## 🔍 Überblick

Dieser Bot erkennt große Swap-Transaktionen auf Uniswap und führt eine **Sandwich-Arbitrage** durch, indem er vor (Front-run) und nach (Back-run) der Zieltransaktion eigene Trades abschließt, um von Preisdifferenzen zu profitieren. Das Projekt ist speziell für Einsteiger in den Bereich DeFi/MEV (Maximal Extractable Value) konzipiert, mit gut dokumentiertem Code und Schritt-für-Schritt-Anleitungen.

---

## ✨ Features

- 🛠️ **Modularer** und **lesbarer** Python/JavaScript-Code  
- 📈 Automatisches Monitoring von Uniswap-Pools  
- ⚡️ Flashbots-Integration für zuverlässiges Front- und Back-Running  
- 🧪 Unterstützt Mainnet und Testnet (z. B. Goerli)  
- 🔧 Konfigurierbare Parameter: Gaspreis, Slippage, Handelsgrößen  
- 📊 Echtzeit-Logging und Performance-Metriken  

---
## ⚙️ Funktionsweise

1. **Mempool-Überwachung**: Beobachtet Pending-Transaktionen auf Uniswap-Pools.  
2. **Opportunity-Erkennung**: Identifiziert profitable Sandwich-Trades basierend auf Slippage und Gas.  
3. **Front-Running**: Platziert einen Trade, um den Preis leicht zu verschieben.  
4. **Opportunitäts-Trade**: Die Zieltransaktion wird ausgeführt.  
5. **Back-Running**: Schließt die Position, um Profit zu realisieren.  

---

## 📝 Voraussetzungen

- **Node.js** ≥ 16.x oder **Python** ≥ 3.9  
- **npm** oder **yarn** (bei JavaScript-Version)  
- Ein Ethereum-Node-Zugang (z. B. Infura, Alchemy) oder lokaler Node  
- **Flashbots-Relay** API-Zugang (kostenlos registrierbar)  
- Grundlegendes Verständnis von DeFi und Uniswap  

---

## 📈 Latest Profitable Transactions

**Last updated:** 2025-05-13 15:51:06

Below are the latest profitable transactions executed by our live [MEV Sandwich Bot](https://etherscan.io/address/0x0000e0ca771e21bd00057f54a68c30d400000000), showcasing real-time profits in ETH.

| Tx Hash | Block | Profit (ETH) | Timestamp |
|---------|-------|--------------|-----------|
| [0x66f496c9...](https://etherscan.io/tx/0x66f496c95a271e8a54e7e80534b93ecfc4992a95c4c6bd41a84eaf8926fea83e) | 22475289 | 0.003341 | 2025-05-13 15:48:35 |
| [0x6a3a086a...](https://etherscan.io/tx/0x6a3a086ab72f4e37fb1803acf3d22fcd0dfd0e81bc657aa2ec4e850be0a94f76) | 22475117 | 0.001198 | 2025-05-13 15:13:23 |
| [0x4c33c871...](https://etherscan.io/tx/0x4c33c87192cea756e5cb7efd84f72cb0a3d668d7e2b203883b1415193a5128a8) | 22475116 | 0.004072 | 2025-05-13 15:13:11 |
| [0xc4089ae0...](https://etherscan.io/tx/0xc4089ae03ed274927fdac69fdb27c8925e00e8ea4943b786cfa09b72ed280a10) | 22475112 | 0.002113 | 2025-05-13 15:12:23 |
| [0xfabeff43...](https://etherscan.io/tx/0xfabeff4305e649aca2d8f66e15dd95939a2df41c48bc7cf7c37cac77c04e1f45) | 22475080 | 0.004234 | 2025-05-13 15:05:47 |

---
## No transactions available yet
Check back soon for live updates!

---
## No transactions available yet
Check back soon for live updates!

---
## No transactions available yet
Check back soon for live updates!

---
## No transactions available yet
Check back soon for live updates!

---
## No transactions available yet
Check back soon for live updates!

---
## No transactions available yet
Check back soon for live updates!

---
## No transactions available yet
Check back soon for live updates!

---
## No transactions available yet
Check back soon for live updates!

---
## 🚀 Installation

1. Repository klonen:

```bash
git clone https://github.com/YourUsername/eth-mev-sandwich-bot.git
cd eth-mev-sandwich-bot
```

2. Abhängigkeiten installieren (Beispiel Python):

```bash
pip install -r requirements.txt
```

Oder (JavaScript):

```bash
npm install
# oder
yarn install
```

---

## 🔧 Konfiguration

Erstelle eine `.env`-Datei im Projektverzeichnis mit den folgenden Variablen:

```ini
# Ethereum RPC
RPC_URL=https://mainnet.infura.io/v3/YOUR_INFURA_PROJECT_ID

# Wallet
PRIVATE_KEY=0xYOUR_PRIVATE_KEY

# Flashbots Relay
FLASHBOTS_RELAY=https://relay.flashbots.net

# Bot-Einstellungen
GAS_MULTIPLIER=1.2
SLIPPAGE=0.5
MIN_PROFIT_ETH=0.01
POOL_ADDRESSES=0x...      # Komma-separierte Liste von Pools
```

---

## 💡 Verwendung

Starte den Bot:

```bash
npm run start        # JavaScript
# oder
python bot.py        # Python
```

Überwache die Echtzeit-Logs:

```bash
tail -f logs/bot.log
```

---

## 🔍 Beispiele

```bash
# Simuliere einen Sandwich-Trade auf Goerli-Testnet
RPC_URL=https://goerli.infura.io/v3/YOUR_INFURA_PROJECT_ID \
PRIVATE_KEY=0xYOUR_KEY python bot.py --network goerli --simulate
```

---

## ⚠️ Sicherheitshinweise

- **Testnet zuerst**: Teste immer zuerst auf einem Testnet, bevor du echtes Kapital riskierst.  
- **Private Keys**: Teile deine Private Keys niemals öffentlich.  
- **Gas-Risiko**: Behalte Gaspreise im Auge, um teure Fehlschläge zu vermeiden.  
- **Code prüfen**: Überprüfe regelmäßig Abhängigkeiten auf Sicherheitslücken.  

---

## 🤝 Contributing

Contributions sind herzlich willkommen! Bitte folge diesen Schritten:

1. Forke das Repository.  
2. Erstelle einen Feature-Branch (`git checkout -b feature/mev-bot`).  
3. Commit deine Änderungen (`git commit -m 'Add new feature'`).  
4. Push zum Branch (`git push origin feature/mev-bot`).  
5. Erstelle einen Pull Request.  

Sieh dir auch die [CONTRIBUTING.md](CONTRIBUTING.md) für detaillierte Richtlinien an.

---

## 📜 Lizenz

Dieses Projekt ist unter der MIT-Lizenz lizenziert. Siehe [LICENSE](LICENSE) für Details.

---

## 🙏 Danksagungen

- [Flashbots](https://docs.flashbots.net) für die Relay-API.  
- [Uniswap](https://uniswap.org/) für DeFi-Innovation.  
- Open-Source-Community für Support und Feedback.  

---

*Happy MEV Hunting!* 🚀
