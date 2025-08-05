# Task 2: Phishing Email Analysis

## Objective
To analyze a phishing email sample and identify phishing characteristics in a suspicious email.

## Tools Used
- Email Header Analyzer (e.g., MXToolbox, Google Admin Toolbox)
- Manual inspection

## Files Included
- `sample_phishing_email.jpg` — Visual representation of the phishing email.
- `phishing_report.md` — Main report outlining the suspicious email elements.
- `phishing_header_analysis.md` — Detailed technical breakdown of the phishing email header.
- `README.md` — Overview and context for the analysis.

## Steps Followed
1. **Collected a phishing email sample** simulating a PayPal security alert.
2. **Inspected the sender’s address** — identified a spoofed domain (`support@paypal-account-secure.com`).
3. **Checked the subject line** for urgency: `[Action Required] Suspicious Activity`.
4. **Analyzed headers** using an online tool for return path, SPF, and DKIM mismatches.
5. **Hovered over hyperlinks** — discovered links to non-PayPal domains.
6. **Looked for urgency and threats** like *“automatic account closure”*.
7. **Noted grammar issues** like "plesse", "temporarirly", "accout" and incorrect formatting — common in phishing attempts.
8. **Compiled findings** into a report for training and awareness.

## Usage
These files are useful for:
- Educational training on email security.
- Demonstrating red flags in phishing attempts.
- Practicing incident response and awareness.

## Security Advice
- Never click suspicious links from unsolicited emails.
- Always check the full email address and domain.
- Use an email header analyzer to validate authenticity.
- Educate others to recognize and report phishing attempts.

## Conclusion
This task demonstrated how to detect a phishing email, exposing typical tricks used to deceive recipients. Recognizing these signs can prevent account compromise and data theft. Regular training and technical validation tools are key to strengthening email security posture.

---

⚠️ **Disclaimer:** This content is for educational and awareness purposes only. Do **not** interact with real phishing emails. Always report them to your organization’s IT or security team.
