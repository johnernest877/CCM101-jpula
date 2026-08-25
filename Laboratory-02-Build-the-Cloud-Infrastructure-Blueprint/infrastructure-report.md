# Cloud Infrastructure Report

## 1. Operating System

The cloud server is running **Ubuntu 24.04.4 LTS** (codename **Noble**).

## 2. Kernel Version

**6.8.0-138-generic**

## 3. CPU

| Detail | Value |

| --- | --- |

| Model | Intel Xeon E312xx (Sandy Bridge, IBRS update) |

| Cores | 1 |

## 4. Memory

| Memory    | Amount  |

| --------- | ------: |

| Total RAM | 1.9 GiB |

| Used      | 453 MiB |

| Free      | 747 MiB |

| Available | 1.4 GiB |

| Swap      | 1.0 GiB |

## 5. Disk Capacity

| File System | Size | Used | Available | Usage | Mount Point |

| ----------- | ---: | ---: | --------: | ----: | ----------- |

| `/dev/vda1` |  19G | 5.4G |       13G |   30% | `/`         |

## 6. Mounted File Systems

| File System  | Size | Used | Available | Usage | Mounted On  |

| ------------ | ---: | ---: | --------: | ----: | ----------- |

| `tmpfs`      | 191M | 996K |      190M |    1% | `/run`      |

| `/dev/vda1`  |  19G | 5.4G |       13G |   30% | `/`         |

| `tmpfs`      | 952M |  84K |      952M |    1% | `/dev/shm`  |

| `tmpfs`      | 5.0M |    0 |      5.0M |    0% | `/run/lock` |

| `/dev/vda16` | 881M | 117M |      703M |   15% | `/boot`     |

| `/dev/vda15` | 105M | 6.2M |       99M |    6% | `/boot/efi` |

## 7. Hostname

**ubuntu**

## 8. IP Addresses

- **172.30.1.2**

- **172.17.0.1**

## 9. Commands Used

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

## 10. Summary

The KillerCoda environment provides a virtualized **Ubuntu 24.04.4 LTS** cloud server, hostname **ubuntu**, reachable at **172.30.1.2** and **172.17.0.1**. It runs on an **Intel Xeon E312xx** processor with a single core, roughly **1.9 GiB of RAM**, and a **19 GB** main disk partition (`/dev/vda1`) that is 30% utilized. Additional mounted file systems support the OS, boot, EFI, and temporary in-memory data.
