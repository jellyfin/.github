# Security Policy

## Supported Versions of Jellyfin Server/Web

Only the **most recent stable release of Jellyfin server** is guaranteed to have security patches applied. **Running older stable versions may leave you vulnerable to security risks**; always run the latest version, or avoid exposing your instance to the public Internet to minimize risk. Further, please always understand that providing a person Administrator access to your Jellyfin server is a risk, as Administrators can perform many destructive or damaging actions, regardless of any potential security issues.

As such, this security policy only applies to the most recent stable version of Jellyfin. Flaws present in old stable versions which are not present in the current stable version **will not** be fixed.

## Supported Versions of other Jellyfin Projects (Plugins, Clients, etc.)

Most Jellyfin projects are only supported for their most recent release. Please see any project's README for cases where this may differ.

## Vulnerability Triage

We ask you to please review the following details before reporting an issue.

* We are aware that many Administrator-level API endpoints may have inherent security risks. Due to the internal details of Jellyfin works, many of these are unavoidable, and we expect users to understand that providing Administrator access to a Jellyfin server is very sensitive and requires careful consideration. We consider any vulnerabilities that **exclusively require administrator-level privileges** to be a low priority, and those should be disclosed in normal GitHub Issues and shall be considered and fixed like any other bug, if possible.

* We have a public list of known (mostly Administrator-level as mentioned above) vulnerabilities in [this issue on the main repository](https://github.com/jellyfin/jellyfin/issues/5415). If your vulnerability is **already disclosed there**, please do not duplicate effort by re-reporting it to our security team.

* Vulnerabilities that **can not be exploited remotely** are considered low- to medium-priority bugs instead. For example, anything that requires shell access to the Jellyfin server, manual manipulation of the databases, etc. 

* We **do not accept automated/AI-generated security reports**, in line with our broader [LLM policies](https://jellyfin.org/docs/general/contributing/llm-policies). These are so prone to false-positives and overanalysis that we simply do not have the time to evaluate them all. Don't submit anything you have not personally validated yourself, as a human being, and have a reasonable PoC for.

* We **do not offer bounties** in any form. We request that you report bugs to help the software, not to make some quick money; after all, none of us who are fixing them are paid either.

* Do not overexaggerate vulnerability scores. Calling something a 9 or 10 will not get it seen/addressed any faster just because of this. Score your vulnerabilities appropriately.

* Vulnerability reports about our project infrastructure (our forums, servers, CI/CD, etc.) are welcome, but please tag those separately with `[Jellyfin Infrastructure]` in the email subject instead of the tag mentioned below. Please also be aware that our server infrastructure team does follow the news and has a standard patch policy, so duplicating publicly-known vulnerabilities here is not usually necessary.

## Reporting a Vulnerability

Once self-triaged and found to be a new and relevant vulnerability, please reach out for responsible disclosure via **an email to `security <at> jellyfin <dot> org`**. We do not accept ANY other methods of reporting vulnerabilities privately, as we have a number of workflows built around this email.

When providing a report, please ensure that you:

1. Begin your e-mail subject with `[Jellyfin Security]` or your private Matrix room with some variation thereof.

2. For email write only in **plain text**; do not use HTML, special formatting, embedded images, etc.

3. Start with an "overview" section, **written for public view**, that describes at a high level what is affected, and the possible consequences. Ideally, we will use this verbatim as the **public, user-facing** description of the GHSA.

4. Continue on with a "details" section outlining any code or API investigation you have done and, if possible, any suggested fixes. Please provide as much context and detail as you can, including, ideally, a process for reliably triggering the vulnerability so we may test fixes with it.

5. Please provide your GitHub username and (optionally if desired; please specify) real name so we may invite you into the GHSA and provide proper credit.

Once a report is received, it will be reviewed and, if applicable, we will create a GHSA and invite the reporter as well as the relevant team(s) to discuss the issue and work towards a fix.

## Post-Disclosure Process

As a pure volunteer project, **we recognize that we may sometimes be slow to handle vulnerabilities**; we greatly **appreciate patience and the absence of arbitrary timelines for disclosures**, especially for complex vulnerabilities. This includes initial responses. You are welcome to send follow-up emails if things go too long without a reply, though please remain polite and patient.

Generally speaking, unless we are very close to a new major release, we will create a point release for any fixes for major vulnerabilities as soon as possible. When close to a new major release, we may wish to defer the fix to the major release instead to avoid duplicated work.

Once a new version of the server is released, **we will wait at least 14 days (2 weeks) to publish our GHSA**. We believe this time is a fair balance between quick disclosure and the time needed by the majority of users to update their instances. We ask that all 3rd party disclosures (blog posts, etc.) occur **after** our GHSA is published.

CVEs will be requested by us through the GitHub Security interface and published along with the disclosure.
