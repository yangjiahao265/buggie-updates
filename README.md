# Buggie signed updates

Public Windows amd64 client archives and TUF metadata, signed by the existing Buggie publisher. This repository contains distribution assets only. The signing keys stay in the publisher's private store.

Metadata base: `https://raw.githubusercontent.com/yangjiahao265/buggie-updates/main/metadata/`

Targets base: `https://raw.githubusercontent.com/yangjiahao265/buggie-updates/main/targets/`

Bootstrap root SHA-256: `ca727a736dca0c90862eeaf0dde78e9fba4fc7ad1385ee2b277b754cd47cc029`.

The stable channel selects `0.2.12-103-windows-amd64`, build `0465f9c7331a`. Its archive SHA-256 is `db6e5bf38512223c28108a16fa85dc3efa55beaa109d2bcf3769628cb8767f32`. Generation 101 remains an immutable signed target for verified recovery. A download or signature check alone does not authorize selecting an old program.

Generation 99 was superseded before a production installation. Generation 100 adds the Windows administrator token-owner alignment fix and passed the complete temporary SCM signed-update acceptance with race checking.

Generation 101 also preserves the protected machine program root when configuring trust on an existing Windows service installation. It passed the complete temporary SCM signed upgrade and a real installed-root trust refresh without changing the root's security descriptor. On 2026-10-14, the production Windows device completed the official HTTPS signed service update to generation 101. Workspace search, all five sort fields in both directions, pagination, successful-open access counts, restart persistence and a temporary 129th registration passed live acceptance. The original 128 registrations and stable bootstrap were preserved.

The initial upgrade attempts were safely aborted because 32 older command receipts failed to persist. The owner explicitly accepted the possible loss of those unpersisted receipts and authorized a normal service restart. Background maintenance was drained with a temporary pause before the successful update, then normal admission was restored. A zero failure count in the new process does not prove the older receipts were recovered or their persistence defect was repaired.

Installations must bootstrap the independently verified root, use HTTPS, and verify the complete signed archive. Windows service upgrades use the official administrator service-update transaction. Use the notify policy for manual installation.

Generation 103 adds explicit Codex/Fork/source-folder imports with owner-controlled permissions, paginated workspace queries and bounded metadata scanning. It also adds configurable checkpoint byte ceilings, bounded recovery inspection memory, and a fix for background command receipts inheriting an expired invocation lease. Generation 102 was superseded before publication. Generation 103 passed the complete temporary SCM signed upgrade with race checking, real owner/worker startup and old/new native MCP continuity (304.680 seconds). That test used a synthetic loopback TUF origin. The installed production device acceptance is recorded separately; signing or publishing this inventory does not demonstrate an installed upgrade.

The current targets, snapshot and timestamp expire 30 days after signing. Before expiry, the publisher must refresh them with the existing signing store and its monotonic version counter. Publishing renewed metadata does not install a client update. This repository has no automatic signing job.
