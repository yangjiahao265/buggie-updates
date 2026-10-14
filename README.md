# Buggie signed updates

Public Windows amd64 client archives and TUF metadata, signed by the existing Buggie publisher. This repository contains distribution assets only. The signing keys stay in the publisher's private store.

Metadata base: `https://raw.githubusercontent.com/yangjiahao265/buggie-updates/main/metadata/`

Targets base: `https://raw.githubusercontent.com/yangjiahao265/buggie-updates/main/targets/`

Bootstrap root SHA-256: `ca727a736dca0c90862eeaf0dde78e9fba4fc7ad1385ee2b277b754cd47cc029`.

The stable channel currently selects `0.2.10-99-windows-amd64`, build `9469e20a7fb2`. The previous `0.2.9-local.20261014.1-98-windows-amd64` archive remains an immutable signed target for verified recovery. A download or signature check alone does not authorize selecting an old program.

Installations must bootstrap the independently verified root, use HTTPS, and verify the complete signed archive. Windows service upgrades use the official administrator service-update transaction. Use the notify policy for manual installation.

The current targets, snapshot and timestamp expire 30 days after signing. Before expiry, the publisher must refresh them with the existing signing store and its monotonic version counter. Publishing renewed metadata does not install a client update. This repository has no automatic signing job.
