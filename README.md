# Reverse Engineering & Malware Analysis Lab

*Focused on static and basic dynamic binary analysis, Windows API behavior tracking, Ghidra decompilation, and extractable IoCs for Threat Hunting and Detection Engineering.*

---

## 🛠 Technical Stack

* **Static & Disassembly Analysis:** Ghidra, PEStudio, FLOSS / Strings, Godbolt Compiler Explorer.
* **File Format & PE Inspection:** PEStudio, Detect It Easy (DIE), PE-bear.
* **Detection & Blue Team:** Suspicious Windows API Mapping, YARA Rule Drafting, IoC Extraction.

---

## 🔧 Tools & Techniques

* **Reverse Engineering:** Ghidra decompiler workflows, Control Flow Graph (CFG) analysis, function renaming, and data retyping.
* **PE Header Inspection:** Import Address Table (IAT) auditing, section entropy verification, suspicious API call identification.
* **Malware Dissection:** XOR loop analysis, string extraction/deobfuscation, CrackMe logic reversing, and threat detection profiling.

---

## 📁 Labs

This section contains the core practical work , including Ghidra writeups, and challenge solutions.

| # | Lab / Guide | Key Findings | Focus Area |
|---|---|---|---|
| 01 | [Strings & FLOSS Analysis](./static-analysis/strings-analysis.md) | Extracting obfuscated strings, grep filtering for IoCs | Static Analysis |
| 02 | [CrackMe #01 Writeup](./ghidra/crackme-01-writeup.md) | Ghidra decompilation, reversing hardcoded validation logic | Decompilation |
| 03 | [CrackMe #02 Writeup](./ghidra/crackme-02-writeup.md) | Reversing anti-analysis techniques and custom algorithm logic | Logic Analysis |
| 04 | [Challenges.re Writeups](./challenges/challenges-re-solutions.md) | Solutions and detection takeaways from practical RE challenges | Practical RE |

---

## 🚩 Current Objectives

* Master Ghidra decompilation to extract readable logic from obfuscated binaries.
* Map suspicious assembly patterns and Windows API calls directly to detection rules (YARA / Sysmon).

---

## ⚠️ Disclaimer
All activities were performed in a controlled, isolated lab environment for educational and defensive research purposes.

---
[![Back to Profile](https://img.shields.io/badge/BACK_TO_PROFILE-333333?style=plastic&logo=github&logoColor=white)](https://github.com/lewandovskii9)
