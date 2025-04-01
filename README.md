# Server Overview

## **Cameras Server**

### **CPU:**

| Feature           | Details                          |
|-------------------|----------------------------------|
| Vendor            | Intel                            |
| Model             | Pentium(R) Dual-Core CPU E5300 @ 2.60GHz |
| Cores             | 2                                |
| Threads           | 2 (1 per core)                   |
| Base Clock        | 2.6 GHz                          |
| L1 Cache          | 64 KiB per core                 |
| L2 Cache          | 2 MiB                            |
| Speed             | 667 MHz to 2600 MHz (scalable)  |

### **RAM:**

| Feature           | Details                          |
|-------------------|----------------------------------|
| Total             | 2 GB                             |
| Type              | DDR2                             |
| Speed             | 667 MT/s                         |
| Manufacturer      | Kingston                         |
| Form Factor       | DIMM                             |
| Slot              | J6H1 (2 GB)                      |

### **Storage:**

| Disk              | Size  | Used  | Free  |
|-------------------|-------|-------|-------|
| **/dev/sda1 (HDD1)** | 916 GB | 861 GB | 46 GB |
| **/dev/sdb1**       | 109 GB | 23 GB  | 81 GB |
| **/dev/sdc1 (HDD2)** | 916 GB | 374 GB | 534 GB |

### **Operating System:**

| Feature           | Details                          |
|-------------------|----------------------------------|
| Distribution      | Debian GNU/Linux 12 (bookworm)   |
| Kernel            | 6.1.0-28-amd64                   |

### **Swap:**

| Total  | Used  | Free  |
|--------|-------|-------|
| 974 MB | 669 MB | 305 MB |

---

## **Playground Server**

### **CPU:**

| Feature           | Details                          |
|-------------------|----------------------------------|
| Vendor            | Intel                            |
| Model             | Pentium(R) Dual-Core CPU E5300 @ 2.60GHz |
| Cores             | 2                                |
| Threads           | 2 (1 per core)                   |
| Base Clock        | 2.6 GHz                          |
| L1 Cache          | 64 KiB per core                 |
| L2 Cache          | 2 MiB                            |
| Speed             | 667 MHz to 2600 MHz (scalable)  |

### **RAM:**

| Feature           | Details                          |
|-------------------|----------------------------------|
| Total             | 2 GB                             |
| Type              | DDR2                             |
| Speed             | 667 MT/s                         |
| Manufacturer      | Kingston                         |
| Form Factor       | DIMM                             |
| Slot              | J6H1 (2 GB)                      |

### **Storage:**

| Disk              | Size  | Used  | Free  |
|-------------------|-------|-------|-------|
| **/dev/sda1 (320GB)** | 293 GB | 99 GB  | 191 GB |
| **/dev/sdb1**       | 109 GB | 7.3 GB | 96 GB  |

### **Operating System:**

| Feature           | Details                          |
|-------------------|----------------------------------|
| Distribution      | Debian GNU/Linux 12 (bookworm)   |
| Kernel            | 6.1.0-32-amd64                   |

### **Swap:**

| Total  | Used  | Free  |
|--------|-------|-------|
| 974 MB | 974 MB | 172 KiB |

---

## **Comparison**

| Feature             | Cameras Server                | Playground Server            |
|---------------------|-------------------------------|------------------------------|
| **CPU**             | Pentium(R) Dual-Core CPU E5300 | Pentium(R) Dual-Core CPU E5300 |
| **Cores/Threads**   | 2/2                            | 2/2                          |
| **RAM**             | 2 GB DDR2, 667 MT/s           | 2 GB DDR2, 667 MT/s         |
| **Storage**         | 3 disks (2 HDDs)              | 2 disks (1 HDD, 1 SSD)       |
| **Swap**            | 974 MB                        | 974 MB                      |
| **OS**              | Debian GNU/Linux 12 (bookworm) | Debian GNU/Linux 12 (bookworm) |
| **Kernel Version**  | 6.1.0-28-amd64                | 6.1.0-32-amd64              |

