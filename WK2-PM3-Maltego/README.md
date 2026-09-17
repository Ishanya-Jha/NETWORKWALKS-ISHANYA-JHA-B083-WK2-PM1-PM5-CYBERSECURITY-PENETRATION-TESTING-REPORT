# 🔎 W2-PM3: Footprinting with Maltego

![Cybersecurity](https://img.shields.io/badge/Domain-Cybersecurity-red)
![Module](https://img.shields.io/badge/Week%202-Project%20Module%203-blue)
![Topic](https://img.shields.io/badge/Topic-Maltego-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 🎯 Objective

The objective of this module was to learn the basics of **Maltego** and use it for footprinting and reconnaissance.

The module focused on installing and configuring Maltego and performing email-address reconnaissance related to the authorized target domain:

`networkwalks.com`

---

## 📌 Project Information

| Category | Details |
|---|---|
| 🎓 **Program** | Cybersecurity Internship |
| 🏢 **Organization** | NetworkWalks |
| 📅 **Training Week** | Week 2 |
| 🧪 **Project Module** | W2-PM3 |
| 🔎 **Module Title** | Footprinting with Maltego |
| 🛠️ **Primary Tool** | Maltego |
| 🔍 **Security Domain** | Footprinting & Passive Reconnaissance |
| 📚 **Tasks Completed** | 2 |
| 📊 **Evidence Collected** | Screenshots, video demonstration, and transform output |
| 🔐 **Testing Approach** | Passive reconnaissance |
| ⚖️ **Methodology** | Authorized and responsible security research |

---

## 🛠️ Task 1: Download & Install Maltego

The first task involved downloading, installing, and configuring **Maltego** on a Windows computer.

The following activities were completed:

- 💻 Downloaded Maltego
- ⚙️ Installed the Maltego application
- 🔧 Completed the initial configuration
- 👤 Created and configured a Maltego account
- 🌐 Logged into Maltego and accessed the main interface
- 🔎 Added a **Domain** entity to the Maltego graph

### 📸 Task 1 Evidence

<p align="center">
  <img src="./screenshots/screenshot-Task01.png" alt="Maltego Task 1 Screenshot" width="900">
</p>

---

## 📧 Task 2: Find Email Addresses Related to the Target Domain

The second task involved using Maltego to identify email-address information associated with the authorized target domain:

`networkwalks.com`

The domain was added as the starting entity and relevant Maltego transforms were executed.

### 🔍 Transforms Used

The following transforms were executed:

- `Utilities → To Email Addresses [Search Engine]`
- `Utilities → To Email Addresses [PGP]`
- `Utilities → To Emails @domain [Search Engine]`

The transforms were executed against the `networkwalks.com` domain entity.

### 📸 Task 2 Evidence

<p align="center">
  <img src="./screenshots/screenshot-Task02.png" alt="Maltego Task 2 Screenshot" width="900">
</p>

### 📄 Transform Output

The collected Maltego transform logs are available here:

📄 **[View Task 2 Output](./Task02-output.txt)**

---

## 🎥 Video Demonstration

A demonstration of the PM3 Maltego workflow and activities is included below:

▶️ **[Watch PM3 Maltego Demonstration](./PM3-maltegp.mp4)**

The video provides additional evidence of the practical work performed during this module.

---

## 🔐 Security Relevance

Maltego can assist security professionals during the reconnaissance and information-gathering phase of an assessment.

This module demonstrated how:

- 🔎 Domain entities can be used as starting points for reconnaissance.
- 📧 Email-related information can be investigated using transforms.
- 🧩 Different data sources can be queried through Maltego transforms.
- 🌐 Publicly available information can contribute to an organization's digital footprint.
- 📝 Reconnaissance findings can be collected and documented in a structured manner.

---

## 🎓 Learning Outcomes

Through this module, I learned:

- 🛠️ How to install and configure Maltego.
- 🔎 How to create and use a Domain entity.
- 🧩 How Maltego transforms work.
- 📧 How email-related reconnaissance can be performed.
- 📊 How reconnaissance results can be collected and documented.
- 🔐 The importance of performing reconnaissance only within an authorized scope.
- 📝 How to maintain technical evidence using screenshots, logs, and demonstration videos.

---

## ⚖️ Ethical Considerations

The activities in this module were performed as part of an authorized cybersecurity internship exercise.

- ✅ Reconnaissance was performed within the assigned training scope.
- 🔐 The target domain was used with the required permission for the exercise.
- 🚫 No attempt was made to bypass authentication or access restricted systems.
- 🚫 No exploitation or unauthorized access was performed.
- 📹 Evidence was collected for educational and documentation purposes.
- 🛡️ Real-world reconnaissance should only be performed with explicit authorization from the system or resource owner.

---

## 📁 Evidence Structure

```text
W2-PM3-Maltego/
│
├── README.md
├── PM3-maltegp.mp4
│
├── screenshots/
│   ├── screenshot-Task01.png
│   └── screenshot-Task02.png
│
└── Task02-output.txt
```

---

## 🏁 Conclusion

This module provided practical experience with **Maltego** for footprinting and passive reconnaissance.

The activities covered Maltego installation and configuration, creation of a domain entity, execution of email-related transforms, and documentation of the resulting activity through screenshots, logs, and a demonstration video.

The exercise improved practical understanding of how graphical reconnaissance tools can be used to organize and investigate publicly available information during an authorized security assessment.
