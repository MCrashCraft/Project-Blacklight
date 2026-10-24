# Whitelisting and Java server security

For a small private Java server, enable Microsoft/Minecraft account authentication and allow only the players you intend to admit. Back up the server before changing its configuration.

## Enable the whitelist

On a directly accessible Paper or vanilla Java server, review these `server.properties` settings:

```properties
online-mode=true
white-list=true
enforce-whitelist=true
```

Use each player's actual Minecraft Java profile name. In the server console, run:

```text
whitelist add YourJavaUsername
whitelist on
whitelist list
```

In-game commands require permission and a leading `/`. Restart when changing startup properties, then test with one approved account and one unapproved account. Check the behavior you observe rather than assuming the file alone proves access is restricted. See the [Paper property reference](https://docs.papermc.io/paper/reference/server-properties/) and [command reference](https://docs.papermc.io/paper/reference/commands/).

## Protect administration

- Give operator access sparingly and review permission groups.
- Update the server and use maintained plugins from their publishers.
- Protect hosting-panel, SSH, and website accounts with strong unique passwords and multifactor authentication where available.
- Restrict RCON, database access, and management panels to trusted access paths.
- Keep backup copies on separate storage and test restoration.

## If you use a proxy

Proxy deployments require their own authentication and forwarding configuration. Prevent players from bypassing the proxy and connecting directly to backend servers. Follow the publisher's [Velocity security guide](https://docs.papermc.io/velocity/security/) and [player-information forwarding instructions](https://docs.papermc.io/velocity/player-information-forwarding/). Forwarding configuration and network access controls both matter.

If you intentionally operate in offline mode, read the [authentication guide](AUTHME-AND-OFFLINE-MODE.md) before relying on player names or a name-based whitelist.
