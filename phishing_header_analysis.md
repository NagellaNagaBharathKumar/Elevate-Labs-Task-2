# Phishing Email Header Analysis

This section analyzes a sample email header from a suspected phishing email pretending to be from PayPal.

---

## Sample Header (Simulated)

```
Return-Path: <support@paypal-account-secure.com>
Received: from suspicioushost123.fakeisp.net (unknown [203.0.113.45])
    by mail.yourdomain.com (Postfix) with ESMTPS id 9AC3D23E91
    for <you@example.com>; Tue, 5 Aug 2025 10:45:33 +0530 (IST)
Received-SPF: Fail (mail.yourdomain.com: domain of paypal-account-secure.com does not designate 203.0.113.45 as permitted sender)
Authentication-Results: mail.yourdomain.com;
    spf=fail smtp.mailfrom=support@paypal-account-secure.com;
    dkim=none (message not signed)
    dmarc=fail (p=NONE dis=NONE) header.from=paypal-account-secure.com
Message-ID: <20250805101533.support@paypal-account-secure.com>
Date: Tue, 5 Aug 2025 10:45:33 +0530
From: "PayPal Security" <support@paypal-account-secure.com>
To: <you@example.com>
Subject: [Action Required] Suspicious Activity Detected on Your Account
MIME-Version: 1.0
Content-Type: text/html; charset=UTF-8
Content-Transfer-Encoding: 7bit
X-Mailer: PHP/7.4.3
X-Priority: 1 (High)
```

---

## Header Red Flags and Indicators

| Header Field | Indicator | Description |
|--------------|-----------|-------------|
| Return-Path | Spoofed | Not a legitimate PayPal domain. |
| Received | Suspicious origin | Sent from `fakeisp.net`, not PayPal's mail servers. |
| SPF | **Fail** | Indicates the sender IP is not authorized by the domain. |
| DKIM | **None** | No digital signature to verify sender identity. |
| DMARC | **Fail** | Fails domain-based authentication checks. |
| From | Lookalike domain | Domain mimics a trusted brand (paypal-account-secure.com). |
| X-Mailer | PHP script | Commonly used in manually crafted phishing emails. |
| X-Priority | High | Attempts to create urgency. |

---

## Summary

This header contains multiple signs of email spoofing and phishing:

- SPF, DKIM, and DMARC all **fail**, indicating **no authentication**.
- **Return-Path and From address** are not trusted or verified domains.
- Server IP and domain (`fakeisp.net`) are **unrelated to PayPal**.
- Email crafted to **appear urgent and mimic PayPal security warnings**.

⚠️ Always inspect full headers of suspicious emails using tools like:
- [MXToolbox Email Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx)
- [Google Admin Toolbox](https://toolbox.googleapps.com/apps/messageheader/)

---

## Recommendation

Do **not** interact with any links or reply to this email. Report such messages to `spoof@paypal.com` and delete them immediately.
