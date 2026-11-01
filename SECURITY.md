# Security Policy

## Supported Versions

TimeCraft is in active development. Security fixes are applied to the latest
code on the default branch of each published repository; there are no
versioned release branches yet.

| Component | Branch | Supported |
| :--- | :--- | :--- |
| All published repositories | default branch | Yes |
| Older snapshots | — | No |

## Reporting a Vulnerability

Please **do not** file public issues for exploitable vulnerabilities.

Use GitHub's private vulnerability reporting: open a **Security Advisory** on
the repository affected (Repository → Security → Report a vulnerability). If
you are unsure which repository is affected, report it on any published
repository and the maintainers will redirect it.

When reporting, include:

- the affected component and version or commit;
- a description of the impact and the steps to reproduce;
- any known mitigations.

You will receive an acknowledgement within 7 days. After triage, the
maintainers will keep you informed of the remediation plan and will credit
reporters who wish to be credited once a fix is released.

## Scope Notes

TimeCraft is designed to minimize its security surface:

- Family data is stored **locally** on the family's own computer; the
  components do not transmit usage data to third-party services.
- The synchronization relay is **stateless** and routes encrypted messages
  without retaining family data.

Reports about the local administrative password flow, the device pairing
protocol, the D-Bus interfaces, and the relay's routing and rate limiting are
especially welcome.
