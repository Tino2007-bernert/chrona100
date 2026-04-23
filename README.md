# ⚙️ Chrona100

Chrona100 is a lightweight time calculation tool that converts real-world time (Epoch 2000) into a custom 100-based unit system with cycles, tags, tiks, miks and units.

It includes:
- encoder / decoder
- live time conversion
- debug view
- deterministic time structure

---

# 🌍 Concept

Chrona100 is based on a fixed time epoch:


01.01.2000 00:00:00 UTC


From this point, all time is converted into a structured numeric system.

---

# ⏱ Core Conversion


1 second = 11.574074 Units


---

# 🧩 Chrona100 Structure

Time is split into a hierarchical 100-based system:


1 Cycle = 100,000,000 Units
1 Tag = 1,000,000 Units
1 Tik = 10,000 Units
1 Mik = 100 Units


---

# 🔁 Features

✔ Real-time conversion  
✔ Epoch-based calculation  
✔ Encoder / Decoder system  
✔ Debug tool for developers  
✔ Fully deterministic logic  

---

# 💾 Example Encoding


ChronaValue =
(Cycle × 10^8)

(Tag × 10^6)
(Tik × 10^4)
(Mik × 10^2)
Unit

---

# 🧠 Purpose

Chrona100 is designed as:

- a time transformation system
- a developer utility
- a simulation-friendly time format
- a reproducible time standard

---

# 🚀 Usage

Clone the repo and open:


index.html


or use the SDK:

- JavaScript (chrona.js)
- PHP (chrona.php)

---

# ⚙️ Status

This project is experimental and evolving.

---

# 👤 Author

Created by **Tino Bernert**

---

# 🔗 Repository

Chrona100 project:
[GITHUB REPO](https://github.com/Tino2007-bernert/chrona100/)
