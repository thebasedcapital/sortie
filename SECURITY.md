# Security

Sortie is in TestFlight beta. Please do not open public issues for vulnerabilities or sensitive account data.

## Reporting A Vulnerability

Use the GitHub private vulnerability reporting flow when available for this repository. If it is unavailable, open a minimal public issue that says you need a private security contact, without including exploit details, secrets, tokens, logs, or screenshots.

## Data Boundary

Sortie uses the iPhone as the command surface and the Mac CLI as the local execution environment. The relay server routes encrypted messages; device-held keys protect message content.

When sharing diagnostics, remove secrets, tokens, private repository names, file paths you do not want public, and any agent transcript content that should remain private.
