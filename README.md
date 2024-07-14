
# HyperLane - Arbuzers 🍉

[![works on my machine badge](https://cdn.jsdelivr.net/gh/nikku/works-on-my-machine@v0.4.0/badge.svg)](https://github.com/nikku/works-on-my-machine)


### **Запускать на python 3.10!**

To run code:
```
python3.10 -m venv venv
```
```
source venv/bin/activate
```
```
pip install -r requirements.txt
```
```
python app.py
```


<br />

### **Выводы с биржи**:
Выводы если недостаточно денег на счету, для этого вам нужно:
- иметь баланс на правильной биржи и в правильной нативной монетке для контркетного блокчейна (например: Polygon - Matic)
- добавить api ключи для бирж в setings.json
- и указать True для нужных сетей в withdrawal_networks (setings.json)

*Раскидали монеты по биржам в зависимости от стоимости вывода.

_Если вы не хотите пользовать выводы с бирж и у вас уже есть балансы то ставим везде False в withdrawal_networks (setings.json)_

OKX:

    Polygon
    Base ETH
    Optimism ETH
    Moonbeam

Binance:

    Celo
    Avax
    BNB

### **Настройки setings.json:**
- в OKX + Binance указывает api ключи (игнорируем required_minimum_balance и withdraw_amount)
- h_mekr / h_nft сколько минтить (не работает подсчет транз оставляем как есть, считайте сами транзы примерно и ставьте большие паузы)
- hFT_amount_for_mint_and_bridge - сколько минтить токенов (не нфт а токены hMERK) меркли для бриджа, каждый токе 0.02 стоит +-
- chains_min_balances - мин баланс, если у вас балик ниже - то будет пробовать выводить если сетка добавлена в withdrawal_networks и есть баланс на бирже
- source_chains / destination_chains - откуда и куда бриджим
- withdrawal_amounts сколько выводить в каждую сетку
