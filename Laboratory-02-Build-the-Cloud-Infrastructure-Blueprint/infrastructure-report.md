<div align="center">

# 🖥️ Cloud Infrastructure Report

`ubuntu` · KillerCoda virtualized cloud instance

![OS](https://img.shields.io/badge/OS-Ubuntu%2024.04.4%20LTS-E95420?logo=ubuntu&logoColor=white)
![Kernel](https://img.shields.io/badge/Kernel-6.8.0--138--generic-333333?logo=linux&logoColor=white)
![Cores](https://img.shields.io/badge/vCPU-1-blue)
![RAM](https://img.shields.io/badge/RAM-1.9%20GiB-informational)
![Disk](https://img.shields.io/badge/Disk-19GB%20(30%25%20used)-yellow)

</div>

---

## 📋 At a Glance

| | |
|---|---|
| **OS** | Ubuntu 24.04.4 LTS (Noble) |
| **Kernel** | `6.8.0-138-generic` |
| **CPU** | Intel Xeon E312xx (Sandy Bridge, IBRS update) — 1 core |
| **Memory** | 1.9 GiB total |
| **Disk** | 19 GB (`/dev/vda1`, 30% used) |
| **Hostname** | `ubuntu` |
| **IP addresses** | `172.30.1.2`, `172.17.0.1` |

---

## 🧬 Operating System

> **Ubuntu 24.04.4 LTS** — codename **Noble**

**Kernel:** `6.8.0-138-generic`

---

## ⚙️ CPU

| Detail | Value |
|---|---|
| Model | Intel Xeon E312xx (Sandy Bridge, IBRS update) |
| Cores | 1 |

---

## 🧠 Memory

| Metric | Amount |
|---|---:|
| Total RAM | 1.9 GiB |
| Used | 453 MiB |
| Free | 747 MiB |
| Available | 1.4 GiB |
| Swap | 1.0 GiB |

---

## 💾 Disk Capacity

| Filesystem | Size | Used | Available | Usage | Mount |
|---|---:|---:|---:|---:|---|
| `/dev/vda1` | 19G | 5.4G | 13G | `███░░░░░░░` 30% | `/` |

---

## 📂 Mounted File Systems

| Filesystem | Size | Used | Available | Usage | Mounted On |
|---|---:|---:|---:|---:|---|
| `tmpfs` | 191M | 996K | 190M | `░░░░░░░░░░` 1% | `/run` |
| `/dev/vda1` | 19G | 5.4G | 13G | `███░░░░░░░` 30% | `/` |
| `tmpfs` | 952M | 84K | 952M | `░░░░░░░░░░` 1% | `/dev/shm` |
| `tmpfs` | 5.0M | 0 | 5.0M | `░░░░░░░░░░` 0% | `/run/lock` |
| `/dev/vda16` | 881M | 117M | 703M | `█░░░░░░░░░` 15% | `/boot` |
| `/dev/vda15` | 105M | 6.2M | 99M | `░░░░░░░░░░` 6% | `/boot/efi` |

---

## 🌐 Network

| | |
|---|---|
| **Hostname** | `ubuntu` |
| **IP addresses** | `172.30.1.2` · `172.17.0.1` |

---

## 🛠️ Commands Used

<details>
<summary>Click to expand shell history</summary>

```bash
lsb_release -a
uname -r
lscpu | grep "Model name"
nproc
free -h
df -h
hostname
hostname -I
```

</details>

---

## 📝 Summary

> The KillerCoda environment provides a virtualized **Ubuntu 24.04.4 LTS** cloud server, hostname `ubuntu`, reachable at `172.30.1.2` and `172.17.0.1`. It runs on an **Intel Xeon E312xx** processor with a single core, roughly **1.9 GiB** of RAM, and a **19 GB** main disk partition (`/dev/vda1`) at 30% utilization. Additional mounted file systems support the OS, boot, EFI, and temporary in-memory data.

---

<div align="center">

*Generated diagnostic snapshot — static report*

</div>
