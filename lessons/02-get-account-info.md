# 📦 Урок 2 — Чтение информации об аккаунте

Во втором уроке мы научимся **извлекать данные об аккаунтах в сети Solana**. Это фундаментальный навык, который понадобится при взаимодействии с контрактами, кошельками и токенами.

---

## 🎯 ЗАДАЧА

Напиши скрипт, который:

1. Подключается к **Devnet**
2. Принимает на вход **публичный ключ** (можно задать переменной или через аргумент)
3. Получает и выводит:
   - Баланс в SOL
   - Существует ли аккаунт (или `null`)
   - Размер аккаунта в байтах
   - Владелец (owner)
   - Является ли executable
   - Rent epoch

---

## 💡 Подсказки

### 📘 Используй метод

```ts
const info = await connection.getAccountInfo(new PublicKey(pubkey));
```

Если `info === null`, значит аккаунт **не существует** в сети.

---

### 📐 Пример структуры AccountInfo:

```ts
{
  data: Buffer,
  executable: boolean,
  lamports: number,
  owner: PublicKey,
  rentEpoch: number
}
```

---

### 📤 Пример вывода скрипта:

```
🔎 Account: 2AfsqkTa7aL1DcsqehaCp815APiGJWeuAEVsKuSWa3JT
💰 Balance: 0.002039 SOL
✅ Exists: true
📏 Data size: 0 bytes
🧑‍💼 Owner: 11111111111111111111111111111111
⚙️ Executable: false
📆 Rent epoch: 415
```

---

## 📚 Что ты узнаешь:

- Как работает `getAccountInfo`
- Что такое `lamports` и `rent_epoch`
- Как выглядит структура аккаунта в Solana
- Как обрабатывать ситуации, когда аккаунта ещё нет в сети

---

## 🧪 Devnet RPC

```
https://api.devnet.solana.com
```

---

## 🔗 Explorer для проверки

[explorer.solana.com/?cluster=devnet](https://explorer.solana.com/?cluster=devnet)

## 📚 База знаний: что нужно знать, чтобы выполнить этот урок

---

### 🔤 **Переменные и константы**

- Как объявлять переменные с помощью `const` и `let`
- Понимание разницы: `const` — неизменяемая ссылка, `let` — можно менять

```ts
const address = "2AfsqkT...";
let balance = 0;
```

---

### 📦 **Импорт библиотек**

- Как импортировать модули из Solana SDK

```ts
import { Connection, PublicKey } from "@solana/web3.js";
```

---

### 🌐 **Работа с RPC**

- Как создать соединение с сетью:

```ts
import { Connection } from "@solana/web3.js";
const connection = new Connection("https://api.devnet.solana.com", "confirmed");
```

---

### 🧠 **Типы данных**

- Строки: `"hello"`
- Числа: `0.1`, `123`
- Boolean (логические): `true`, `false`
- Объекты: `{ key: "value" }`

---

### 🧱 **Работа с объектами**

- Как обращаться к полям объекта:

```ts
console.log(accountInfo.lamports);
console.log(accountInfo.owner.toBase58());
```

---

### ❓ **Условия (if / else)**

- Как проверить, существует ли аккаунт:

```ts
if (accountInfo === null) {
  console.log("Аккаунт не существует");
} else {
  console.log("Аккаунт существует");
}
```

---

### 🔄 **Функции**

- Как обернуть код в `async function` и использовать `await`

```ts
const main = async () => {
  const info = await connection.getAccountInfo(new PublicKey(pubkey));
};
main();
```

---

💡 Непонятно — не бойся задавать вопросы в [Questions](https://t.me/c/2772080252/291)
