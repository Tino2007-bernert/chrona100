# ⚙️ Chrona100

**Chrona100** is a lightweight, deterministic time calculation system that converts real-world UTC time into a structured, decimal (100-based) time representation starting from **Epoch 2000** (01.01.2000 00:00:00 UTC).

It replaces irregular Gregorian units (months, leap hours, 60-second minutes) with a uniform, hierarchical structure consisting of **Cycles, Tags, Tiks, Miks, and Units**.

---

## 🌍 Concept & Epoch

* **Base Epoch:** `2000-01-01 00:00:00 UTC` (Chrona Standard Time `0:0:0:0:0`)
* **Core Ratio:** $1 \text{ second} \approx 11.574074074 \text{ Units}$
* **1 Standard Day (86,400s):** Exactly $1,000,000 \text{ Units}$

---

## 🧩 Time Hierarchy Structure

Chrona100 operates on a hierarchical 100-based scale:

| Unit | Sub-Units | Total Units | Real World Equivalent (Approx.) |
| :--- | :--- | :--- | :--- |
| **1 Unit** | - | $1$ | $\approx 86.4 \text{ ms}$ ($0.0864 \text{s}$) |
| **1 Mik** | $100 \text{ Units}$ | $100$ | $\approx 8.64 \text{ s}$ |
| **1 Tik** | $100 \text{ Miks}$ | $10,000$ | $14 \text{ min } 24 \text{ s}$ ($864 \text{s}$) |
| **1 Tag** | $100 \text{ Tiks}$ | $1,000,000$ | $24 \text{ hours}$ ($86,400 \text{s}$) |
| **1 Cycle** | $100 \text{ Tags}$ | $100,000,000$ | $100 \text{ days}$ |

---

## 💾 Mathematical Encoding

A Chrona100 value is uniquely encoded into a total unit count using the following formula:

$$\text{TotalUnits} = (\text{Cycle} \times 10^8) + (\text{Tag} \times 10^6) + (\text{Tik} \times 10^4) + (\text{Mik} \times 10^2) + \text{Unit}$$

---

## 🔁 Features

- ✔ **Real-Time Conversion:** Live conversion between standard JS `Date` / PHP `DateTime` and Chrona100 format.
- ✔ **Deterministic Logic:** Pure mathematical mapping from Epoch 2000 without leap second edge-case issues.
- ✔ **Encoder & Decoder:** Full two-way conversion support.
- ✔ **Developer Utilities:** Includes interactive web UI and debug view.
- ✔ **Multi-Language Support:** SDK available for JavaScript and PHP.

---

## 🚀 Usage & Quickstart

### 1. Web Interface
Clone the repository and open `index.html` in any modern web browser to view live time conversions and the debug tool.

```bash
git clone [https://github.com/Tino2007-bernert/chrona100.git](https://github.com/Tino2007-bernert/chrona100.git)
cd chrona100
# Open index.html in your browser

```

### 2. JavaScript (`chrona.js`)

```javascript
import { Chrona } from './chrona.js';

// Encode current time to Chrona
const chronaTime = Chrona.now();
console.log(chronaTime.toString()); // e.g., "97:84:12:05:42"

// Decode Chrona back to JS Date
const date = Chrona.decode("97:84:12:05:42");
console.log(date.toISOString());

```

### 3. PHP (`chrona.php`)

```php
require_once 'chrona.php';

// Encode current timestamp
$chrona = Chrona::now();
echo $chrona->format(); // e.g., "97:84:12:05:42"

// Decode back to UNIX timestamp / DateTime
$dateTime = Chrona::decode("97:84:12:05:42");

```

---

## ⚙️️ Status

This project is experimental and under active development.

---

## 👤 Author

* **Tino Bernert** — Creator & Developer

---

## 🔗 Links

* **Repository:** [GitHub - Tino2007-bernert/chrona100](https://www.google.com/search?q=https://github.com/Tino2007-bernert/chrona100)
