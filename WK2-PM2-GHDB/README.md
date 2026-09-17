# W2-PM2: Footprinting & Reconnaissance Attacks with GHDB

## Objective

The objective of this module was to understand how Google Hacking Database (GHDB) search operators and Google dorks can be used during footprinting and reconnaissance to identify publicly indexed resources.

---

## Task 1: Find 10x Live Vulnerable Security Camera Links

The task was performed using GHDB/Google dorks to identify publicly indexed webcam-related resources.

> **Note:** Live-camera screenshots were not included to avoid capturing or redistributing identifiable individuals or sensitive surveillance content. No authentication bypass or unauthorized access was attempted.

### Results

| No. | Link | Relevant Dork | Username / Password (if any) |
|---:|---|---|---|
| 1 | http://122.116.41.8:8080/ | `intitle:"webcamXP" inurl:8080` | --- |
| 2 | https://www.lmc.edu/webcam.htm | `intitle:"Webcam" inurl:WebCam.htm` | --- |
| 3 | https://tuwebcam.towson.edu/index.html | `intitle:"Webcam" inurl:WebCam.htm` | --- |
| 4 | https://www.nps.gov/subjects/air/webcams.htm?site=dena | `intitle:"Webcam" inurl:WebCam.htm` | --- |
| 5 | https://pixelheal.bandcamp.com/album/intitle-toshiba-network-camera-user-login | `intitle:"Toshiba Network Camera"` | Cookies/login required |
| 6 | http://99.114.240.169:8080/ | `intitle:"Webcam" inurl:WebCam.htm` | --- |
| 7 | https://www.shodan.io/search?query=webcam | `intitle:"Webcam" inurl:WebCam.htm` | Login required |
| 8 | https://www.skylinewebcams.com/webcam/italia/lazio/roma/piazza-di-spagna.html | `inurl:webcam site:skylinewebcams.com inurl:roma` | --- |
| 9 | https://www.skylinewebcams.com/webcam/italia/lazio/roma/fontana-di-trevi.html | `inurl:webcam site:skylinewebcams.com inurl:roma` | --- |
| 10 | https://www.skylinewebcams.com/en/webcam/italia/lazio/roma/roma-colosseo.html | `inurl:webcam site:skylinewebcams.com inurl:roma` | --- |

### Observation

The results demonstrate how search-engine indexing can expose webcam-related resources and public camera pages. The activity was limited to passive reconnaissance and documentation. No attempt was made to bypass authentication, obtain credentials, or access restricted systems.

---

## Task 2: Find 10x Listings Containing Downloadable Mathematics Ebooks in PDF Format

The task was performed using the following Google dork:

`intitle:index.of "parent directory" mathematics pdf`

### Results

| No. | Link | Relevant Dork | Username / Password (if any) |
|---:|---|---|---|
| 1 | http://inis.jinr.ru/sl/vol2/Mathematics/Math.Encyclopedia/Pdf/ | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 2 | http://erewhon.superkuh.com/library/Math/ | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 3 | https://sajaipuriacollege.ac.in/pdf/pdf/MATHEMATICS/ | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 4 | https://www.unm.edu/~megrad/Math/ | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 5 | https://www.netlib.org/math/docpdf/ | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 6 | https://www.wvfa.org/pdf/projectLearningTree/ | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 7 | https://ochicken.net/library/Mathematics/ | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 8 | https://education.giakonda.org.uk/Maths/?SD | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 9 | https://www.learn-fo.com/FYUG%20mathematics%20solutions/?SD | `intitle:index.of "parent directory" mathematics pdf` | --- |
| 10 | https://math.dartmouth.edu/~carlp/PDF/ | `intitle:index.of "parent directory" mathematics pdf` | --- |

### Observation

The search results demonstrate how directory indexing and search-engine operators can be used to locate publicly indexed mathematical PDF resources. This illustrates the importance of proper web-server configuration and access controls to prevent unintended exposure of files and directories.

---

## Security Relevance

GHDB and Google dorks are useful during the reconnaissance phase of security assessments because they can reveal information that has been indexed by search engines.

Key observations include:

- Publicly indexed resources can expose information without directly attacking a server.
- Misconfigured directory listings may reveal files and documents.
- Search-engine indexing can expose unintended web resources.
- Security assessments should distinguish between publicly accessible information and authorized access.
- Authentication controls should never be bypassed during reconnaissance activities.

---

## Evidence

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

## Conclusion

This module demonstrated the use of Google Hacking Database techniques and Google dorks for passive footprinting and reconnaissance. The activities highlighted how publicly indexed information can reveal web resources and documents, while also demonstrating the importance of responsible and authorized security testing.
