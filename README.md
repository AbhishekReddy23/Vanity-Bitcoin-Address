# 🪙Vanity-Bitcoin-Address

🔍 Objective

This project demonstrates the computational effort behind Bitcoin mining by generating custom Bitcoin addresses (known as vanity addresses) that follow specific character patterns derived from your name.
It provides hands-on experience with cryptographic computation and the complexity involved in customizing blockchain addresses.

🧠 Task Overview

Generate five addresses where each address’s characters match an increasing prefix of your first name:

| **Address #** | **Pattern Requirement** |
|:--:|:--|
| 1 | 2nd character = 1st letter of your name |
| 2 | 2nd–3rd characters = 1st–2nd letters of your name |
| 3 | 2nd–4th characters = 1st–3rd letters of your name |
| 4 | 2nd–5th characters = 1st–4th letters of your name |
| 5 | 2nd–6th characters = 1st–5th letters of your name |

If your first name has fewer than 5 characters, concatenate with your surname.

🧰 Tools & Methods

Primary: Vanitygen++ (10gic/vanitygen-plusplus
) — recommended for GPU support (OpenCL).

Alternate method: a Python script I wrote to generate addresses suitable for Windows Users (see code/generate_vanity.py).

OS: Linux (Kali/Ubuntu recommended)

⚙️ Example Vanitygen++ Commands

| **Command #** | **Command Used** |
|:--:|:--|
| 1 | `./vanitygen++ -v 1A` |
| 2 | `./vanitygen++ -v 1Ab` |
| 3 | `./vanitygen++ -v 1Abh` |
| 4 | `./vanitygen++ -v 1Abhi` |
| 5 | `./vanitygen++ -v 1Abhis` |

⚡ CPU vs GPU

During generation, I observed that CPU performance quickly becomes a bottleneck as the pattern length increases.
Each extra matching character exponentially increases the computation time.
Using GPUs, which perform thousands of operations in parallel, drastically improves performance—mirroring how real Bitcoin miners use GPU or ASIC hardware for faster results.
