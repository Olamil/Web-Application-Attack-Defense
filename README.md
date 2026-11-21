# Web Application Attack & Defense

This lab combined hands-on web application testing with defensive configuration. I tested SQL injection and cross-site scripting (XSS) against DVWA, then enabled ModSecurity and repeated the tests. I also reviewed the configuration of a PrestaShop deployment hosted using AWS EC2 and Amazon RDS.

## Environment
Kali Linux, DVWA, Apache2, ModSecurity, AWS EC2, Amazon RDS, PrestaShop.

## What I did
1. Tested SQL injection and XSS against the deliberately vulnerable DVWA application. The initial test payloads succeeded.
2. Configured ModSecurity and repeated those tests. The tested requests were blocked.
3. Reviewed the deployed PrestaShop application against a security checklist: modules, administrator access, permissions, directory listing, session cookies, TLS, and backups.
4. Tested the PrestaShop search function with SQL injection and XSS inputs. Both tested requests returned HTTP 403; the tested JavaScript did not execute.

## Findings and limits
The results show that the tested inputs were rejected after defensive controls were applied. They do **not** establish that every SQL injection or XSS variant is blocked or that the application is free of vulnerabilities. I also encountered a ModSecurity parser conflict when attempting additional custom PrestaShop rules; that work was not completed as intended.

## What I learned
A before-and-after test is more useful than simply saying a WAF was installed. The test result matters, and so do its limits. Application hardening also involves configuration decisions beyond a WAF.

## Evidence to add
See `EVIDENCE_CHECKLIST.md`. Original lab screenshots and exact configuration files are not included in this package because they have not been verified for safe publication.

## Original project report
[Read the lab report in Google Drive](https://docs.google.com/document/d/15MkL8CJB5ZKJzVCS04rlz0oFkgM292fHqMX-OZ__Cqo/edit)

> All security testing described here was carried out in a controlled lab environment.

## Screenshots from my lab report

These are extracted from the original project report, not simulated results. The source page number is retained in each filename.

![Lab evidence from report, page-02-figure-01.jpg](evidence/page-02-figure-01.jpg)

![Lab evidence from report, page-02-figure-02.jpg](evidence/page-02-figure-02.jpg)

![Lab evidence from report, page-02-figure-03.jpg](evidence/page-02-figure-03.jpg)

![Lab evidence from report, page-03-figure-01.jpg](evidence/page-03-figure-01.jpg)

![Lab evidence from report, page-03-figure-02.jpg](evidence/page-03-figure-02.jpg)

![Lab evidence from report, page-03-figure-03.jpg](evidence/page-03-figure-03.jpg)

![Lab evidence from report, page-03-figure-04.jpg](evidence/page-03-figure-04.jpg)

![Lab evidence from report, page-03-figure-05.jpg](evidence/page-03-figure-05.jpg)

![Lab evidence from report, page-06-figure-01.jpg](evidence/page-06-figure-01.jpg)

![Lab evidence from report, page-06-figure-02.jpg](evidence/page-06-figure-02.jpg)

![Lab evidence from report, page-07-figure-01.jpg](evidence/page-07-figure-01.jpg)

![Lab evidence from report, page-07-figure-02.jpg](evidence/page-07-figure-02.jpg)

![Lab evidence from report, page-08-figure-01.jpg](evidence/page-08-figure-01.jpg)

![Lab evidence from report, page-08-figure-02.jpg](evidence/page-08-figure-02.jpg)

![Lab evidence from report, page-08-figure-03.jpg](evidence/page-08-figure-03.jpg)

![Lab evidence from report, page-08-figure-04.jpg](evidence/page-08-figure-04.jpg)

![Lab evidence from report, page-09-figure-01.jpg](evidence/page-09-figure-01.jpg)

![Lab evidence from report, page-09-figure-02.jpg](evidence/page-09-figure-02.jpg)

![Lab evidence from report, page-09-figure-03.jpg](evidence/page-09-figure-03.jpg)


> Evidence note: Screenshots were extracted from the report. Review the images for any account identifiers or other details you would prefer not to make public before publishing.
