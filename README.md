# AES Encryption Core in Verilog 🔐

This project implements a **128-bit AES (Advanced Encryption Standard)** encryption engine using **Verilog HDL**. It is designed for hardware-based cryptographic acceleration and security applications in embedded systems and VLSI architectures.

The core is written in **structural RTL** and simulates the full AES encryption process, including all transformation steps: SubBytes, ShiftRows, MixColumns, and AddRoundKey. This project strengthens my expertise in secure digital design and RTL module integration.

---

## 🎯 Objective

- To implement a synthesizable AES-128 encryption core in Verilog
- To simulate the functionality and validate correctness using test vectors
- To understand and apply block cipher architecture in hardware

---

## 🛠️ Tools & Technology

| Item              | Details                        |
|-------------------|--------------------------------|
| HDL Language      | Verilog                        |
| Simulation Tool   | Xilinx ISE / ISim / ModelSim   |
| Encryption Mode   | AES-128 (ECB, one block)       |
| Target Platform   | FPGA/RTL simulation            |

---

## 🔐 AES Overview

AES (Advanced Encryption Standard) is a symmetric-key algorithm used for secure data encryption. AES-128 operates on:
- **128-bit blocks**
- **128-bit key**
- **10 rounds** of transformation

Each round includes:
1. **SubBytes** – Byte substitution using an S-box
2. **ShiftRows** – Row-wise permutation
3. **MixColumns** – Column mixing via matrix multiplication
4. **AddRoundKey** – XOR with a round-specific key

---

## 📂 Repository Contents

### 🔹 Core AES Modules

| File Name             | Description                       |
|----------------------|------------------------------------|
| `AES.v`              | Top-level wrapper for AES core     |
| `AES_Encrypt.v`      | AES encryption controller          |
| `AES_Decrypt.v`      | AES decryption controller          |
| `encryptRound.v`     | AES encryption round logic         |
| `decryptRound.v`     | AES decryption round logic         |
| `addRoundKey.v`      | XOR round key to state             |
| `keyExpansion.v`     | Key schedule for 10 rounds         |
| `sbox.v`             | Substitution box (ROM-based)       |
| `inverseSbox.v`      | Inverse substitution box           |
| `AES Decrypt Output,wcfg`      | Waveform Output           |
| `AES Verilog File Descriptions`      | PDF Explaining Purpose of each file        |

### 🔹 AES Transformations

| Module File             | Description                        |
|-------------------------|-------------------------------------|
| `subBytes.v`            | Byte substitution                   |
| `inverseSubBytes.v`     | Inverse of SubBytes                 |
| `shiftRows.v`           | Shift rows left (encryption)        |
| `inverseShiftRows.v`    | Shift rows right (decryption)       |
| `mixColumns.v`          | MixColumns transformation           |
| `inverseMixColumns.v`   | Inverse MixColumns                  |

### 🔹 Testbenches

| Testbench File            | Tests                            |
|---------------------------|----------------------------------|
| `AES_tb.v`                | Full AES encryption/decryption   |
| `AES_Encrypt_tb.v`        | Encrypt-only pipeline            |
| `AES_Decrypt_tb.v`        | Decrypt-only pipeline            |
| `addRoundKey_tb.v`        | Round key logic                  |
| `keyExpansion_tb.v`       | Key schedule logic               |
| `subBytes_tb.v`           | S-box transformation             |
| `inverseSubBytes_tb.v`    | Inverse SubBytes                 |
| `shiftRows_tb.v`          | Row permutation                  |
| `inverseShiftRows_tb.v`   | Inverse row permutation          |
| `mixColumns_tb.v`         | Column mixing                    |
| `inverseMixColumns_tb.v`  | Inverse column mixing            |


---

## 📊 Simulation

- The testbench provides a **known plaintext and key**
- Output is matched against expected AES-128 ciphertext
- Simulation validates correct operation of internal blocks and key expansion



## 💡 Key Highlights

- Fully modular and parameterized design
- Structural coding style for RTL synthesis
- Useful as an IP core in secure embedded devices
- Optimized for educational and FPGA-targeted applications

---

## 🚀 Future Scope

- Add AES decryption module
- Expand to AES-192 and AES-256 variants
- Support for multiple encryption modes (e.g., CBC, CTR)
- Integrate with AXI or APB bus for SoC-level communication
- Implement on FPGA (e.g., Spartan-6 or Artix-7)

---

## 📌 Applications

- Secure embedded systems (IoT devices, smartcards)
- Cryptographic accelerators in ASIC/FPGA design
- IP core development for SoCs

---

## 👩‍💻 Author

**Ritika Roy**  
Electronics & Communication Engineer | VLSI Design Enthusiast  
🔐 RTL Coding • Secure Digital Systems • FPGA  
[GitHub](https://github.com/ritikaroy01) • [LinkedIn](https://www.linkedin.com/in/ritikaroy01)

---

## 📜 License

This project is open-source and intended for academic, educational, and research purposes. Proper attribution is appreciated.
