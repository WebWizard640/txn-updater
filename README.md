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

**Last updated:** 2025-05-16 04:55:09

Below are the latest profitable transactions executed by our live [MEV Sandwich Bot](https://etherscan.io/address/0x0000e0ca771e21bd00057f54a68c30d400000000), showcasing real-time profits in ETH.

| Tx Hash | Block | Profit (ETH) | Timestamp |
|---------|-------|--------------|-----------|
| [0x62f48dea...](https://etherscan.io/tx/0x62f48dead65a0d9aa1e9caa458e3ccf99a5058f178ce262584636b928d7a6cb4) | 22493393 | 0.002735 | 2025-05-16 04:54:35 |
| [0x12d0fb2c...](https://etherscan.io/tx/0x12d0fb2c9ea3d97dc5cd3db8c0801572780d19f6b09b85a0e9070bb1e2faa610) | 22493302 | 0.004724 | 2025-05-16 04:36:11 |
| [0x3a9a80f7...](https://etherscan.io/tx/0x3a9a80f7104d0b68dfcad3512952309eda131a11b7da5293c2593618f116ce86) | 22493301 | 0.004348 | 2025-05-16 04:35:59 |
| [0x56d6a0d7...](https://etherscan.io/tx/0x56d6a0d762f1dd5ba550ccb6c96722ba50a53a5b750de43d737a86b3dcf49d49) | 22493300 | 0.002513 | 2025-05-16 04:35:47 |
| [0xf526f975...](https://etherscan.io/tx/0xf526f97530d96e82d61d0cc362f08a2dfacea261d4bbb83e1a424a21bd559a8f) | 22493285 | 0.004516 | 2025-05-16 04:32:47 |

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
