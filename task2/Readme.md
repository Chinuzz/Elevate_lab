
Phishing Email Analysis — README
Overview

This README explains a repeatable, step-by-step process for analyzing suspected phishing emails. It contains a realistic sample phishing message (headers + body) and an 8-step checklist you can apply to any suspicious message to determine if it is malicious.

Purpose

Use this guide to:

Recognize common phishing indicators.

Inspect email headers and sender details safely.

Identify malicious links or attachments.

Produce a short, actionable report you can share with security teams or your email provider.

Sample (for training only)

From: accounts@paypa1-secure.com
To: you@yourdomain.com
Subject: Urgent: Your PayPal account has been LIMITED — verify now

Body (example):

Hello Customer,
We detected suspicious activity on your PayPal account and have temporarily limited access to your funds. To restore full access you must verify your account within 24 hours.
Click here to verify: http://bit.ly/verify-paypal-now
Alternatively download the attached secure form and submit it back to us: Account_Verify_Form.pdf.exe
Failure to verify within 24 hours will result in permanent account suspension.
Thank you,
PayPal Security Team

Example headers (simplified)

Return-Path: <accounts@paypa1-secure.com>
Received: from mail2-45.serverhosted.net (45.88.102.77) by mx.yourmailprovider.com
Reply-To: support@paypalsecure.helpdesk.ru
DKIM-Signature: d=paypa1-secure.com ...

Note: the above sample is fictional and meant for training and practice only.

8‑Step Analysis Checklist

Follow these steps for every suspicious email. Save a copy of the message and do not click links or open attachments when testing.

Obtain a sample

Save the full email (headers + body). Work on a copy. Do not interact with links or attachments.

Examine the sender address

Compare the From: domain to the legitimate organization (e.g. paypal.com). Watch for character swaps (e.g. paypa1-secure.com).

Check Reply-To for a different/fishy domain.

Inspect full headers

Use an email header analyzer to parse Received: hops, originating IP, and show SPF/DKIM/DMARC results.

Look for mismatches between the sending domain and the signing domain or failing authentication checks.

Identify suspicious links & attachments

Hover (don’t click) to compare visible text vs href.

Expand shortened URLs (add + for bit.ly or use a link expander) before visiting.

Treat double-extension files (e.g. .pdf.exe, .doc.scr) as malicious.

Scan for urgency/threats

Phishers press with deadlines or threats ("24 hours", "account suspended"). This is a common social-engineering tactic.

Check for mismatched URLs

Confirm the final landing domain belongs to the legitimate service. If the email says paypal.com but the link goes elsewhere, it’s suspicious.

Verify spelling & grammar

Poor language, odd capitalization, or formatting issues increase the likelihood of phishing.

Summarize findings

List the red flags discovered: spoofed domain, differing Reply‑To, broken header auth, shortener/mismatched link, dangerous attachment, urgency, typos.

Recommended Immediate Actions

Do not click links or open attachments.

Visit the service directly (type the URL or use a known bookmark) and verify your account status.

Mark the email as phishing/spam in your mail client and report it to the impersonated company (e.g. phish@paypal.com) and your security team.

If credentials were entered, change passwords immediately and enable MFA.

If you suspect malware, isolate the device and run a full AV/malware scan or contact incident response.

Quick Copy‑Paste Checklist

Check From: domain and Reply‑To.

Inspect headers (originating IP, SPF/DKIM/DMARC).

Hover links; expand shortened URLs.

Never open double‑extension attachments.

Watch for urgent/threatening language.

Look for spelling/grammar errors.

If suspicious, access account via official site and report the email.

How to use this README

Keep this file in your security playbook or intranet.

When you receive a suspicious email, copy the full message into a working file and follow the 8‑step checklist.

Use the Quick Checklist for triage and the Recommended Actions for remediation.

Contribution & Feedback

If you find additional common phishing techniques or want templates for reporting to different providers, add a contribution or open an issue in this repository.

License

This guide is provided as-is for educational and defensive use.

Prepared for training and incident triage — exercise caution and never interact with suspected phishing content on a production device.
