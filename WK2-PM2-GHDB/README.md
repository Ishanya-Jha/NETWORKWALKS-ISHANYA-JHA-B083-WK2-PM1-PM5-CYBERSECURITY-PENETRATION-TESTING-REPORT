# 🔎 W2-PM2: Footprinting & Reconnaissance Attacks with GHDB

![Cybersecurity](https://img.shields.io/badge/Domain-Cybersecurity-red)
![Module](https://img.shields.io/badge/Week%202-Project%20Module%202-blue)
![Topic](https://img.shields.io/badge/Topic-GHDB%20Reconnaissance-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 🎯 Objective

The objective of this module was to understand how Google Hacking Database (GHDB) search operators and Google dorks can be used during footprinting and reconnaissance to identify publicly indexed resources.

---

## 📹 Task 1: Find 10x Live Vulnerable Security Camera Links

The task was performed using GHDB/Google dorks to identify publicly indexed webcam-related resources.

> ⚠️ **Security Note:** Specific camera URLs and access-related information are not published in this README to avoid redistributing potentially sensitive surveillance resources. No authentication bypass or unauthorized access was attempted.

### 📊 Results

| No. | Resource Type | Relevant Dork | Authentication |
|---:|---|---|---|
| 1 | Webcam-related resource | `intitle:"webcamXP" inurl:8080` | --- |
| 2 | Webcam-related resource | `intitle:"Webcam" inurl:WebCam.htm` | --- |
| 3 | Webcam-related resource | `intitle:"Webcam" inurl:WebCam.htm` | --- |
| 4 | Webcam-related resource | `intitle:"Webcam" inurl:WebCam.htm` | --- |
| 5 | Toshiba network camera-related resource | `intitle:"Toshiba Network Camera"` | Cookies/login required |
| 6 | Webcam-related resource | `intitle:"Webcam" inurl:WebCam.htm` | --- |
| 7 | Webcam search resource | `intitle:"Webcam" inurl:WebCam.htm` | Login required |
| 8 | Public webcam resource | `inurl:webcam site:skylinewebcams.com inurl:roma` | --- |
| 9 | Public webcam resource | `inurl:webcam site:skylinewebcams.com inurl:roma` | --- |
| 10 | Public webcam resource | `inurl:webcam site:skylinewebcams.com inurl:roma` | --- |

### 🔍 Observation

The results demonstrate how search-engine indexing can expose webcam-related resources and public camera pages. The activity was limited to passive reconnaissance and documentation. No attempt was made to bypass authentication, obtain credentials, or access restricted systems.

Detailed results are maintained separately in the Task 1 evidence file.

---

## 📚 Task 2: Find 10x Listings Containing Downloadable Mathematics Ebooks in PDF Format

The task was performed using the following Google dork:

```text
intitle:index.of "parent directory" mathematics pdf
```

### 📊 Results

| No. | Resource Type | Relevant Dork | Authentication |
|---:|---|---|---|
| 1 | Mathematics PDF directory | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 2 | Mathematics PDF directory | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 3 | Mathematics PDF directory | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 4 | Mathematics PDF directory | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 5 | Mathematics PDF directory | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 6 | Mathematics PDF directory | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 7 | Mathematics PDF directory | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 8 | Mathematics PDF directory | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 9 | Mathematics PDF directory | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 10 | Mathematics PDF directory | `intitle:index.of "parent directory" mathematics pdf` | --- |

### 🔍 Observation

The search results demonstrate how directory indexing and search-engine operators can be used to locate publicly indexed mathematical PDF resources. This illustrates the importance of proper web-server configuration and access controls to prevent unintended exposure of files and directories.

Detailed URLs and collected results are maintained separately in the Task 2 evidence file.

---

## 🛡️ Security Relevance

GHDB and Google dorks are useful during the reconnaissance phase of security assessments because they can reveal information that has been indexed by search engines.

Key observations include:

- 🌐 Publicly indexed resources can expose information without directly attacking a server.
- 📂 Misconfigured directory listings may reveal files and documents.
- 🔎 Search-engine indexing can expose unintended web resources.
- 🔐 Security assessments should distinguish between publicly accessible information and authorized access.
- 🚫 Authentication controls should never be bypassed during reconnaissance activities.
- 📝 Sensitive reconnaissance findings should be handled carefully when publishing cybersecurity project documentation.

---

## 🎓 Learning Outcomes

Through this module, I learned:

- 🔎 How Google Hacking Database (GHDB) techniques can be used for passive reconnaissance.
- 🧩 How Google dorks can help identify publicly indexed web resources.
- 🛠️ How search operators such as `intitle`, `inurl`, and `site` can narrow reconnaissance results.
- 📂 How directory indexing can unintentionally expose files and documents.
- 🌐 How publicly indexed information can provide useful reconnaissance data without directly attacking a target.
- 🔐 The importance of identifying publicly accessible information without attempting unauthorized access.
- 📝 How to document reconnaissance findings in a structured and professional manner.
- 🛡️ The importance of protecting sensitive information when publishing cybersecurity project results on public repositories.
- ⚖️ How responsible reconnaissance supports security assessments and helps identify potential information-exposure risks.

---

## 📁 Evidence

The supporting evidence for this module is stored in the respective task directories:

```text
W2-PM2-GHDB/
│
├── README.md
├── W2-PM2-GHDB-Report.pdf
│
├── Task-1-GHDB/
│   ├── ghdb_screenshot.png
│   └── ghdb_live_cam_result.txt
│
└── Task-2-Mathematics-PDF/
    ├── screenshot_01.png
    ├── screenshot_02.png
    ├── screenshot_03.png
    ├── ...
    ├── screenshot_10.png
    └── mathematics_pdf_results.txt
```

---

## ⚖️ Ethical Considerations

The reconnaissance activities in this module were performed for educational and authorized cybersecurity training purposes.

- ✅ Only publicly indexed information was considered during the reconnaissance process.
- 🚫 No attempt was made to bypass authentication or access restricted resources.
- 🔑 No credentials were obtained, tested, or used to gain unauthorized access.
- 📹 Live surveillance content was not captured or redistributed in the project documentation.
- 🔒 Sensitive information was excluded from the public README to reduce the risk of unintended disclosure.
- 📋 The reconnaissance process was limited to the scope and requirements of the assigned internship module.
- 🎓 Findings were documented for educational and security-awareness purposes rather than for unauthorized access or exploitation.
- 🛡️ Any real-world security testing should be performed only with explicit permission from the system or resource owner.

---

## 🏁 Conclusion

This module demonstrated the use of Google Hacking Database techniques and Google dorks for passive footprinting and reconnaissance.

The activities highlighted how publicly indexed information can reveal web resources and documents while demonstrating the importance of responsible, authorized, and ethical security testing.

The module also provided practical experience in using search operators, documenting reconnaissance findings, protecting sensitive information, and understanding the security implications of publicly indexed resources.

---

## 📌 Project Information

| Category | Details |
|---|---|
| 📚 Program | Cybersecurity Internship |
| 📅 Week | Week 2 |
| 🧪 Module | W2-PM2 |
| 🔎 Topic | Footprinting & Reconnaissance with GHDB |
| 🛠️ Primary Technique | Google Dorking / GHDB |
| 📊 Tasks Completed | 2 |
| 📁 Evidence | Screenshots + Text Results + PDF Report |
| 🔐 Testing Type | Passive Reconnaissance |
| ⚖️ Approach | Authorized & Ethical |
