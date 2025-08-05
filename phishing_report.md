# Phishing Email Analysis Report

## 1. Email Overview
- **Sender:** PayPal Security `<support@paypal-account-secure.com>`
- **Subject:** [Action Required] Suspicious Activity Detected on Your Account
- **Claim:** Suspicious activity detected, account access limited.
- **Action Prompted:** Click “Verify Now” to restore access.

## 2. Sender's Email Address Analysis
- **Observed Email:** support@paypal-account-secure.com
- **Legitimate Email Expected:** support@paypal.com
- **Issue:** Domain spoofing using a lookalike domain.

## 3. Email Header Discrepancy
- Email headers are commonly used to validate a message’s source.
- In this case, full headers suggest spoofing and failed authentication.
- See detailed header analysis in [`phishing_header_analysis.md`](./phishing_header_analysis.md)

## 4. Suspicious Links or Attachments
- **Link Text:** 👉 Verify Now
- **Issue:** Actual destination of the link is hidden and may redirect to a phishing site.

## 5. Urgent or Threatening Language
- “failure to respond within 24 hours will result in automatic account closure”
- “avoid permanent suspension”
- These are intended to create panic and provoke immediate reaction.

## 6. Mismatched URLs
- **Link verification recommended:** Hover over the link to inspect destination.
- **Phishing Indicator:** If not a paypal.com subdomain, it’s likely malicious.

## 7. Spelling and Grammar Errors
- “temporarirly” instead of “temporarily”
- “accout” instead of “account”
- “plesse” instead of “please”

## 8. Summary of Phishing Traits

| Trait | Description |
|-------|-------------|
| Fake sender address | support@paypal-account-secure.com |
| Urgent language | Threat of account closure in 24 hours |
| Suspicious link | Hidden destination |
| Spelling/grammar issues | Multiple typos present |
| Generic greeting | “Dear Customer” |
| Mismatched domain | Not a real PayPal domain |
| Lack of email signature verification | No mention of digital verification methods |

## Conclusion
⚠️ **This is a phishing email. Do not click on any links. Report the email to `spoof@paypal.com`.**

For deeper analysis, refer to [`phishing_header_analysis.md`](./phishing_header_analysis.md)
