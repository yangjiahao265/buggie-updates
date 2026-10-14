# Buggie signed updates

Public Windows amd64 client archives and TUF metadata, signed by the existing Buggie publisher. This repository contains distribution assets only. The signing keys stay in the publisher's private store.

Metadata base: `https://raw.githubusercontent.com/yangjiahao265/buggie-updates/main/metadata/`

Targets base: `https://raw.githubusercontent.com/yangjiahao265/buggie-updates/main/targets/`

Bootstrap root SHA-256: `ca727a736dca0c90862eeaf0dde78e9fba4fc7ad1385ee2b277b754cd47cc029`.

The stable channel currently selects `0.2.10-101-windows-amd64`, build `0dba43e0414c`. Its archive SHA-256 is `5570b916a5dfcb874ad1bee814a0db6e54011d3a1a1ef4b36febedf1df49590a`. The previous `0.2.9-local.20261014.1-98-windows-amd64` archive remains an immutable signed target for verified recovery. A download or signature check alone does not authorize selecting an old program.

Generation 99 was superseded before a production installation. Generation 100 adds the Windows administrator token-owner alignment fix and passed the complete temporary SCM signed-update acceptance with race checking.

Generation 101 also preserves the protected machine program root when configuring trust on an existing Windows service installation. It passed the complete temporary SCM signed upgrade and a real installed-root trust refresh without changing the root's security descriptor. The existing production device has not switched programs: the official upgrade was safely aborted because 32 older command receipts failed to persist.

Installations must bootstrap the independently verified root, use HTTPS, and verify the complete signed archive. Windows service upgrades use the official administrator service-update transaction. Use the notify policy for manual installation.

The current targets, snapshot and timestamp expire 30 days after signing. Before expiry, the publisher must refresh them with the existing signing store and its monotonic version counter. Publishing renewed metadata does not install a client update. This repository has no automatic signing job.
