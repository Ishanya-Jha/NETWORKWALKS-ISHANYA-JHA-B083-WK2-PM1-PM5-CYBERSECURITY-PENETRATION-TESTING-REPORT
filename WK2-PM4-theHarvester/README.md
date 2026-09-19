# 🔎 W2-PM4: Footprinting & Reconnaissance with theHarvester

## 📌 Project Overview

This project is part of **Week 2** of the **Cybersecurity & Ethical Hacking Internship** at **Networkwalks**.

The objective of this module is to understand how **theHarvester** can be used for passive reconnaissance and information gathering, particularly for identifying publicly available email addresses, subdomains, hostnames, and related information associated with a target domain.

All activities were performed within the assigned educational scope and with appropriate authorization.

---

## 📋 Project Information

| Field | Details |
|---|---|
| **Program** | Cybersecurity & Ethical Hacking Internship |
| **Organization** | Networkwalks |
| **Training Week** | Week 2 |
| **Project Module** | W2-PM4 |
| **Module Title** | Footprinting & Reconnaissance with theHarvester |
| **Primary Tool** | theHarvester |
| **Security Domain** | Footprinting & Passive Reconnaissance |
| **Target Domain** | microsoft.com |
| **Tasks Completed** | 2 |
| **Testing Approach** | Passive Reconnaissance |
| **Methodology** | Authorized and responsible security research |

---

## 🎯 Objectives

The objectives of this module were to:

- Learn the basic usage of **theHarvester**.
- Perform passive reconnaissance against an assigned domain.
- Identify publicly available email addresses.
- Identify publicly available subdomains and hostnames.
- Understand how different search sources can affect reconnaissance results.
- Compare reconnaissance results obtained using different sources and search limits.
- Document the execution and results using screenshots.

---

# 🛠️ Tasks Performed

## Task 1: Reconnaissance Using Baidu

The first task used theHarvester with the **Baidu** search source and a result limit of **1000**.

### Command Used

```bash
theHarvester -d microsoft.com -l 1000 -b baidu
```

### Purpose

This command was used to perform passive reconnaissance against the assigned domain and collect publicly available information indexed through the selected source.

### Evidence

- `img/theHarvester_task_01.png`
- `img/theHarvester-01.png`

---

## Task 2: Reconnaissance Using All Sources

The second task used theHarvester with **all available supported sources** and a result limit of **50**.

### Command Used

```bash
theHarvester -d microsoft.com -l 50 -b all
```

### Purpose

This task demonstrates how using multiple passive information sources can produce a broader reconnaissance dataset.

### Evidence

- `img/theHarvester_task_02.png`
- `img/theHarvester_task_02_output.png`

---

# 📂 Repository Structure

```text
WK2-PM4-theHarvester/
├── img/
│   ├── theHarvester-01.png
│   ├── theHarvester_task_01.png
│   ├── theHarvester_task_02.png
│   └── theHarvester_task_02_output.png
└── README.md
```

---

# 🔍 Methodology

The module followed a passive reconnaissance methodology:

1. Identify the assigned target domain.
2. Execute theHarvester using the specified search source.
3. Set the required result limit.
4. Observe publicly available reconnaissance information.
5. Repeat the process using the required source configuration.
6. Capture screenshots as evidence.
7. Document the activities and observations.

No exploitation or unauthorized access was performed.

---

# 🛡️ Security & Ethical Considerations

The activities in this module were performed as part of an educational cybersecurity training exercise.

The following principles were followed:

- Reconnaissance was performed only against the assigned domain.
- No attempt was made to gain unauthorized access.
- No passwords or authentication mechanisms were bypassed.
- No exploitation was performed.
- No denial-of-service activity was performed.
- Collected information was used only for the assigned educational exercise.
- Results may vary because public search engines and reconnaissance sources change over time.

---

# 📚 Learning Outcomes

After completing this module, the following concepts were practiced:

- Passive reconnaissance
- Domain footprinting
- Email enumeration
- Subdomain discovery
- Search-engine-based reconnaissance
- theHarvester command-line usage
- Source selection and result limits
- Evidence collection and documentation
- Responsible security research

---

# 📸 Evidence

The `img/` directory contains screenshots documenting the execution of both assigned theHarvester tasks.

These screenshots provide evidence of:

- Tool execution
- Target configuration
- Search-source configuration
- Result limits
- Reconnaissance output

---

# ⚠️ Disclaimer

This project was completed as part of an authorized cybersecurity training exercise. The techniques demonstrated are intended for educational and legitimate security-testing purposes only.

Unauthorized reconnaissance or information gathering against systems or organizations without permission may violate applicable laws, policies, or terms of service.

---

# ✅ Conclusion

W2-PM4 provided practical experience with **theHarvester** for passive reconnaissance and domain footprinting.

The module demonstrated how different information sources and search limits can be used to gather publicly available reconnaissance information. The completed tasks and screenshots have been documented as evidence for the Week 2 cybersecurity internship project.

---

## 👤 Author

**Ishanya Jha**  
Cybersecurity & Ethical Hacking Intern  
**B083-Networkwalks**  
Networkwalks Cybersecurity Internship  
Week 2 Project

---

**End of README**
