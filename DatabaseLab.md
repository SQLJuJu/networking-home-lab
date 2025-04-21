# Home Lab for Learning Database Administration

This guide outlines a budget-friendly home lab setup for anyone looking to get hands-on experience with major relational database systems, including SQL Server, Oracle, PostgreSQL, and MySQL/MariaDB.

## Goals

- Install & configure SQL Server, Oracle, PostgreSQL, and MySQL
- Practice DBA tasks:
  - Backups & restores
  - Query tuning & indexing
  - User roles & permissions
  - Replication & High Availability
  - Security & automation
- Simulate hybrid environments and real-world setups
- Use automation tools like Ansible, PowerShell, Terraform (optional)

---

## Core Hardware Setup

### Lab Server (Virtualization Host)
- **Model:** Dell OptiPlex 7010 / 9010 SFF or Lenovo ThinkCentre M92p
- **Specs:** i5/i7, 32GB RAM, 500GB+ SSD
- **OS:** Proxmox VE, Hyper-V, or VirtualBox
- **Cost:** ~$80–$130 used
- **Why:** Quiet, efficient, capable of running 4–6 VMs

### Optional Secondary Host
- **Use for:** Replication / HA / cluster setups
- **Can use:** A second OptiPlex or even a Raspberry Pi for light DBs

---

## Suggested VM Layout

| VM Name     | OS               | DBMS                 | RAM   | Purpose |
|-------------|------------------|----------------------|-------|---------|
| `sql-node1` | Windows Server 2019 | SQL Server 2022 Dev | 4–6GB | Main Microsoft SQL Server instance |
| `oracle-node1` | Oracle Linux 8 | Oracle 19c XE         | 4GB   | Enterprise-grade Oracle environment |
| `pgsql-node1` | Ubuntu 22.04    | PostgreSQL 15         | 2–3GB | Advanced open-source RDBMS |
| `mysql-node1` | Ubuntu 22.04    | MySQL 8 / MariaDB     | 2–3GB | Replication, tuning, etc. |
| `mgmt-node` | Windows 10 or Ubuntu | Admin tools       | 2GB   | DBeaver, SSMS, pgAdmin, scripts |

---

## Software Stack

- **SQL Server 2022 Developer Edition** – Free for learning
- **Oracle Database 19c XE** – Lightweight but feature-rich
- **PostgreSQL** – Flexible open-source RDBMS
- **MySQL / MariaDB** – Popular in web and app environments
- **DBeaver** – Multi-platform DB management GUI
- **SSMS, pgAdmin, Oracle SQL Developer** – Native tools
- **Proxmox VE** – Powerful free virtualization platform

---

## Optional Network Layer

- Add a pfSense VM to simulate network segmentation
- Assign separate VLANs/subnets for DB tiers
- Test database access control and security across "zones"

---

## Learning Exercises

- Create and restore backups in each RDBMS
- Set up SQL Server Agent jobs and alerts
- Configure PostgreSQL replication
- Use `EXPLAIN` and query plans for performance tuning
- Secure your MySQL installation and enable SSL
- Automate provisioning of databases using:
  - **Ansible** (Linux)
  - **PowerShell DSC** (Windows)

---

## Budget Estimate

| Item                     | Est. Cost |
|--------------------------|-----------|
| OptiPlex / ThinkCentre   | $100      |
| SSD (upgrade if needed)  | $25–$50   |
| Software (DBMS, tools)   | Free      |
| Optional second host     | $60–$100  |
| **Total**                | **$100–$150** |

---

## Useful Resources

- [AdventureWorks](https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure): SQL Server sample DB
- [Sakila](https://dev.mysql.com/doc/sakila/en/): MySQL sample DB
- [PostgreSQL Exercises](https://pgexercises.com/)
- [Oracle Live SQL](https://livesql.oracle.com/)

---

## License

MIT

