# Network Security Scanner Scraper
A fast, flexible network security scanner built to automate SSL checks, IP discovery, and deep reconnaissance across large cloud and enterprise infrastructures. This tool helps uncover hidden services, bypass protective layers, and gather actionable intelligence for enhanced security analysis.


<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/scraper.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/Bitbash333" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20BitBash%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:sale@bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-sale@bitbash.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>




<p align="center" style="font-weight:600; margin-top:8px; margin-bottom:8px;">
  Created by Bitbash, built to showcase our approach to Scraping and Automation!<br>
  If you are looking for <strong>network-security-scanner</strong> you've just found your team — Let’s Chat. 👆👆
</p>


## Introduction
The Network Security Scanner Scraper identifies real IPs, scans entire IP ranges, evaluates SSL certificates, and analyzes endpoints to reveal otherwise undiscoverable infrastructure details. It solves the challenge of expanding attack surfaces across cloud networks by offering high-speed scanning and structured insights.

### Deep Infrastructure Intelligence
- Scan millions of IPs efficiently using Masscan or direct IP lists.
- Discover real server IPs behind Web Application Firewalls.
- Collect SSL metadata, endpoints, redirections, and response headers.
- Identify vulnerabilities, misconfigurations, and exposed services.
- Extend reconnaissance for cloud environments such as AWS and GCP.

## Features
| Feature | Description |
|---------|-------------|
| Masscan-Based IP Scanning | Enables ultra-fast scanning of large IP ranges using configurable ports and rate limits. |
| SSL Certificate Analysis | Extracts certificate info, domains, validation details, and server behavior. |
| WAF Bypass Detection | Helps uncover origin IPs hidden behind WAF layers. |
| Subdomain & Endpoint Discovery | Reveals extended attack surface areas and potential weak points. |
| Proxy Support | Allows region-based scanning and improved anonymity. |
| Structured Export Formats | Outputs results in JSON, XML, CSV, Excel, or HTML. |
| Result Limiting | Users can define max result count for workload control. |

---

## What Data This Scraper Extracts
| Field Name | Field Description |
|------------|-------------------|
| title | Parsed page or service title associated with the scanned IP. |
| redirected_url | URL to which the request was redirected, if any. |
| request | Full request URL used during the scan. |
| port | Port scanned on the target IP. |
| ip | The discovered or scanned IP address. |
| domain | Domain or wildcard domain resolved from the server. |
| response_text | Body content returned from the scanned endpoint. |
| response_headers | Complete set of response headers extracted from the server. |

---

## Example Output

    [
        {
            "title": "",
            "redirected_url": "",
            "request": "https://3.94.15.209:443",
            "port": "443",
            "ip": "3.94.15.209",
            "domain": "*.execute-api.us-east-1.amazonaws.com",
            "response_text": "{\"message\":\"Forbidden\"}",
            "response_headers": {
                "Date": "Mon, 07 Oct 2024 23:21:14 GMT",
                "Content-Type": "application/json",
                "Content-Length": "23",
                "Connection": "keep-alive",
                "x-amzn-RequestId": "c1f2ff47-007d-481e-9a76-02f2bd2c21bc",
                "x-amzn-ErrorType": "ForbiddenException",
                "x-amz-apigw-id": "fTX0oGxcoAMEawg="
            }
        }
    ]

---

## Directory Structure Tree

    Network Security Scanner /
    ├── src/
    │   ├── main.py
    │   ├── masscan/
    │   │   ├── masscan_runner.py
    │   │   └── parser.py
    │   ├── ssl_analysis/
    │   │   ├── ssl_checker.py
    │   │   └── cert_utils.py
    │   ├── network/
    │   │   ├── request_handler.py
    │   │   └── endpoint_discovery.py
    │   ├── outputs/
    │   │   ├── exporter_json.py
    │   │   ├── exporter_csv.py
    │   │   └── exporter_excel.py
    │   └── config/
    │       └── settings.example.json
    ├── data/
    │   ├── cidr_input.sample.txt
    │   └── example_output.json
    ├── requirements.txt
    └── README.md

---

## Use Cases
- **Security researchers** map hidden infrastructure to identify weaknesses in cloud networks.
- **Bug bounty hunters** expand their reconnaissance surface to locate real server IPs and exploitable services.
- **Penetration testers** uncover endpoints, misconfigurations, and unprotected assets for deeper testing.
- **Blue teams** analyze exposure levels and monitor potential vulnerabilities proactively.
- **Network administrators** validate SSL configurations, service behavior, and infrastructure hygiene.

---

## FAQs

**Does the scanner support both IP ranges and individual IPs?**
Yes — users can choose to scan CIDR ranges with Masscan or provide IP lists directly to skip fast scanning.

**Is proxy usage optional?**
Proxies can be configured for anonymity or region-limited testing, but they are not required for basic scans.

**Can I limit how many results the scanner returns?**
Yes — the `max_results` parameter allows fine control over how many findings are collected.

**What ports can be scanned?**
Any port can be specified. Defaults to 443, but ranges such as `80`, `443`, or `0–65535` are supported.

---

### Performance Benchmarks and Results

**Primary Metric:** Capable of scanning tens of thousands of IPs per minute using optimized Masscan configurations.

**Reliability Metric:** Consistently achieves over 98% response retrieval on stable networks, even under high throughput.

**Efficiency Metric:** Low compute overhead through asynchronous request handling and throttled packet emission.

**Quality Metric:** Produces highly complete datasets, including headers, SSL metadata, and origin IP insights with strong accuracy.


<p align="center">
<a href="https://calendar.app.google/74kEaAQ5LWbM8CQNA" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
  <a href="https://www.youtube.com/@bitbash-demos/videos" target="_blank">
    <img src="https://img.shields.io/badge/🎥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
  </a>
</p>
<table>
  <tr>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/MLkvGB8ZZIk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review1.gif" alt="Review 1" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash is a top-tier automation partner, innovative, reliable, and dedicated to delivering real results every time."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Nathan Pennington
        <br><span style="color:#888;">Marketer</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/8-tw8Omw9qk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review2.gif" alt="Review 2" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash delivers outstanding quality, speed, and professionalism, truly a team you can rely on."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Eliza
        <br><span style="color:#888;">SEO Affiliate Expert</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/m-dRE1dj5-k?si=5kZNVlKsGUhg5Xtx" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review3.gif" alt="Review 3" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Exceptional results, clear communication, and flawless delivery. <br>Bitbash nailed it."
      </p>
      <p style="margin:1px 0 0; font-weight:600;">Syed
        <br><span style="color:#888;">Digital Strategist</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
  </tr>
</table>
