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

**Last updated:** 2025-05-02 11:26:58

Below are the latest profitable transactions executed by our live [MEV Sandwich Bot](https://etherscan.io/address/0x0000e0ca771e21bd00057f54a68c30d400000000), showcasing real-time profits in ETH.

| Tx Hash | Block | Profit (ETH) | Timestamp |
|---------|-------|--------------|-----------|
| [0x92154545...](https://etherscan.io/tx/0x921545457c9a5153593a9a0287523dc3015d9289246fc00d7e841f16bb5a3d11) | 22395708 | 0.003736 | 2025-05-02 11:04:59 |
| [0xb8b2c44d...](https://etherscan.io/tx/0xb8b2c44dd105400cd65080c405bf5a24000ed7f77a7d8689954b034ffb2970d7) | 22395680 | 0.002874 | 2025-05-02 10:59:11 |
| [0x152a61b4...](https://etherscan.io/tx/0x152a61b4086e44aa5894278a41bfecf439ae929439421c1de3bbf6d194cf20f5) | 22395661 | 0.004815 | 2025-05-02 10:55:23 |
| [0x46974eb4...](https://etherscan.io/tx/0x46974eb4e292081b9ee14b61da2b562da47a0fbb7c4836ab4bf5323d62c8f9c0) | 22395610 | 0.001492 | 2025-05-02 10:44:59 |
| [0xaf88a726...](https://etherscan.io/tx/0xaf88a72631c39ffa810a05510c4353a449f23e997a0ad056a8ee62065f217cb5) | 22395571 | 0.004173 | 2025-05-02 10:36:47 |

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
