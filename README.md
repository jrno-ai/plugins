# JRNO plugin

Save useful notes, ideas, and research from your assistant to your JRNO workspace.
The plugin includes four skills that identify useful information, clean it up,
send it to JRNO when asked, and explain how to use the integration.

## Install in Claude Desktop

1. Open **Customize → Plugins → Add → Add marketplace → Add from a repository**.
2. Enter `https://github.com/jrno-ai/plugins`.
3. Open the **jrno-prod** marketplace and install **JRNO**.
4. Open the plugin's **Connectors** tab, add/connect JRNO, sign in, and choose your workspace.

Try: “Send these meeting notes to JRNO.” The plugin prepares the useful material
before sending it. Review sensitive material before sharing it with your workspace.

The plugin includes the remote MCP connection at `https://api.jrno.app/mcp`.
Installing only a custom MCP connector does not install these skills.

## Install in Claude Code

Run these commands inside Claude Code:

```text
/plugin marketplace add jrno-ai/plugins
/plugin install jrno@jrno-prod
```

Use `/mcp` to connect JRNO and authorize your workspace.

## Updates

This repository is generated after successful JRNO production deployments.
Changed skills receive a new plugin version. Updates include all four skills
and the plugin's connection configuration.

In Claude Desktop, turn on **Sync automatically** for this GitHub marketplace.
Once a new version syncs, your installed plugin updates automatically, including
its skills, without another acceptance step. Select **Check for updates** to
pull the latest version manually. Updates are not guaranteed to arrive immediately
after a deployment.

In Claude Code, enable auto-update for **jrno-prod** in `/plugin` → **Marketplaces**,
or update manually with `/plugin marketplace update jrno-prod`.

See [Claude plugin installation and updates](https://claude.com/docs/plugins/overview#manage-installed-plugins)
and [Claude Code update behavior](https://code.claude.com/docs/en/plugins/host-marketplace#keep-users-up-to-date).
