# Security Policy

## Supported Versions of Jellyfin Server
Only the most recent stable release of Jellyfin server is guaranteed to have security patches applied. Running older stable versions may leave you vulnerable to security risks; always run the latest version, or avoid exposing your instance to the public Internet to minimize risk. Further, please always understand that providing a person Administrator access to your Jellyfin server is a risk, as Administrators can perform many destructive or damaging actions.

## Supported Versions of other Jellyfin Projects (Plugins, Clients, etc.)
Most Jellyfin projects are only supported for their most recent release. Please see any project's README for cases where this may differ.

## Reporting a Vulnerability
Before reporting a vulnerability, please note that we are aware that many Administrator-level API endpoints may have security risks. Due to how Jellyfin works, many of these are unavoidable, and we expect users to understand that providing Administrator access to a Jellyfin server is very sensitive as mentioned above. Thus, we consider any vulnerabilities that exclusively require administrator level privileges to be a low priority, and those should be disclosed in normal GitHub Issues that can be fixed like any other bug.

For all other vulnerabilities, please reach out for responsible disclosure using one of the following channels:

1. An email to `security <at> jellyfin <dot> org`.
2. A Matrix DM to any member [of the core team](https://jellyfin.org/docs/general/about#core-team).
3. A private DM on [our Forum](https://forum.jellyfin.org) to any member of the core team.

When providing a report, please try as much as possible to do the following:

1. Start with an "overview" section, written for public view, that describes at a high level what is affected, and the possible consequences. Ideally, we will use this verbatim as the description of the GHSA.
2. Continue on with a "details" section outlining any code or API investigation you have done and, if possible, any suggested fixes. Please provide as much context and detail as you can, including, ideally, a process for reliably triggering the vulnerability so we may test fixes with it.
3. Please provide your GitHub username so we may invite you into the GHSA and provide proper credit.

Once a report is received, we will create a GHSA and invite the reporter as well as the relevant team(s) to discuss the issue and work towards a fix.

## Post-Disclosure Process

As a pure voluneer project, we recognize that we may sometimes be slow to handle vulnerabilities; we greatly appreciate patience and the absence of arbitrary timelines for disclosures, especially for complex vulnerabilities.

Generally speaking, unless we are very close to a new major release, we will create a point release for any fixes for major vulnerabilities as soon as possible. When close to a new major release, we may wish to defer the fix to the major release instead to avoid duplicated work.

Once a new version of the server is released, we will wait *at least* 7 days (1 week) to publish our GHSA. We believe this time is a fair balance between quick disclosure and the time needed by the majority of users to update their instances. We ask that all 3rd party disclosures (blog posts, etc.) occur after our GHSA is published.

CVEs will be requested by us through the GitHub Security interface and published along with the disclosure.
