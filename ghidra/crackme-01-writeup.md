
# Crackmes.one - 1st write-up 

* **Source Material:** crackmes.one 
* **URL:** https://crackmes.one/crackme/6a512980234391ae74f63ae8 
* **File Name:** `level1easy.exe` 
* **MD5:** `ee43bb935bdcd442363ca5f0d2372137`
* **SHA256:** `2a7fc7448560b95eef9c7f95ceab51a7c155d92945f0848bead38f5ea6e83ec9`
* **Architecture:** x86-64 | **Language:** C/C++
* **Platform:**  Windows
---
### Executive Summary:

Performed static analysis on `level1easy.exe` to reverse engineer the password validation routine using Ghidra. Analysis revealed PE logic, and built-in code with variables .The valid password (`password`) was recovered without requiring dynamic analysis.

---
### Technical Triage

![[Pasted image 20260818165739.png]]

**Community score** : 1/70 security vendor flag this PE as malicious.
**Protections:** None (No Packers / No Anti-Debugging)

---
### Decompilation & Static Analysis

1) Program main code.

Found password identificator via `Ghidra Search` using `Search For String` option.The string `Enter Password:` referenced at `140003438` led directly to the core validation block via `XREF[1]`.
![[Pasted image 20260818161711.png]]

Located the primary target function (`FUN_140001290`).
![[Pasted image 20260818164046.png]]


2) Password Logic & Variables

![[Pasted image 20260818163626.png]]

![[Pasted image 20260818162339.png]]


3) Result
I used `wine` to test analysis results of `Ghidra` (Because PE was built for Windows platform), and it ended successfully.

![[Pasted image 20260818164801.png]]

---

### IoCs:

| Type      | Value                                                              |
| --------- | ------------------------------------------------------------------ |
| File Name | `level1easy.exe`                                                   |
| MD5       | `ee43bb935bdcd442363ca5f0d2372137`                                 |
| SHA256    | `2a7fc7448560b95eef9c7f95ceab51a7c155d92945f0848bead38f5ea6e83ec9` |
| Flag{}    | `password`                                                         |

---

### Notes

- `Ghidra` option must have to static binary analysis of PE, it shortens a lot of work.
