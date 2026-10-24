# Backups and recovery

A backup becomes useful when you can identify its contents and restore them successfully.

## Create a consistent recovery set

For a straightforward manual backup, arrange downtime and stop the server cleanly before copying files. Include every world and dimension, server configuration, plugin/mod data, and the exact version list. External databases need their own consistent export; record how their timing relates to the world copy.

Keep private keys, credentials, authentication databases, and administrative configuration private. Store at least one copy away from the original server and retain older recovery points so recent damage does not replace every useful copy.

Record the backup time, source, file inventory, sizes, and hashes. Check the archive or repository for integrity. A matching checksum detects changes to the bytes; it does not establish that the world is complete or playable.

## Test restoration

Restore a copy into an isolated environment with public access disabled and a separate port or network. Match the required Minecraft, loader, plugin, mod, and database versions. Inspect important builds, inventories, dimensions, and permissions. Record the exact backup tested, problems found, and validation result.

Do not overwrite the only original while testing. Keep a rollback path when returning a repaired world to service.

## Respond to griefing

1. Restrict access and preserve the original damaged state.
2. Record affected locations, dates, screenshots, logs, and what remains uncertain.
3. Find a trustworthy baseline or backup and compare its coverage.
4. Repair or restore an isolated copy with the owner's agreement.
5. Have the owner validate the result before reopening access.
6. Archive the evidence and a tested recovery point.

## Understand client-capture limits

A client capture records data the client actually receives. Unvisited chunks, unopened containers, server-side plugin data, and the true world seed may be absent or unknown. A playable local copy does not prove a complete world backup. Record coverage and omissions, and prefer an owner-provided server export when available.

See the [preservation workflow](PRESERVATION-WORKFLOW.md) for case documentation and validation gates.
