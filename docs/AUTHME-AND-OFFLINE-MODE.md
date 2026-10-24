# Offline-mode servers and authentication

On a directly accessible offline-mode Java server, the claimed username alone does not prove control of a paid Minecraft account. A name-based whitelist by itself cannot supply that missing identity check. Decide whether offline mode is necessary before adding more moving parts.

## Paper and Spigot: AuthMe Reloaded

[AuthMe Reloaded](https://github.com/AuthMe/AuthMeReloaded) is a server-side authentication plugin. Check the publisher's supported server versions and release instructions before installing it. Make a backup, install a compatible official release, and review the generated configuration against the [current configuration documentation](https://github.com/AuthMe/AuthMeReloaded/blob/master/docs/config.md).

Review what unauthenticated users can do: movement, interaction, commands, registration, login, and reconnect/session behavior. Protect administrative identities and the authentication database. Choose the publisher-supported password-storage settings and keep the database private.

Use disposable test accounts to check registration, correct and incorrect passwords, reconnect behavior, and whether any actions are possible before authentication. Verify the installed combination of server, proxy, permissions, and plugins. A plugin name in a server list does not prove that the server is configured safely.

If there is a proxy, follow AuthMe's [proxy configuration guidance](https://github.com/AuthMe/AuthMeReloaded/blob/master/docs/proxies/configuration.md) as well as the proxy's network-security instructions. Do not expose backend servers directly.

## Fabric and other modded servers

Choose a maintained **server-side** authentication mod that explicitly supports the exact Minecraft and loader versions you run. Test it before opening access. The [axieum/AuthMe client mod](https://github.com/axieum/authme) helps a client sign back into its own account; installing it does not add authentication protection to a Minecraft server.

## Recovery and maintenance

Back up authentication data together with the relevant world, permissions, and server configuration. Protect those backups as sensitive data. Record versions and restore the combination in isolation before relying on it. Consult the publisher when upgrading or migrating password databases; do not guess at compatible settings.

Read the [server-security checklist](WHITELIST-AND-SECURITY.md) and [backup guide](BACKUPS-AND-RECOVERY.md) too.
