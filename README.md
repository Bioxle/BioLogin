<div align="center">

# 🔐 BioLogin

**A configurable authentication plugin for Minecraft servers.**

Register, log in, and manage player authentication with customizable messages and straightforward setup.

[![Minecraft](https://img.shields.io/badge/Minecraft-1.8–1.17-62B47A?style=flat-square)](https://www.spigotmc.org/resources/88918/)
[![Platform](https://img.shields.io/badge/Platform-Spigot-orange?style=flat-square)](https://www.spigotmc.org/)
[![Version](https://img.shields.io/badge/Published_version-2.0-blue?style=flat-square)](https://www.spigotmc.org/resources/88918/)

[SpigotMC page](https://www.spigotmc.org/resources/88918/) · [Download published release](https://www.spigotmc.org/resources/88918/)

</div>

## About

**BioLogin** is a Minecraft login and registration plugin designed to provide a customizable authentication experience. It was originally released in February 2021 and received a major rewrite with version **2.0** in September 2021.

This repository is intended for BioLogin's ongoing redevelopment. **The features and compatibility listed under “Published version” refer to the existing SpigotMC 2.0 release, not to an unreleased 3.0 build.**

## Published version (2.0)

According to the original SpigotMC listing and release notes:

- 🔑 Player registration and login commands
- ⚙️ Configurable settings and customizable messages, including support for translating messages
- 🏠 Configurable login lobby using `/biologin setlobby`
- 🌐 BungeeCord support (added in 2.0)
- 🔒 AES-based password encryption (added in 2.0; **not equivalent to password hashing**)
- 🛠️ Bug fixes and performance improvements introduced in the 2.0 rewrite

### Minecraft compatibility

The original listing names **Minecraft 1.8 through 1.17** as tested major versions. This is historical compatibility information, **not a claim that BioLogin currently supports newer releases**.

| Release | Status |
| --- | --- |
| 1.8–1.17 | Listed as tested for the original plugin |
| 1.18 and newer | Not verified for the published 2.0 release |

## Installation (published release)

1. Download BioLogin from the [SpigotMC resource page](https://www.spigotmc.org/resources/88918/).
2. Stop your compatible Spigot server.
3. Place the `.jar` inside the server's `plugins/` directory.
4. Start the server to load the plugin and generate its configuration files.
5. Review and customize the generated settings and messages before allowing players to connect.

> **Security notice:** Version 2.0's release notes describe AES encryption for passwords. Reversible encryption is not a recommended password-storage design. Consider the published version a legacy release and evaluate its security before deploying it on a public server. Do not reuse important passwords on legacy authentication systems.

## Commands

Commands referenced in the original public listing:

| Command | Description |
| --- | --- |
| `/register <password> <password>` | Register a player account by entering the password twice |
| `/biologin setlobby` | Set the authentication lobby location |

The plugin also provides a login flow. Consult the published plugin or its generated help/configuration for the complete command and permission list; this README does not invent unverified permission nodes.

## Configuration

BioLogin's original release advertises customizable configuration and messages. Version 2.0 includes fixes for the `messages.yml` file and allows messages to be changed to another language.

After the first server start, check the generated files under `plugins/BioLogin/` and adjust them to your server's needs.

## BioLogin 3.0 — rewrite goals

The next major version is being redesigned with maintainability, security, and compatibility in mind. The items below are **goals, not shipped features**:

- [ ] Refactor authentication into clearly separated services and components
- [ ] Use a one-way password hashing algorithm such as Argon2id
- [ ] Add safe migration paths for existing accounts
- [ ] Improve login session management and abuse protection
- [ ] Isolate version-specific Minecraft API behavior
- [ ] Extend compatibility from Minecraft 1.8 to newer releases, with per-version testing
- [ ] Expand automated testing and documentation

## Building from source

The rewrite is planned as a **Java and Maven** project. Once the source is published and the build is configured, the expected build command is:

```bash
mvn clean package
```

Check the project's `pom.xml` and release notes for the required JDK and supported server versions. The build instructions above describe the intended Maven workflow and are not a guarantee that the repository is already buildable.

## Feedback and contributions

Bug reports, compatibility findings, and feature suggestions are welcome through GitHub Issues when enabled for this repository. Please include your Minecraft version, server implementation, Java version, and relevant logs, **without passwords or other secrets**.

## Links

- [Original SpigotMC resource](https://www.spigotmc.org/resources/88918/)
- [BioLogin 2.0 release notes](https://www.spigotmc.org/resources/88918/update?update=424918)

---

<div align="center">

Made by **Bioxle** · Not affiliated with Mojang or Microsoft.

</div>
