# 🚀 SOLANA С НУЛЯ

Время **погружаться в Solana с полного нуля** и учиться писать скрипты для взаимодействия с блокчейном — **без лишнего шума, только код и практика**

---

## 📁 Уроки

Все уроки находятся в папке [`lessons`](./lessons) — каждый файл - отдельный мини-проект: **скрипт + теория**, которые ты можешь запускать, редактировать и изучать.

📂 Решения всех задач находятся в [`lessons/solvings`](./lessons/solvings)

---

## 🧠 Что ты узнаешь

- Как работать с **Solana SDK** на JavaScript/TypeScript (и Python)
- Как **создавать кошельки, делать airdrop, проверять баланс, отправлять SOL**
- Как пользоваться **Devnet**, RPC, и проверять транзакции
- Как написать свой софт для взаимодействия с [Jupiter](https://jup.ag/), [Radium](https://raydium.io) и многими другими

---

## 📦 Как начать: Полный гайд по окружению

![Jim Rohn](Jim%20Rohn.jpg)

```
"Покажи мне своё окружение — и я скажу, каким будет твоё будущее"
```

_Джим Рон явно имелл ввиду наше окружение при разработке на Solana_

### 🔨 JavaScript / TypeScript

1. Установи [Node.js (LTS)](https://nodejs.org/)

   > Это обеспечит тебя менеджером пакетов `npm`

2. Установи VS Code (для написания кода):  
   [code.visualstudio.com/](https://code.visualstudio.com/)

3. Установи Solana SDK:

   ```bash
   npm install --save @solana/web3.js@1
   ```

4. Убедись, что ты работаешь в `Devnet RPC`:

   ```ts
   import { Connection } from "@solana/web3.js";
   const connection = new Connection(
     "https://api.devnet.solana.com",
     "confirmed"
   );
   ```

5. Запускаем свои скрипты:

```bash
node index.js
```

или если используем TypeScript:

```bash
npx ts-node index.ts
```

---

### 🐍 Python (опционально)

1. Установи [Python 3.10+](https://www.python.org/downloads/)

2. Установи среду разработки:

```
vs code - редактор для всех языков

pycharm - редактор для пайтона, со всеми его бонусами и удобствами
```

- [VS Code](https://code.visualstudio.com/)
- [PyCharm Community](https://www.jetbrains.com/pycharm/download)

3. Создай виртуальное окружение:

   ```bash
   python -m venv venv
   source venv/bin/activate  # или venv\Scripts\activate в Windows
   ```

4. Установи библиотеки:

   ```bash
   pip install solders
   pip install solana
   ```

5. Пиши и запускай Python-скрипты (`.py`) — всё работает с Devnet:

   ```python
    from solana.rpc.api import Client
    http_client = Client("https://api.devnet.solana.com")
   ```

---

## 🔧 Devnet

> Все действия выполняем в **Devnet**
> RPC: `https://api.devnet.solana.com`

🔍 Проверка транзакций:
[https://explorer.solana.com/?cluster=devnet](https://explorer.solana.com/?cluster=devnet)

---

## 👶 С нуля до языка программирования

Если ты **никогда не писал код** — вот ресурсы, с которых лучше всего начать:

### 📚 Лучшие сайты для старта с JavaScript / TypeScript

- [jschallenger.com](https://jschallenger.com) — практика с нуля
- [learntypescript.online](https://learntypescript.online) — TypeScript шаг за шагом
- [hackerrank.com/dashboard](https://hackerrank.com/dashboard) — практикуем Python, математику, алгоритмы

---

## 🧠 Как всё запоминать?

**Записывай каждый шаг обучения:**

- [notion.so](https://notion.so) — удобно и кроссплатформенно
- [obsidian.md](https://obsidian.md) — локальное хранение, супер для разработчиков

> Веди дневник обучения, фиксируй задачи и их решения — это ускорит твой рост.

---

## ⚔ Алгоритмы и логика

Развиваем **алгоритмическое мышление**

- [leetcode.com](https://leetcode.com)
- [codewars.com](https://codewars.com)
- [hackerearth.com/practice](https://hackerearth.com/practice)

---

## ❓ Вопросы

Все вопросы — в [`Questions`](https://t.me/c/2772080252/291)
Спрашивай — помогут.

---

## 📢 Контакты

Автор репозитория — [@code_vartcall](https://t.me/code_vartcall)

💬 Все обновления — в Telegram!

---

> ⭐ Ставь звезду на репозиторий, если материал оказался полезен!
