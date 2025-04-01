# Server Overview


# System Specifications Comparison

| Feature          | Playground System                                | TLServer System                                | Cameras System                                 |
|------------------|--------------------------------------------------|------------------------------------------------|-------------------------------------------------|
| **CPU** | Pentium Dual-Core E5300 @ 2.60GHz (2 cores)       | Intel Xeon E5-1603 v3 @ 2.80GHz (4 cores)      | Intel Core2 Duo E7500 @ 2.93GHz (2 cores)      |
| **Architecture** | x86_64                                           | x86_64                                         | x86_64                                          |
| **RAM** | 2GB DDR2 (800 MT/s)                               | 32GB DDR4 (1866 MT/s configured, 2667 MT/s rated)| 2GB DDR2 (667 MT/s)                              |
| **Storage** | 109GB HDD (root), 293GB HDD (/mnt/320GB)          | 233GB NVMe (root), 110GB, 3.6TB, 1.8TB HDDs     | 109GB HDD (root), 916GB (/mnt/HDD2), 916GB (/mnt/HDD1) |
| **OS** | Debian 12 (bookworm)                              | Debian 12 (bookworm)                             | Debian 12 (bookworm)                             |
| **Kernel** | 6.1.0-32-amd64                                   | 6.1.0-28-amd64                                 | 6.1.0-28-amd64                                 |
| **Swap** | 974 MiB (Almost Full)                             | 975 MiB (Partially used)                         | 974 MiB (Partially used)                         |
| **L1d Cache** | 64 KiB (2 instances)                             | 128 KiB (4 instances)                            | 64 KiB (2 instances)                             |
| **L1i Cache** | 64 KiB (2 instances)                             | 128 KiB (4 instances)                            | 64 KiB (2 instances)                             |
| **L2 Cache** | 2 MiB (1 instance)                               | 1 MiB (4 instances)                              | 3 MiB (1 instance)                               |
| **L3 Cache** | N/A                                              | 10 MiB (1 instance)                              | N/A                                              |
| **SMT** | Disabled (for vulnerability mitigation)          | Disabled (for vulnerability mitigation)          | Disabled (for vulnerability mitigation)          |
| **dmidecode** | Installed(After initial command fail)             | Installed(After initial command fail)             | Installed(After initial command fail)             |

## Server 1: **Cameras**
| **Category**         | **Details**                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| **CPU Model**        | Intel(R) Xeon(R) CPU E5-1603 v3 @ 2.80GHz                                   |
| **Cores / Threads**  | 4 cores, 1 thread per core                                                  |
| **RAM**              | 2 GB DDR2, 667-800 MT/s, Kingston                                          |
| **Storage**          | 110 GB SSD (sdb1), 3.6 TB HDD (sdc1), 1.8 TB HDD (sda1)                    |
| **Operating System** | Debian GNU/Linux 12 (bookworm)                                              |
| **Kernel Version**   | 6.1.0-28-amd64                                                             |
| **Architecture**     | x86_64                                                                      |
| **Virtualization**   | VT-x (Intel Virtualization Support)                                         |

## Server 2: **TLServer**
| **Category**         | **Details**                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| **CPU Model**        | Intel(R) Xeon(R) CPU E5-1603 v3 @ 2.80GHz                                   |
| **Cores / Threads**  | 4 cores, 1 thread per core                                                  |
| **RAM**              | 32 GB DDR4, 2667 MT/s, Hynix (1866 MT/s configured speed)                   |
| **Storage**          | 233 GB SSD (nvme0n1p1), 110 GB SSD (sdb1), 3.6 TB HDD (sdc1), 1.8 TB HDD (sda1) |
| **Operating System** | Debian GNU/Linux 12 (bookworm)                                              |
| **Kernel Version**   | 6.1.0-28-amd64                                                             |
| **Architecture**     | x86_64                                                                      |
| **Virtualization**   | VT-x (Intel Virtualization Support)                                         |

## Server 3: **Playground**
| **Category**         | **Details**                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| **CPU Model**        | Intel(R) Xeon(R) CPU E5-1603 v3 @ 2.80GHz                                   |
| **Cores / Threads**  | 4 cores, 1 thread per core                                                  |
| **RAM**              | 2 GB DDR2, 667 MT/s, Kingston                                              |
| **Storage**          | 110 GB SSD (sdb1), 3.6 TB HDD (sdc1), 1.8 TB HDD (sda1)                    |
| **Operating System** | Debian GNU/Linux 12 (bookworm)                                              |
| **Kernel Version**   | 6.1.0-28-amd64                                                             |
| **Architecture**     | x86_64                                                                      |
| **Virtualization**   | VT-x (Intel Virtualization Support) 
