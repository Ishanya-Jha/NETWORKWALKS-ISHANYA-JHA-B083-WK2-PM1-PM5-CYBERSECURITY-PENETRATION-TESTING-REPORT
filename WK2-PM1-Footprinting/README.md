W2-PM1: Footprinting & Reconnaissance

Overview

This module demonstrates footprinting and reconnaissance techniques using multiple Kali Linux tools against "networkwalks.com".

The objective was to collect publicly accessible information about the target domain, including:

- Domain registration information
- Web technologies and software
- DNS resolution
- HTTP response headers
- Web Application Firewall (WAF) information
- DNS records and service infrastructure

The results documented below are based on the actual command outputs collected during the practical exercises.

---

Target

Target Domain: "networkwalks.com"

Primary IPv4 Address: "192.232.216.135"

---

Task 1: WHOIS

Command

whois networkwalks.com

Purpose

WHOIS was used to obtain publicly available domain registration and registrar information.

Findings

Information| Result
Domain| "NETWORKWALKS.COM"
Registrar| GoDaddy.com, LLC
Registrar IANA ID| 146
Creation Date| 2019-11-06
Updated Date| 2025-11-12
Registry Expiry Date| 2027-11-06
Name Server| "NS6135.HOSTGATOR.COM"
Name Server| "NS6136.HOSTGATOR.COM"
DNSSEC| Unsigned

The WHOIS output also identified GoDaddy's WHOIS service and included standard domain-status information such as "clientDeleteProhibited", "clientRenewProhibited", "clientTransferProhibited", and "clientUpdateProhibited".

Observation

The WHOIS query exposed publicly available registration metadata, registrar information, registration dates, domain status values, and authoritative name servers.

No specific registrant/owner identity was present in the collected output.

The WHOIS server also reported that the service is being retired in favor of RDAP and displayed a rate-limit message after the query.

Screenshot

"WHOIS Screenshot" (Task-1-WHOIS/screenshot_whois.png)

Raw Output

"View WHOIS command output" (Task-1-WHOIS/whois_networkwalks.txt)

---

Task 2: WhatWeb

Command

whatweb networkwalks.com

Purpose

WhatWeb was used to identify publicly observable web technologies, frameworks, server software, and application components.

Findings

The HTTP request produced a "301 Moved Permanently" response that redirected to HTTPS.

The HTTPS endpoint returned "200 OK".

Technology / Information| Result
Web Server| Apache
CMS| WordPress 7.1
WordPress Download Manager| 3.3.58
Bootstrap| 7.1
jQuery| 3.7.1
Google Tag Manager| Detected
IP Address| "192.232.216.135"
Website Title| Networkwalks Academy
Public Email| "info@networkwalks.com"
HTML5| Detected
Open Graph Protocol| Detected
Cookie| "__wpdm_client"
HTTP → HTTPS| 301 Redirect

Observation

WhatWeb identified the website's web server, CMS, software versions, JavaScript library, and other publicly observable components.

This information provides a basic technology profile of the website and can help security professionals understand the externally visible technology stack.

Technology or version disclosure alone does not establish that a vulnerability exists.

Screenshot

"WhatWeb Screenshot" (Task-2-WhatWeb/screenshot_WhatWeb.png)

Raw Output

"View WhatWeb command output" (Task-2-WhatWeb/whatweb_networkwalks.txt)

---

Task 3: NSLookup

Command

nslookup networkwalks.com

Purpose

NSLookup was used to resolve the domain name and identify its associated IPv4 address.

Findings

Information| Result
DNS Server| "10.198.219.151"
DNS Server Port| "53"
Response Type| Non-authoritative answer
Domain| "networkwalks.com"
IPv4 Address| "192.232.216.135"

Observation

The domain successfully resolved to the IPv4 address "192.232.216.135".

The response was identified as non-authoritative because the result was returned by the configured DNS resolver rather than directly from an authoritative DNS server.

Screenshot

"NSLookup Screenshot" (Task-3-NSLookup/screenshot_NSLookup.png)

Raw Output

"View NSLookup command output" (Task-3-NSLookup/nslookup_networkwalks.txt)

---

Task 4: cURL

Command

curl -I https://networkwalks.com

Purpose

cURL was used to inspect the HTTP response headers returned by the HTTPS web server.

Findings

The server returned:

HTTP/2 200

Important headers observed included:

Header| Observed Value / Information
"server"| Apache
"content-type"| "text/html; charset=UTF-8"
"referrer-policy"| "no-referrer-when-downgrade"
"x-endurance-cache-level"| "0"
"x-nginx-cache"| WordPress
"permissions-policy"| Private State Token policies
"link"| WordPress REST API references
"set-cookie"| "__wpdm_client" cookie with "Secure" and "HttpOnly"

The "Link" header referenced the WordPress REST API:

/wp-json/

It also referenced a WordPress REST API page endpoint.

Observation

The HTTP response headers revealed information about the web server, content type, caching configuration, security-related policies, cookies, and WordPress API functionality.

These headers provide useful reconnaissance information about the externally visible HTTP configuration.

The cookie value from the original command output should not be reproduced in public documentation. If the screenshot is uploaded to a public repository, the cookie value should be redacted.

Screenshot

"cURL Screenshot" (Task-4-cURL/screenshot_cURL.png)

Raw Output

"View cURL command output" (Task-4-cURL/curl_networkwalks.txt)

---

Task 5: Wafw00f

Command

wafw00f networkwalks.com

Purpose

Wafw00f was used to determine whether a Web Application Firewall was protecting the website.

Findings

Information| Result
Wafw00f Version| 2.4.2
Target| "https://networkwalks.com"
WAF Detected| ModSecurity (SpiderLabs)
Number of Requests| 2

Observation

Wafw00f identified ModSecurity (SpiderLabs) as the Web Application Firewall protecting the website.

A WAF provides an additional defensive layer for web applications by inspecting and filtering HTTP requests.

The detection of a WAF does not itself indicate the presence or absence of a vulnerability.

Screenshot

"Wafw00f Screenshot" (Task-5-Wafw00f/screenshot_WafW00f.png)

Raw Output

"View Wafw00f command output" (Task-5-Wafw00f/wafw00f_networkwalks.txt)

---

Task 6: DNSRecon

Command

dnsrecon -d networkwalks.com

Purpose

DNSRecon was used to enumerate publicly accessible DNS records associated with the target domain.

Findings

SOA Record

ns6135.hostgator.com
50.87.144.87

NS Records

ns6136.hostgator.com → 192.232.216.131
ns6135.hostgator.com → 50.87.144.87

BIND Version

DNSRecon reported the following BIND version information for both name servers:

9.16.23-RH

MX Record

mail.networkwalks.com → 192.232.216.135

A Record

networkwalks.com → 192.232.216.135

TXT Records

A Google site-verification record was identified.

An SPF record was also identified:

v=spf1 +a +mx +ip4:50.87.144.87 +include:websitewelcome.com ~all

SRV Records

DNSRecon identified "_autodiscover._tcp.networkwalks.com" service records pointing to:

cpanelemaildiscovery.cpanel.net

The returned records used port:

443

DNSRecon reported 8 SRV records for the autodiscovery service.

DNSSEC

DNSRecon reported:

ERROR No answer for DNSSEC query for networkwalks.com

Observation

DNSRecon revealed publicly accessible information about the domain's DNS infrastructure, including authoritative name servers, web hosting, mail infrastructure, TXT records, SPF configuration, and email autodiscovery services.

The BIND version reported by DNSRecon represents version disclosure observed during enumeration. It was not treated as evidence of a vulnerability.

Screenshot

"DNSRecon Screenshot" (Task-6-DNSRecon/screenshot_DNSRecon.png)

Raw Output

"View DNSRecon command output" (Task-6-DNSRecon/dnsrecon_networkwalks.txt)

---

Overall Reconnaissance Summary

The six reconnaissance activities produced the following results:

Category| Finding
Domain| "networkwalks.com"
IPv4 Address| "192.232.216.135"
Registrar| GoDaddy.com, LLC
Name Servers| "NS6135.HOSTGATOR.COM", "NS6136.HOSTGATOR.COM"
Web Server| Apache
CMS| WordPress 7.1
WordPress Download Manager| 3.3.58
jQuery| 3.7.1
WAF| ModSecurity (SpiderLabs)
Mail Host| "mail.networkwalks.com"
DNSSEC| No DNSSEC answer reported
SPF| Published
Email Autodiscovery| "_autodiscover._tcp.networkwalks.com"
HTTPS Status| HTTP/2 "200 OK"

---

Security Relevance

The reconnaissance exercise demonstrated how publicly accessible information can reveal details about an organization's external infrastructure.

The collected information included:

- Domain registration information
- DNS name servers
- IP addressing information
- Web server technology
- CMS and software versions
- HTTP response headers
- WAF technology
- Mail infrastructure
- SPF configuration
- TXT records
- Email autodiscovery services

This type of information can assist security professionals in building an initial understanding of an organization's external attack surface during an authorized assessment.

The findings are reconnaissance observations and should not automatically be interpreted as security vulnerabilities.

---

Evidence Structure

All screenshots and command outputs are stored with their respective tasks:

W2-PM1-Footprinting/
│
├── Task-1-WHOIS/
│   ├── screenshot_whois.png
│   └── whois_networkwalks.txt
│
├── Task-2-WhatWeb/
│   ├── screenshot_WhatWeb.png
│   └── whatweb_networkwalks.txt
│
├── Task-3-NSLookup/
│   ├── screenshot_NSLookup.png
│   └── nslookup_networkwalks.txt
│
├── Task-4-cURL/
│   ├── screenshot_cURL.png
│   └── curl_networkwalks.txt
│
├── Task-5-Wafw00f/
│   ├── screenshot_WafW00f.png
│   └── wafw00f_networkwalks.txt
│
├── Task-6-DNSRecon/
│   ├── screenshot_DNSRecon.png
│   └── dnsrecon_networkwalks.txt
│
└── README.md

---

Conclusion

W2-PM1 provided practical experience with six commonly used reconnaissance tools in Kali Linux.

WHOIS provided domain registration information, WhatWeb identified web technologies, NSLookup resolved the domain, cURL examined HTTP headers, Wafw00f detected the web application firewall, and DNSRecon enumerated publicly accessible DNS records.

The collected results demonstrate how multiple reconnaissance techniques can be combined to build a structured technical profile of a web domain without performing exploitation or unauthorized access.
